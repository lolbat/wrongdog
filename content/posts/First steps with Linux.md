---
title: First steps with Linux
date: 2024-07-01T18:50:46-06:00
draft: false
description: What happens when a lifelong Apple guy starts using Linux?
tags:
    - Linux
    - LinuxMint
    - Apple
---

Moving to a new operating system can be difficult to say the least. The first Mac that I ever used was a Macintosh SE that the Linguistics department had in a student accessible lab. It only had Illustrator '88 installed and was there for staff and students to use to make illustrations for papers and manuscripts. It was how I learned Illustrator and how I was able to land a job at a reprographics company later that year using Illustrator on an SE 30.

For the longest time I availed myself of machines that were available either at work or at student labs at the university. It wasn't until 1993 that I was able to buy a [Macintosh Quadra 610](https://en.wikipedia.org/wiki/Macintosh_Quadra_610) and work at home. I quite literally wouldn't have had a career in design and layout without the Mac. I also am not sure if the software that powered the explosion of new design and typography in the 90s would even have been possible without the Macintosh. 

There were certainly issues with Macs at the time. They were slower than Intel PCs. No-one made games for them. Prior to Steve Jobs coming back and rescuing the company, they made a series of bland hardware and spent a lot of time trying to fix the Mac OS which was truly showing its age by then. The company was run by a series of uninspiring CEOs that didn't seem to really understand the Mac and what it was for. 

But even looking back at those days with my rose-coloured glasses removed, I think that the Macs I used and owned then felt more personal and also felt as if they were *my* computer. I tinkered with them. I changed settings. I installed whatever the hell I wanted. I started composing this on an M1 Macbook Air. It is very fast. It has quite a few very well crafted applications that I use on a daily basis. It doesn't seem as if this Mac is _my_ Mac. I can change the desktop picture. I can put some stickers on the lid of the laptop. But I feel as if I am missing an inherent part of owning a computer - the feeling that I can tweak and tinker to my heart's content and make the device truly mine. 

