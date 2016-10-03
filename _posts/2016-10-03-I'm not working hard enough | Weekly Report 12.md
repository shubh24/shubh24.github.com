---
layout: post
section-type: post
title: "I'm not working hard enough | Weekly Report 12"
category: report
tags: [ 'pilani', 'data science', 'delhi' ]
---

My weekly report - from the 26th of September to the 2nd of October. In terms of productivity, this week was bad, and I didn't even try working hard on the Datahack competition when things got stuck :(

I'd been working on a Regression Problem, regarding predicting the footfall in parks, given various environmental variables. My standard approach to such problems is to visualize the various variables with the target variable, and to extract some basic features like "weekday" from the timestamp, or "mean footfall per month" or "date-month" pair(the same date may be a holiday every year!). Then, I try modelling some of the predictive algorithms like Random Forests, XGBoost and CNNs. Since the Redhat competition, I've become loyal to H2O's package in R -- I can have upto 1000 levels in a factor variable while building a random forest! What on Earth! My local RAM supports just 52 -- the difference! 

My process in this competition was similar, and I ranked well in the first 2-3 days but by the end of the competition I slipped to 77 on the Public Leaderboard. The extra variables I used were "weekday", "footfall_ave_by_park_id", "atmospheric_ave_by_park_id", "moisture_ave_by_park_id", "footfall_ave_by_month", "date_month" etc. -- but except "date_month", no variable was giving me a considerable jump on the Leaderboard. I trained a 200-tree Random Forest, with "max depth" set as 50, which is complex enough! The good thing with RFs is that it is pretty tough to overfit(bagging models + randomness at two levels) , and there are far fewer hyperparameters to tune. XGBoost does offer a better performance, but I still have to learn the art of tuning the parameters. I tried coming up with better features over the week, but none of them were giving me a good enough delta. I think the trouble was that I was doing a mean imputation over the whole dataframe, and I didn't explore the dataset well enough. 

Now that I'm reading up on winners' solutions, I realize that a lot more importance needs to be given to understanding the dataset. My approach is still very beginner-like and I'm not writing standard R code, just making it work isn't good enough. Understanding the winners' solutions will give me a better idea into their approaches and help me in further challenges -- [@anokas](https://www.kaggle.com/anokas) and [@srk](https://www.kaggle.com/sudalairajkumar) look unreachable with their standards, but I'll get there! One day I will.

I also made a 22-hour trip to Delhi, to watch "M.S.Dhoni--The Untold Story" and picking up on some trekking gear. I'm planning on trekking the Annapurna Base Camp in Nepal next week! Will be a 10-12 day trip, hopefully it becomes a reality -- We've been planning the Nepal trip far too long. A pre-trip video will be out soon!

Dhoni's movie was good, but I may be biased with my fanboyism towards MSD.

Me and a couple friends made a "Shikanji Review Video" visiting all "redis" on our campus. Shikanji is basically lemonade without salt! Do have a look!

<iframe width="640" height="360" src="https://www.youtube.com/embed/DHd67FtmkdE" frameborder="0" allowfullscreen></iframe>