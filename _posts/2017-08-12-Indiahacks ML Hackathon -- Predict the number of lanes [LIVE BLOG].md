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