I have had a double handful of Macs over the years but the post-Jobs years have taken a heavy toll on my fanboy status. There are two major issues that have made me start to move away from Apple [^1]. The overall quality of the software that Apple writes has steadily declined. I have [discussed this](https://whatiswrongwithyourdog.netlify.app/posts/artisinalsoftware/) [previously](https://whatiswrongwithyourdog.netlify.app/posts/wtfapple/) and the issues don't really show any sign of improving. 

My other problem with Apple is that they are turning their platforms into systems that are not only closed off from other online stores or software sources but they are also eliminating a user's ability to create their own solutions and tweak their own machines. Back "in the day" you could use apps like [ResEdit](https://en.wikipedia.org/wiki/ResEdit) to change how to operating system and applications looked. You could even change the text in application dialogs if you wanted to. It was crazy. I once used ResEdit and another application to change the entire UI of a British republican coworker's Mac to be a homage to the recently departed Princess Diana. He was furious. It was an awesome prank.

There is something to be said to locking out some aspects of the computer from novice users. And there is also something to be said for making it more difficult for threats to be introduced into your system. Apple seems to have used that impetus to keep the OS and apps safe from malware and poor choices to close down as much of the OS and the hardware as they can. Especially on iOS. In fact, I suspect that iOS is the primary driver for the problems that I have with Apple. 

## When is a computer not a computer?

iOS proved to Apple that they could expand their "protection" of a user's device and use that power to silo the entire user experience. iOS apps, and the OS, are impenetrable to the average user. Apps are all placed in a hardened sandbox [^2] and it is next to impossible to access the application data unless the developer specifically allows you to. If you want to copy your save game files from an iPad to a Mac then you need to hope that the developer thought about that and added features to do so. Developers can also lock down the data and documents you create if they want to [^3]. 

iOS proved to Apple that there was a business model in ,locking down a device and forcing users to go through Apple or third-party developers [^4] for things as simple as changing the look and feel of the device or moving data. Apple also has a large lock on services on the devices. Music, movies, books and TV all have prominent Apple applications that control the market to such an extent that there are no effective third-party competition. Even though the Apple applications are typically second-rate at best. 

This lock-down allows Apple to increase their profits as they provide more and more of the core features of the device. And this appears to be a growing trend on the MacOS side of things as well. Want to resell your M1 laptop? [Good luck](https://www.vice.com/en/article/xgybq7/apple-macbook-activation-lock-right-to-repair). Want to run an app from a developer that isn't paying Apple a monthly fee? [Good luck](https://support.apple.com/guide/mac-help/open-a-mac-app-from-an-unidentified-developer-mh40616/mac).

With each new iteration of MacOS there are, for me at least, fewer and fewer reasons to use the device.

## Linux?

I have an old iMac that was previously being used to run Plex and serve movies and TV shows to the family. It has a very mediocre graphic card and we ran into an issue with it coming to a halt whenever it had to transcode any video or audio. As long as the files were being served to a laptop we were fine(ish) but if I watched anything using my iPad it would bring the server crashing down. It is still a very good machine as long as you don't want to do anything that uses the GPU.

I have been thinking about trying to use Linux for more of my day-to-day work but I didn't want to install it on my laptop [^5]. So I did some searching to see if there was a recommended distro to use on an old iMac and most of the results seemed to recommend using [LinuxMint](https://www.linuxmint.com/). I wanted to make sure that whichever distro I went with was aware of the particular Apple hardware used on the devices as well as having drivers for the Firewire ports.

So I downloaded the .iso for the recent release, flashed it to a USB drive [^6] and then installed it. 

### Install problems

I only ran into two problems with the install. The WiFi chip and the GPU weren't recognized by the installer and so didn't have drivers. Luckily (oddly) the Device Manager in LinuxMint did know what they were and what drivers they needed. My iMac had an Ethernet port so I was able to plug into my router and then download the required drivers. A reboot later and it was connected to WiFi and had the correct driver for my ancient GPU. In terms of issues that I have encountered in the past this was utterly inconsequential. 

## Using LinuxMint

So far I have moved my Python projects and my blog to the new Linux machine. PyCharm is available for Linux and I used Git to quickly copy my projects from Codeberg. Hugo was easy to install and I am using Obsidian, with a few plugins, to write this blog post. I am using a very old wired mouse until I install an app and drivers to use my Logitech trackball mouse. I managed to get Starship installed for my terminal prompt as well. I did need to replace all of the [Symbol font icons](https://whatiswrongwithyourdog.netlify.app/posts/symbolsasnerdfont/) though. 

Most of my issues so far have been with my MacOS muscle memory. I tried to Cmd-Tab to access my list of open apps. I keep hitting Cmd instead of Cntl when I am using a keyboard accelerator. 

### What is missing

There are a few things that are missing. I need to find a solution that matches the functionality of [Hazel](https://www.noodlesoft.com). That said, with this being a "work" machine I am not sure how many files I am going to be downloading that will need to be automatically routed to the proper directories. I also need to find a Linux app that is similar to [Alfred](https://www.alfredapp.com). Alfred is an application/command Launcher and those functions can probably be replaced with something like [Cerebro](https://www.cerebroapp.com). What I have not found, so far, is a replacement for the [Alfred Power Pack](https://www.alfredapp.com/powerpack/) which provides a rich visual programming system. Most of the blogging I do starts in Alfred with me using [the workflow I created](https://whatiswrongwithyourdog.netlify.app/posts/hugo-workflow/) to let me add and edit posts as well as stop and start the server. 

I install [Solaar](https://github.com/pwr-Solaar/Solaar) and that has allowed me to start using my Logitech M575 trackball mouse. With my hand and wrist pain the M575 is a must-have item on the desk. 

One major problem I have is with a lack of feedback in the OS when you launch an app. There isn't anything (that I can see) that shows you that the app/service is actually loading. I did try to install Steam and it was having some issue with the antique GPU on the iMac. Sadly there was no error that was being displayed other than in the logs. So the difference between Steam crashing and Obsidian launching was none. I suspect that there may be a setting to provide some sort of feedback. 

## Overall

I will qualify this by saying that I have only been using the new OS for a few days but so far it has been quite easy to use and except for the lack of a Dock you wouldn't really be able to know that I had changed the OS. I have most of the same, or similar, apps and I am using the same hardware. 

I don't really do anything that would stress the machine or the OS. I write into text files either in `.md` files or in `.py` files. That said, LinuxMint seems responsive and I haven't had any odd issues [^7] that have required trolling through search results or reddit posts to solve. All in all this has been quite a positive move and I look forward to not being reliant on Apple for the work I do. 

[^1]: Let me just say that being semi-retired has made this a much simpler process. I am not sure that it would be possible when I was actively freelancing. 

[^2]: Trying using Shortcuts to move files or documents from one app to another. 

[^3]: Thankfully not many do.

[^4]: Which Apple gets a significant cut of so in a sense it is still Apple. 

[^5]: I also don't know of any distros that support the M1 chip in any case. 

[^6]: Which I had to buy since the last time I used a USB flash drive 1GB was as big as they came. 

[^7]: So far. 