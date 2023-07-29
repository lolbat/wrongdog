---
title: More time with FrontMatter
description: "Some comments and observations based on some more time using the Front Matter CMS for Hugo. "
date: 2023-07-29T19:15:29.101Z
draft: false
tags:
  - Front Matter
  - Hugo
  - VS Codium
  - Marked
---

I have had more opportunity to use the [Front Matter CMS](https://frontmatter.codes/) for my blog posts and I thought I would take a moment to post about some of the observations I had. Both good and bad.

## The Bad

Lets get the negatives out of the way first. As with my [earlier comments](https://whatiswrongwithyourdog.netlify.app/posts/visualstudiomarkdown/), most of the negatives are a result of issues with VC Codium/VS Code and not Front Matter itself.

I am still trying to get used to how VS Codium looks and works. It isn't a native Mac app and so there are many things in it that are non-standard and don't work as they do in other apps. I have gotten used to how the spell-checker works but all of the muscle memory I am developing is only for VS Codium. As soon as I open another app I have to adapt to a new set of keyboard commands.

I spent some time looking through different themes to find one that looks good. Or at least better. I wasn't able to find one and so I am still using a default theme from VS Code. It is okay but it has the same "this will do" feel that most VS Code themes have. I suspect the core problem is Electron. I have seen themes that also have versions available for pyCharm and they look much better in PyCharm.

I have managed to track down a few extensions to add some of the functionality that I used to have in Typewriter and [Nota](https://nota.md/). They are available via the Command Palette which allows for quick access but also ends up with me selecting the wrong command since the order of them in the Command Palette changes each time you use them. 

I also had to change from using VS Codium to Visual Studio Code. Even though they supposedly use the same code base, VS Codium wasn't displaying the controls that Front Matter uses to insert images from the Media Panel. 

## The Good

Transferring from VS Codium to Visual Studio Code was simple. :-) It was actually painless. All my settings for Front Matter were in my Hugo directory and all of my VS Code settings were in my user directory. I was ready to go in seconds. 

Front Matter makes it quite easy to work with [Page Bundles](https://gohugo.io/content-management/page-bundles/) in Hugo.  And using Page Bundles makes it very easy to preview your posts in [Marked 2](https://marked2app.com/). As long as I am not adding images that are referenced from the `/images` directory. My [last post](/posts/evolutionofsummonerwars/) had quite a few images in it but I created it as a Page Bundle and Marked 2 could preview the images without any problems.

Marked 2 also has a better word count than the one that I installed in VS Code. The extension is telling me that I have 557 words while Marked is telling me that I have 525. So anything that makes it easier for me to use Marked 2 is a good thing. 

Now that I am using VS Code, the image functions in Front Matter work correctly and it is quite simple to add images into a post. With the correct paths which is the main issue with almost any other Markdown editor available. 

I quite like being able to see my Git status and also do a commit from within VS Code. I still forget to set my post's `Draft` status to `false` quite a bit but I am working on trying to solve that.

Front Matter also keeps a list of my tags and makes it easier for me to not mess up and either misspell a tag or not capitalise it consistently. 

## Overall

In general this has been a much better transition than I thought it was going to be. In some cases Visual Studio Code is overkill for what you need from a writing tool but Front Matter adds in enough useful tools for managing your Hugo content creation that it makes up for the additional complexity that the editor adds. 

I would still like to have a native app that could do all of this but given the many alternatives that I have used on my Mac this is about the best Hugo blogging tool I have run into. 

As well, there are possibilities to write my own code that would via Front Matter to let me add any specific functions I need. I don't have anything planned or even in mind but it is nice that the possibility is there if I do need it. 

Now I just have to find a theme that I like. 
