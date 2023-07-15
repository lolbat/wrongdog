---
title: Visual Studio Markdown?
date: 2023-06-28T06:39:05.900Z
draft: false
description: Can you expand Visual Studio Code into a good Hugo CMS?
tags:
  - Hugo
  - Visual Studio Code
  - Markdown
  - Frontmatter
---

I think it should be known [^1] by now that I like Markdown quite a bit and I use it for almost everything I write. It lets me format content but not remove me from the process of writing. A format is only really as good [^2]  as the applications that support it though and while I have a Markdown editor that I am happy(_ish_) with there isn't really a good CMS system for Hugo [^3].

There are a few web-based systems that are available but they tend to be expensive and require your content to sit on someone's server. That seems to defeat the purpose of Hugo. All the content and the HTML is here locally and I can take my ball and go play somewhere else if I don't like a host. Leaving my content on a server is only a step away from using Wordpress. The Decap CMS will [work with Hugo](https://decapcms.org/docs/hugo/) but it seems a touch opinionated and also ties one closer into Netlify.

> If you look at many of the discontinued Hugo CMS projects, they all seem to have had a short shelf-life and not been updated in years. Combine that with the number of commercial Hugo CMS sites that are aimed at the business market and I think one is left with the conclusion that blogging is quite dead. At least as a commercial concern. I suspect that the few people that do want to write a blog use something like Wordpress [^4] or just content themselves with social media [^5]. Leaving the only commercial market for this type of tool being corporations.

## Visual Studio Code to the rescue?

There is a copy of Visual Studio Code on my hard drive from when I was testing Python IDEs. VS Code has a lot of extensions and there are many Markdown tools that you can add to it. Microsoft also has [a very nice article]((spit)) about how to kit out VS Code to use it for markdown.

The main tool that VS Code has available to it is the [Frontmatter CMS](https://frontmatter.codes/). It installs effortlessly into VS Code and it also effortlessly integrates with your Hugo installation.

![Very nice!](/images/pretty.jpg)

For me, the best part of the extension is that it has the above view of your content that you can use to see if you have posts still in Draft. I forget to set `draft` to `false` about once a week. You can quickly view all of the content types that you have in the site and Frontmatter reads them all in without you having to specify them.

And since VS Code [^6] can also double as a code editor you can also, if you so desire, edit your site's themes and other code in it as well.

## Problems

There are a few problems with using VS Code, or VS Codium, as a Hugo CMS.

The first issue is that text in the app looks like crap unless you are using a retina screen [^8]. This isn't the case with any of the native Mac apps that I have. You can attempt to disable the GPU rendering in an Electron app but that requires you to access `Preferences: Configure Runtime Arguments` from the Command Palette and then edit a `argv.json` file. Even if you do this, the text still isn't as crisp as it is in a native app. This is a longstanding issue that has been around for years.

Being an Electron app, VS Code also doesn't have access to the Mac system-level spellchecker. You can install a spellchecker and then install additional dictionaries if you need them [^7]. This isn't difficult to do but it does mean that the editor can't take advantage of your existing additions to the system spellchecker and that any new additions won't propagate to other apps.

VS Code can also create a very busy environment when you are using it. This isn't much of a problem when you are editing code. Writing an article or a blog post tends to be a more dense visual environment so the decorations that VS Code can add sometimes becomes a bit much.

![Not so pretty](/images/visualissues.jpg)

These can all be disabled but it does take a bit of time to fiddle with. Some of the settings are also not in the Settings tab but have to be modified in the VS Code settings json file. VS Code is similar to apps like Atom, Pulsar and Zed in that there are some basic settings for it in a UI but that is the thin sheet of ice covering an abyss of options that require the editing of json files and knowledge of the particular names of and values for the settings [^9].

## Good points

Most of the positive points of using VS Code as a Hugo CMS come from the Frontmatter extension. It helps you get quicker access to your files and media and makes it easier to add images to a Hugo document. Hugo stores media in the `static/images` directory but references them as `/images/`. While it is simple enough to manually add the correct path, it is nice to have a tool that will do that for you. Frontmatter also has a sidebar that lets you edit that YAML front-matter for a post, edit the title as well as the description. Frontmatter will also run code making it easy to [build new tools for your Hugo site](https://frontmatter.codes/docs/custom-actions).

I have spent the last few days installing Frontmatter first in VS Code and then in VSCodium so I could test it while I write this post. It was quite a PITA trying to get VS Code to look good. I suspect that some of this might have to do with it being set up to be used as a Python IDE. I did a fresh install of VS Codium and it was a much simpler process.

Microsoft doesn't allow third-party apps access to their VS Code Marketplace and so I had to download the extensions I needed from the [Open VSX Registry](https://open-vsx.org/). I currently have installed:

* Code Spell Checker
* Canadian English
* FrontMatter CMS
* Markdown Extended
* Markdown Footnote

That is enough to cover most of what I need to write and publish posts for my Hugo blog. I could do all of the Git commits to push the blog data to Codeberg and then to Netlify but I actually like doing them via the command line.

With this set up I am going to spend some time using it to write my blog posts and see how well it does or does not work.

[^1]: It is known, Khaleesi.

[^2]: Or as bad as, in the case of Office.

[^3]: Some people call Hugo a CMS but this is nonsense. Those folks are just writing SEO bullshit and don't know what they are talking about.

[^4]: (spit)

[^5]: (spit)

[^6]: Or [VS Codium](https://github.com/VSCodium/vscodium) if you want to avoid Microsoft seeing everything you do.

[^7]: If you are, like me, a Canadian who has a series of odd spellings.

[^8]: As I can confirm when unplugging my laptop from its dock and using the internal screen instead of my external screen.

[^9]: Why anyone would write an app like this is beyond me.
