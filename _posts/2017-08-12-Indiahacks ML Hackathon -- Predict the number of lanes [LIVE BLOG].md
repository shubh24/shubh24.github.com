	---
layout: post
section-type: post
title: Indiahacks ML Hackathon -- Predict the number of lanes [LIVE BLOG]
category: report
tags: [ 'data science', 'machine learning', 'hackathon' ]
---

Welcome to my live blog -- My attempts at cracking into the Indiahacks ML hackathon. This is the second round(zonals), and there are around 50 of us participating across India, only 15 will qualify for the finals. An exciting 20 hours to follow :)

**August 12, 13:56** Almost an hour into the hackathon, i've had a brief look at the dataset, i have a rough idea of whats to follow. The problem is around predicting the number of road lanes, basis satellite data of lane lines, coordinates etc. Will dive into exploration for the next couple of hours, but first i'll catch up on some lunch ;)

**August 12, 16:32** Check-in #2 -- Having understood the construct of the problem, and looked at various correlations between features, i'm now down to building some basic features. I submitted a couple solutions based on a very simple heuristic -- minimum and maximum of the number of lane lines recorded(subtract that by 1) for every road. Didn't score anywhere close to good, but it let me get a hang of the problem.

Learning:The evaluation criteria is F1-score for every value of number of roads, not the regular rmse used for regression based problems.