---
layout: post
title: "Weekly Report   1"
description: "Trump-Detect and other things in life"
category: Report
tags: [weekly]
---

Here is the weekly report of what I've been upto -- from 25th of June to the 1st of July!

I had a long chat with a mentor of mine - [Jaideep Bir](https://www.facebook.com/jaideepbir), regarding future possibilities within the domain of video and social media. I feel that [CaseyBot](https://github.com/shubh24/casey-compile) is something that is commercializable and thus we'll try and delve deeper into this domain.

My friend, [Gyanendra](https://github.com/h4ck3rk3y/) had built this Chrome extension -- [TrumpCat](https://gyani.net/blog/trump-cat/) that replaces images of Donald Trump with those of cats. However for Trump Detection, Alchemy Vision API was being called. Thus, I built Trump-Detect, which uses the LBPH Face Recognizer Module in OpenCV, which basically builds a histogram of deltas w.r.t each pixel. It then compares the histograms of test images for identification.

![Before and After]({{site.baseurl}}/images/before-after.jpg)

 I scraped Trump on Google Images for training the recognizer with around a hundred photos for now. The code is currently in production - the extension can be downloaded [here](https://chrome.google.com/webstore/detail/trumpcat/hfajcdnolhbfcbcfkjkppgjlmfidpnnd). Trump-Detect is an experiment which will lead to bigger projects - compilation of falling people, people saying stupid things etc.   

I have also started doing a bit of GeeksForGeeks, revising CS basics for the placement season. It is pretty tiring though. 
![Before and After]({{site.baseurl}}/images/gfg.jpg)

Me and Gyanendra have begun building another side-project - World-in-Pictures, based on building an API in the travel domain. More on that in the next week. 

I just returned from a meetup on Tech/Data in Investment & Trading. It was a good meetup - met some people working on awesome things in AI and Deep Learning. I'll try and pick up a good #Data project in the next week, and build something cool.

That's it folks!    