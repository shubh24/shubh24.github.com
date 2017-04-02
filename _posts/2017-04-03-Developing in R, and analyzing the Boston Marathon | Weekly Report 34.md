---
layout: post
section-type: post
title: Developing in R, and analyzing the Boston Marathon | Weekly Report 34
category: report
tags: [ 'data science', 'kaggle', 'fitness', 'bangalore' ]
---

My weekly report from the 27th of March to the 2nd of April - good productive hours put in. Pushed out a data journalism blog. And also, Happy April Fools :)

At my internship, I've been developing this data platform for reports/visualizations in R -- it's coming along pretty well, but my confidence in getting it shipped is very shaky. A lot of stuff is hanging on loose strings, sql queries need to be verified and data validation shall be done. I've finally begun to appreciate the whole db schema design, getting a hang of it. Data requests are still tough for me to get around with, but i'm currently okay with extracting/visualizing the simple stuff. Patience!

On the renthop challenge, i've put in some effort on feature engineering with marginal gains. Got good jumps on my validation dataset, but not as much on the leaderboard -- Probably my gbm is overfitting, shall be experimenting with max_depth. Regarding features, i came up with a good concept map of the problem -- "Price" and "Interest Level" are the two primary features. Secondary features surrounding them are "Manager", "Town", "Neighborhood", "Building" and "Display Address". The secondary variables interact with the primary variable, either directly(eg. manager opportunity), or with another secondary variable (eg. manager nbd count). Going a little deep here, but this will help me documenting my thought process. I feel like i've got most of the important features covered, just need to optimize a subset to minimize overfitting. 3 weeks left in the competition, i hope to rank within the Top 40% :)

I worked on a Data Journalism project for the last couple of days, this had been irritating me on my March to-do list! Credits to Kaggle Datasets, i got hold of the Boston Marathon dataset -- comprising of every athletes splits timings, and his/her demographics. Put in good concentrated work, and came out with a [blog](https://shubh24.github.io/shubh24.github.com/math/2017/04/01/Running-the-Boston-Marathon,-with-Data!-Sports-Analytics.html) yesterday. Pushed it out as a Kaggle Kernel as well. Felt good!

I've been very slow on my side-projects, just writing about them in these weekly reports is not gonna do anything. Will focus on them this week. i got in touch with a guy from nyc, who wants my help in building a YouTube channel, with politics explainer videos from an Indian standpoint. Pretty interesting, psyched to contribute!

On the fitness front, i was consistent with the workouts this week. Knee seems to be recovering well. The tennis session was pretty good, getting the forehands back. Talking of tennis, Roger Federer seems to be on a roll, beating Nadal 4th time in a row! I'm betting on Federer for French, i know it's crazy but why not! #FedererForFrench

Later folks!