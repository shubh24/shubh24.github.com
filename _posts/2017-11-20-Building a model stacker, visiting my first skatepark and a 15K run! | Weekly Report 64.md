---
layout: post
section-type: post
title: Building a model stacker, visiting my first skatepark and a 15K run! | Weekly Report 64
category: report
tags: [ 'data science', 'myntra', 'skateboarding', 'vlog', 'fitness' ]
---

My weekly report from the 13th of November to the 19th of November -- a highly productive week, got a nice set of ToDos striked off my list!

*When feature engineering starts giving diminishing returns, you begin model stacking!*

I built a two-layer stacker of xgboost models, with different subsets of features passed in to models on the first layer. This gave us a nice 0.1 rise in precision at a certain recall value, they were high adrenaline moments :) I had to go through a couple of blogs to get a non-leaky stacker up and running -- its again one of those concepts in machine learning which works but you don't know why! 

We tried to scale my model to train on more data, given that more data has been giving us dividends. Ran into a couple of memory constraints over the weekend, getting cautious with my dataframes now! We're also seeing pandas perform terribly at scale, a complete shift to pure python data structures is on the roadmap :(

I also went through some research papers around the theme of feature engineering in similar problems. We haven't been extensive with the same, lots on the plate for V2. We're exploring opportunities to write one on the RTO problem once considerable progress is made. 

Haven't been able to scrape time for learning projects. Not cool.

The Kaveri Trail Marathon is less than a week away -- put in my last long run(15K @ 5:22) for the prep. Collected my marathon bib from Indiranagar, travel and acco sorted. Excited!

Met up with a lot of Pilani folks over the weekend! i was most excited about visiting the skatepark with [@sodhi](https://www.facebook.com/prabhjyot.singh.12), we tried going up and down the quarterpipes and failed terribly! It was one of those humbling experiences where you know you can do something, but your mind doesn't allow you to -- just a matter of practice. Muscle memory! i'm gonna be regular at the skatepark now, will try and visit it at least once a week :) 

Put out this week's vlog on our Play Arena experience -- had a lot of fun making it! 

<iframe width="560" height="315" src="https://www.youtube.com/embed/FPD_slwsnso" frameborder="0" allowfullscreen></iframe>

Yeah, that's it! Later :)