---
title: "The Kobo arrives"
date: 2024-06-19T10:07:26-06:00
draft: false
description: My new Kobo arrived and, as is the case with technology, has solved some problems and added a few more.
tags:
    - Kobo
    - iPad
    - Apple
    - iOS
---

Last week I purchased a [Kobo Libra Colour](https://ca.kobobooks.com/products/kobo-libra-colour) e-reader. There are three specific reasons why I picked it up. First, my arthritis is making it difficult to hold my iPad while reading. I have a cheap bamboo iPad stand that I use to hold the device when I watch videos or games and I had to resort to using that to hold the iPad while I read. It wasn't comfortable and it still, eventually, made my hand hurt. I also wanted to get away from using the Apple *Books* app to read digital books or PDFs. I have [mentioned my issues with *Books* before](https://whatiswrongwithyourdog.netlify.app/posts/wtfapple/) but the overall issue is that it never felt as if I could rely on the app (and iCloud) to deliver the minimal reading experience I needed. And finally, I am in a long term process of trying to weed myself off of Apple products. 

## Seems good so far

I haven't had any hands on experience with an e-reader since the [Rocket eBook](https://en.wikipedia.org/wiki/Rocket_eBook). It was an amazing product but it wasn't very comfortable to use. It used an LCD screen, held about 10 - 15 books and was heavy. The Rocket weighed about 625g as opposed to the 199g of the Kobo Libre Colour.  I did like it quite a lot despite the weight. 

The Kobo is 199g and it feels negligible when you hold it. It is certainly lighter than any of the paperback novels I am reading with it. I am still getting used to the screen. The refresh "flash" takes a bit to get used to and you do need to manually adjust the brightness and temperature of the screen manually. The colour screen is also much better than I thought it would be when reading graphic novels and comics. The type is quite legible and the colours are quite good as well. 

My only issue with it, so far, is that it is ungainly to get content on the Kobo. This is mostly due to the ease at which you can move files across devices with iOS and MacOS. Kobo does support Dropbox and Google Drive so I may have to resort to using Google Drive [^1]. 

The Kobo appears to do what it is intended to do and I am having a better experience using it when I remember that it isn't a tablet and is an e-reader. That said, the UI is a bit primitive. 

## A Package? How did that happen?

The very first issue I ran into was, as one can imagine, caused by Apple. All of the epub "files" I transferred to my Kobo ended up as a series of individual html and jpeg files. This issue is [at least seven years old](https://www.reddit.com/r/kobo/comments/63fsg7/kobo_aura_is_splitting_epub_files_into_html/). I don't know when Apple started doing this but I suspect that it was part of the authoring app they released. I don't recall Apple ever saying anything about this but that doesn't surprise me.

The solution was to download Calibre and then add the epub files to its library and use the e-reader tools in Calibre to transfer them to the Kobo. It seems extremely arrogant of Apple to do this but then there is a reason why I am trying to move away from Apple products. 

## How large?

My second issue was the size of graphic novel and comic files. Most of them are Zip archives with JPEG or PNG files and the images are typically very high resolution and quite large. They are certainly overkill for a Kobo e-reader screen. The device itself seems to have no issues with resizing the pages prior to displaying them but they take up a significant portion of the limited space that the Kobo has. 

This isn't an insurmountable problem but it did require some time and some Python coding to solve. As an aside, it still boggles my mind just how many solutions to my problems eventually involve Python. There are two steps involved. First you need to either use `unrar` or `unzip` to extract the files into individual bitmap files. Then you need to rescale all of the images and then create a new archive. This isn't difficult but it is tedious. 

I am currently [using a Python script](https://github.com/Dapbler/cbr2cbz) to do this but I want to try to find a better solution. That will involve either writing my own Python code or using some combination of Alfred and [Retrobatch](https://flyingmeat.com/retrobatch/) to do the work. The current Python solution iterates over all of the files in the source directory and this causes problems for me since I use [Hazel](https://www.noodlesoft.com/whats-new-in-hazel-5/) to automate processing my downloads. I can't find any way for Hazel to trigger an event when there are no longer any .cbr or .cbz files in the Download folder so automating it is currently tricky. 

## One down

So with this new addition I am one step closer to replacing my iPad. Despite my two main issues, the Kobo is easier to read with and, as an unexpected bonus, since it has no apps or even internet access I am less distracted when I use it. Which means that I have been reading more and for longer amounts of time. 

[^1]: There is more about this issue below