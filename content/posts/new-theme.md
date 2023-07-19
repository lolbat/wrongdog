---
title: A new theme approaches
description: Nothing makes you want a new theme like trying to edit the old one.
date: 2023-07-19T16:15:01.809Z
draft: false
tags:
  - CSS
  - Hugo
  - Theme
---

I did a few tweaks to the sidebar for the site the other day and I found it a lot more frustrating than I think it should have been. This site's theme is based on one that I found on the Hugo site. It works well and I had no major issues with it until I started to tweak the layout and typography. The theme is based on a theme that is based on a theme. You can probably see where this is going. There are three `.css` files that define the site's look and they all have overlapping definitions for selectors. It works but if you want to change something you have to look through three different files. And also look to make sure that there isn't something that is defined in a selector in one file that gets inherited in the others.

I was going to compile them all into a single file but that is never a good idea. Therein, as the kids say, lies madness. So I am going to work on my own theme. Then any mistakes and design problems are my fault.

Quite some time ago, when I used to do more web work, I was interested in trying to use the [Bulma CSS framework](https://bulma.io) as part of a design for a site. I never got the chance but I will be using it for my new theme. It is modular and has a syntactic style structure that I like. 

Wish me luck. 