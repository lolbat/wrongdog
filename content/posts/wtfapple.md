---
title: WTF? Apple
description: For every thing that Apple does well it screws the pooch on many many more. Here are some of my most recent 'WTF?' moments in relation to Apple apps and OSes.
date: 2023-07-27T15:46:43.451Z
draft: false
tags:
  - Apple
  - MacOS
  - iOS
---

If you are on social media, or share FTF stories with Mac or iOS users, you will eventually see (or hear) the phrase "[Does anyone at Apple use...](https://www.google.com/search?q=%22Does%20anyone%20at%20Apple%20use%22)" [^1]. For quite a while I tended to see the phrase as something that marked people online that either didn't know how to access a feature [^2] or just didn't bother to look to see how to do something [^3]. And then I started to say it myself.

At first my use of the phrase was somewhat embarrassing. I saw it as a sign that my increasing age was starting to have an effect on my ability to understand the more arcane parts of MacOS and iOS. One thing I learned from my brief tenure on Mastodon was that I was not alone and that a lot of developers and folks that are much smarter than me have the same reactions. 

So here is a list of my current "WTF?" moments and issues when dealing with Apple. There are some [four letter words](https://word.tips/four-letter-words/). 

## Safari Widgets

I finally have an iPad that doesn't have a cracked screen and also lasts the entire day on a single battery charge and so I have been using it for a bit more than watching TV while I cook or do the dishes. The screen resolution is much better and so it is easier to read with [^4] and so I have been working through my backlog of ebooks and articles. 

I use Safari on my iPad and iPhone because Apple wants it that way. Consequently I use the Reading List and iCloud Tab features in Safari. Today I was adding an Unread Items widget from [NetNewsWire](https://netnewswire.com/) to my home screen. I had a lightbulb moment and went to add the Safari Reading List widget to the home screen as well.

But there isn't one. There are no Safari widgets. Want to access your Tab Groups? Fuck off. Want to open an article from your Reading List? Fuck you. Want to see your open iCloud Tabs? Go fuck yourself. 

Who writes an OS and then doesn't support one of its features with an app they are forcing you to use? At least mitigate the pain of forcing Safari on iOS users by giving them some useful widgets. iOS 17 will bring us more Stickers though. How is that for a "fuck you"?

## Safari data

This seems to be more of a continuing "go fuck yourself" than a "WTF?" but it appears to be impossible to programmatically access the iCloud Tabs you have open from anywhere other than Safari. If you search online you will see articles that will show you how it _used_ to be possible to do so. None of those techniques work with current versions of MacOS. A more paranoid person would think that Apple sees a post on StackOverflow about the subject and just moves the plist file or SQLite database to a new location.

You can access your bookmarks and Reading List but only by parsing a plist on your own using Alfred, Python or [something more baroque](https://www.npmjs.com/package/read-safari-reading-list). Shortcuts will let you add a URL to the Reading List but won't show you what is in it. I can't be alone in thinking that Apple should make it easier to access your own Safari data from another app [^5]? 

## Shortcuts

While we are on the subject, Shortcuts has to be the worst application that Apple has released. It borders on being unusable on the Mac, the UI on iOS is bewildering and the way the Actions work in Shortcuts change periodically breaking old scripts and making it a total PITA to work with someone who runs a different version of iOS or MacOS than you do. I was trying to help out a fellow in the UK with a shortcut he was running and some of the actions in it would return different values on my Mac. His conditional code had to be rewritten to work on my Mac. 

I also wrote a recent Shortcut on my iPad to rename files based on a regular expression. That part worked well enough but when I ran the shortcut through the Share Sheet it returned a "bookmark not found" error. Which was odd since I was processing files and not bookmarks at all. Even odder, it worked perfectly when I ran it via the Shortcuts app. 

Shortcuts is the first example I bring up when I talk about "Does anyone at Apple use...". It has so many bugs and the UI is so difficult to use that I can't imagine that anyone at Apple actually uses it for anything other than writing simple Gallery examples. 

## Books

My new iPad is a mixed blessing in one respect. Since it is easier to read ebooks and articles with I have been using Books more. The Apple e-reader is the default app on iOS and as such it has stifled any innovation in that area. When it works, it looks very nice and easy to use. Getting it to work is another matter. 

Here is a current list of bugs that are in Books that I run into on a regular [^6] basis. Some have been for some time:

* Books can't download files from iCloud when using cellular data. Even with that permission enabled.
* Books will remove the book you are reading from memory and from the file system whenever it needs room. No matter than there are any number of larger files on the device. It is even better when it does this when you are can't get wifi access and then can't reload the book.
* With the latest version of iOS when the book you are reading is removed the app will now just show a blank screen until you kick the Books app from memory.
* Syncing between devices was hit or miss in the past and is now mostly miss. 

And then there is the new UI. I am still trying to get used to it. I find it a usability nightmare. I also really enjoy having the app default to a screen that shows the Apple book store and not just a list of the books I have on the app.

If anyone at Apple uses the Books app to read they must be filled with a terrible and debilitating self-hatred that makes them think they deserve to have the application be so shitty. 

## Can you conclude by referring to something topical?

I was going to write about how this is all the fault of the time and effort being put into VisionOS but that seems a little too obvious. I actually think that no-one at Apple really cares about MacOS and that they have really run out of ideas in regards to iOS. Unless it is related to Services. 

I read an interesting article [about window management](https://blogs.gnome.org/tbernard/2023/07/26/rethinking-window-management/) on the GNOME OS this morning. It was quite interesting and had some bright ideas illustrated with some animations. After reading it I couldn't help but think that I have seen nothing from Apple about this. Well nothing usable [^7]. There are quite a few indie apps available that are trying to provide solutions but Apple doesn't seem to care. And that is the general feeling I get from them. I don't think the company sees any ROI from investing in MacOS and all of the efforts being made are to push iOS usage paradigms onto the Mac whether they work or not.

Maybe I will look at Linux, and GNOME, with a bit more interest. At least those devs seem to use the damn software they write. 

[^1]: Apologies for the link to Google.

[^2]: Not their fault

[^3]: Totally their fault.

[^4]: The lack of cracks on the screen helps.

[^5]: Who the hell do they think they are? Microsoft?

[^6]: Daily usually. 

[^7]: Stage Manager is a nightmare on the Mac. 