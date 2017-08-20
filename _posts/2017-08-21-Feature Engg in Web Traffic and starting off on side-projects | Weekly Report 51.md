---
layout: post
section-type: post
title: Feature Engg in Web Traffic and starting off on side-projects | Weekly Report 51
category: report
tags: [ 'kaggle', 'data science',  ]
---

My weekly report from the 14th of August to the 20th of August -- a decent week on productivity, could've done better. Gotta cut back on the parties and post-8PM distractions. Still scope for improvement, the August goal list won't realize on its own.

I've been putting some decent effort in building the pipeline in the "Web Traffic Forecast" challenge on Kaggle -- a functional pipeline is up! Currently, running a single xgb model for all pages, all dates. I tried a couple approaches on the proxy features for the test dataset -- Using predictions as features for the next date backfired in a rather extraordinary fashion. All predictions apparently converged to a single value after certain dates :( 

For the purpose of this competition, SMAPE is the evaluation metric -- a non-differentiable objective function which is not very ideal for a model like xgboost. However, i learnt plugging in custom objective functions(feval) in the xgb call. I'm currently redoing the test data creation so as to accommodate for rolling statistics on unseen data.

At work, i'm continuing work on the segmented sort problem -- i did a very top-level exploration in a jupyter notebook, and now i'm reading up on biclustering algorithms for clustering high-dim data at a large scale. I feel that productivity at work iscurrently below-par -- i should get into a productive routine, soon! 

I've been thinking of coming up with a side-project or a data blog idea for the past couple day -- i might have stumbled upon a long-term project :) Developing a website to explore UGC/AI-curated rabbit-holes in topics of your interest, when your code is running. Cheesily named as "while-my-code-runs" :)

On the fitness side of things, this week was a relatively low-key one, put in a weekly mileage of 13km -- The silence before the storm. Still haven't gotten around with the NTC workouts -- gotta get in a morning routine. Not cool.

So yeah, kinda struggling a bit with productivity. Got distracted for a couple of days, but i know i'm getting there. Soon.