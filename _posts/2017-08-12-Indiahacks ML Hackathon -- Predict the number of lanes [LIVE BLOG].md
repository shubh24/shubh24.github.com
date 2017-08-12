---
layout: post
section-type: post
title: Indiahacks ML Hackathon [LIVE BLOG]
category: report
tags: [ 'data science', 'machine learning', 'hackathon' ]
---

Welcome to my live blog -- My attempts at cracking into the Indiahacks ML hackathon. This is the second round(zonals), and there are around 50 of us participating across India, only 15 will qualify for the finals. An exciting 20 hours to follow :)

**August 12, 13:56** Almost an hour into the hackathon, i've had a brief look at the dataset, i have a rough idea of whats to follow. The problem is around predicting the number of road lanes, basis satellite data of lane lines, coordinates etc. Will dive into exploration for the next couple of hours, but first i'll catch up on some lunch ;)

**August 12, 16:32** Check-in #2 -- Having understood the construct of the problem, and looked at various correlations between features, i'm now down to building some basic features. I submitted a couple solutions based on a very simple heuristic -- minimum and maximum of the number of lane lines recorded(subtract that by 1) for every road. Didn't score anywhere close to good, but it let me get a hang of the problem.

Learning:The evaluation criteria is F1-score for every value of number of roads, not the regular rmse used for regression based problems.

**August 12, 18:08** Just had a cappucino, some good productivity flowing through the past hour or so. A basic feature-engineering pipeline is ready, raring up my xgboost and its parameters for a submit. 

**August 12, 18:47** Aaaaand we're in the Top 10! A simple xgb with multi-softmax is giving me .7230 F1 score on the leaderboard, a decent start. Currently, i'm using basic features like "Mean Lane length", "Number of unique lanes", "Ratio of lane length to road length" etc. Will be spending more time on feature engineering, probably till midnight. Model ensembling in the dark and lonely night ;)

**August 12, 20:06** It's crazy how simple features can boost your score straight up! Implemented a couple or so transformed features like "Min difference of road length and lane length", "Road aspect ratio" etc have landed me at 4th position. The ranks are shuffling rapidly, its getting intense! But first, gotta focus on a Dominos pizza sitting right beside me ;)

**August 12, 22:06** Haven't made any progress on the leaderboard, am trying to find the patterns behind certain incosistencies in the dataset. Why are there two sets of "Total Lanes" for a single lane entry, haven't been able to figure it out. Attempts at taking only the rows with "more lanes" hasn't worked either. Keeping at it.

Learning: Don't include all features which are negatively correlated to the target variable. You might think they're giving a negative feedback loop to the model, but apparently no! Gotta read more on this.

**August 12, 23:35** I'm testing on my existing feature set, pruning on some of the negatively correlated features. Some of them giving me quite a shock -- lingering around the Top 10 mark currently :(

**August 13, 01:21** New day yay! I've spent the last hour or so, developing features based on the coordinates of roads and lanes. Trying to build a proxy value for number of lanes of roads which are closer in proximity. I didn't realize the stupididy in this method till quite late, the test dataset's roads are pretty much in a disjoint set than those in train, not giving me any substantial advantage. Its okay, gotta keep going.

**August 13, 03:21** Fatigue seems to have set in, i've taken a short power nap and my system seems to be running on biscuits and water. I've slipped to 18th place, although i did bring in some positive features based on minimum geographical distance between lanes. i've been trying to get a GBM model to work, that hasn't given any dividends -- will go ahead with RF or a neural net.

**August 13, 04:21** I would like to believe i've optimized my xgboost hyperparameters over the past hour, manually though. Just the tuning has pushed me up to 9th place. Going for a short nap now, want to be energized for the last stretch :)