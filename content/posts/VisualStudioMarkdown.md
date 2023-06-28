---
title: "Visual Studio Markdown?"
date: 2023-06-27T20:15:09-06:00
draft: true
description: "Can you expand Visual Studio Code into a good Hugo CMS?"
tags:
    - Hugo
    - Visual Studio Code
    - Markdown
---

I think it should be known [^1] by now that I like Markdown quite a bit and I use it for almost everything I write. It lets me format content but not remove me from the process of writing. A format is only really as good [^2]  as the applications that support it though and while I have a Markdown editor that I am happy(_ish_) with there isn't really a good CMS system for Hugo [^3]. 

There are a few web-based systems that are available but they tend to be expensive and require your content to sit on someone's server. That seems to defeat the purpose of Hugo. All the content and the HTML is here locally and I can take my ball and go play somewhere else if I don't like a host. Leaving my content on a server is only a step away from using Wordpress. The Decap CMS will [work with Hugo](https://decapcms.org/docs/hugo/) but it seems a touch opinionated and also ties one closer into Netlify.

> If you look at many of the discontinued Hugo CMS projects, they all seem to have had a short shelf-life and not been updated in years. Combine that with the number of commercial Hugo CMS sites that are aimed at the business market and I think one is left with the conclusion that blogging is quite dead. At least as a commercial concern. I suspect that the few people that do want to write a blog use something like Wordpress [^4] or just content themselves with social media [^5]. Leaving the only commercial market for this type of tool being corporations.

## Visual Studio Code to the rescue? 

There is a copy of Visual Studio Code on my hard drive from when I was testing Python IDEs. VS Code has a lot of extensions and there are many Markdown tools that you can add to it. Microsoft also has [a very nice article]((spit)) about how to kit out VS Code to use it for markdown. 

The main tool that VS Code has available to it is the [Frontmatter CMS](https://frontmatter.codes/). It installs effortlessly into VS Code and it also effortlessly integrates with your Hugo installation. 

[Very nice!](/images/pretty.jpg)

For me, the best part of the extension is that it has the above view of your content that you can use to see if you have posts still in Draft. I forget to set `draft` to `false` about once a week. You can quickly view all of the content types that you have in the site and Frontmatter reads them all in without you having to specify them. 



[^1]: It is known, Khaleesi.
[^2]: Or as bad as, in the case of Office.
[^3]: Some people call Hugo a CMS but this is nonsense. Those folks are just writing SEO bullshit and don't know what they are talking about. 
[^4]: (spit)
[^5]: (spit)