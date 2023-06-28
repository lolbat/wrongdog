---
title: "Hugo Workflow update"
date: 2023-06-27T18:33:02-06:00
draft: true
description: "I updated my Hugo Workflow for Alfred but not without a few issues cropping up."
tags:
    - Alfred
    - Hugo
    - Python
    - Homebrew
---

![The Hugo layout in all its glory](/images/hugoscreen.jpg)

Sometimes I don't even know why I start working on things. 

This morning I was sitting down in front of the computer getting ready to do something and I decided that I was going to add a new feature to the [Hugo Workflow](https://codeberg.org/lolbat/Alfred-Hugo) I created in Alfred. This was probably inspired by the Draft View in the [FrontMatter CMS](https://frontmatter.codes/) that you can run in Visual Studio. I thought that it was handy and decided to add it to the Workflow.

## The first issue

The code for it is quite simple. I wrote a Python script, based on a similar one I wrote for another Workflow, that got all of the Markdown files in the directory and then used the [python-frontmatter](https://pypi.org/project/python-frontmatter/) library to check the YAML frontmatter and look for posts where `draft: true`.

```python
#!/usr/bin/env python3

import os
import json
import copy
import frontmatter
from pathlib import Path

# get the content path from the Workflow
contentType = os.getenv("contentType")
contentPath = Path(os.getenv("hugoContentPath")) / contentType
fileList = []

# get all of the markdown files in it
directoryFiles = contentPath.rglob('*.md')

for post in directoryFiles:
    blogPost = frontmatter.load(post)
    status = blogPost["draft"]

    # if it is a draft then add it to the list
    if status:
        fileList.append(post)
```

The script then uses code pulled from my [Obsidian Bookmark Workflow](https://whatiswrongwithyourdog.netlify.app/posts/createobsidianlink/) to build the JSON data that the Alfred Script Filter uses to display the files.

It worked properly in PyCharm when I initially wrote it but when I dropped the code into the Script Filter in Python I got an error saying that the frontmatter library couldn't be found. This was odd. I did a `pip list` and then a `pip show frontmatter` command to make sure that it was loaded in the global Python install. When I issued a `which -a python3` command I was confused to see that it was pointing at the [Homebrew](https://brew.sh/) location for Python. 

I found this a bit confusing as I had [spent a fair bit of time](https://whatiswrongwithyourdog.netlify.app/posts/pythoncleanup/) making sure that my system wasn't using the Homebrew Python installation. I had stopped short of uninstalling Python from the Brew libraries but this time I pulled out my +1 Sword of `brew uninstall --ignore-dependencies python` and pulled the plug on Python [^3]. 

That fixed the issue in the Terminal and in my system but Alfred was still refusing to play ball. I am not sure why that is the case [^1] but luckily there is a simple solution.

### Take it outside

As you can see, from the code sample above, I made the code an external file and got Alfred to run it as an external process. This required a `chmod +x` to be run on the file and for it to be moved to the Workflow folder. Once I had done that, the problem was solved. Even though I am processing a **lot** of files in the directory it is actually fairly quick. So much for Python being slow. 

## Keep It Simple...

It was at this point that I realised that it would be much better if the Workflow used the same List Filter to allow the user [^2] to pick which content type they wanted to check. I initially had it just look through the `posts` directory but what if someone had a lot of different content types?

The _Add_ and _Edit_ commands in the Workflow already do this and I thought that it would be a good opportunity to simplify some of the code in the Workflow. Previously the _Add_ and _Edit_ commands had their own line of Actions that split from a single Conditional.

![The old Workflow](/images/hugoworkflow/workflowTitle.jpeg)

Each Command duplicated the List Filter but I didn't think it was a big deal since there was only two of them.

![A List Filter in a row](/images/hugoworkflow/addContent.jpg)

Somehow adding a third was a bridge too far for me and so I reworked the layout of the Workflow to avoid it. 

![The new Workflow](/images/newWorkflow.jpg)

The Workflow still has the same intro List Filter **1** but it now has a new Conditional block **2** that splits for the _Add_, _Edit_ and _Drafts_ commands. An Arg Action stores the selection the user made **3** and then displays the List Filter **4** to let them select a Content Type. This also means that the user only has a single List Filter to edit if they want to add new content types. 

Another Arg Action **5** stores the content type and then a second Conditional splits each command into its own stream. As an added bonus the _Edit_ and _Drafts_ Commands could use the same Bash Action **6** to open the file the user selects. 

It might look more complicated but it is actually an easier set of Actions to work with if I ever need to add new commands or tweak them. 

## Other tweaks

While I was digging around in the internals I rewrote the Python code for the _Edit_ Command so that it used Path instead of strings and `os` functions to do the path manipulation. Aside from looking better it also simplified that code considerably. The _Edit_ Command was also not working correctly. I am not sure when it broke but I suspect this speaks to how often I use the command.

I also fixed the "fix" that I had added to the _Start Server_ Command. I thought it was running correctly but whatever changes I thought I made were either wrong or didn't actually fix the problem. It works now. And it is simpler. That might have been the problem in the first place.

I'll be using this version of the Workflow for the next while and will see what sort of additions I want to make or perhaps even break the entire thing into smaller parts. 


[^1]: I am looking into this and have posted on the Alfred Forum about it. 
[^2]: Me in this case.
[^3]: I don't know how my Python settings changed but I would rather do without Python in Homebrew than have to solve that problem again.