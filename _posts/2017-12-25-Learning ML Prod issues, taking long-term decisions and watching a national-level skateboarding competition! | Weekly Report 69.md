---
layout: post
section-type: post
title: Learning ML Prod issues, taking long-term decisions and watching a national-level skateboarding competition | Weekly Report 69
category: report
tags: [ 'data science', 'myntra', 'kaggle', 'vlog', 'fitness', 'skateboarding' ]
---

My weekly report from the 18th of December to the 24th of December -- another strong week, felt focussed. 

Went a little deep in figuring out goals for the not-so-near-future. One thing that i've noticed about myself is that i tend to while away and procrastinate when a goal isn't set. Once i have the tunnel vision mappend in my head, i can go all in, pushing from all directions. That's what i'm gonna do, come 2018. I guess i like the feeling of chasing something, gives me purpose.

At work, i've been working on some experiments to finalize modelling details -- whether to have a rolling model that runs everyday or would a static model work well enough. Whether we should have a buffer period while taking training data(since our target variable is a lagged metric). We have reached reasonable conclusions after running a couple experiments, the plan of action became a little clearer after a status meet. 

I was intrigued by the concept of having different class ratios in the training and testing set(if we don't consider the buffer period), and whether that would affect my model's performance. Went through many blogs and some papers, couldn't come down to a strong conclusion in my head. We also figured that AUC might be a better metric for our problem rather than logloss, given we are to optimize the recall at a minimum agreeable precision value. This gave rise to a new confusion in my head -- how would we give class weights(scale_pos_weight in xgboost) when the objective metric is AUC! I'm worried about class imbalance, might have to dig deeper. Good problems to have :)

I'm gonna start working on the famous kaggle 'Christmas' competition for the next couple of weeks -- its a nice little optimization problem on pleasing both the kids and Santa, given a list of preferences of gifts from both sides. Will be fun getting back to kaggling, will help me get going with my 2018 goal!

This week, i put out my Cubbon-bookhouse vlog on Youtube. i was a little apprehensive of mixing the themes in my edit, got good positive feedback though :) Have a bunch of vlog ideas lined up, stay tuned!

<iframe width="560" height="315" src="https://www.youtube.com/embed/bDbI1ZeJVGI" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

It wasn't a good reading week, i've only managed to get through 25% of Outliers, and 4 chapters of Tribe of Mentors. Gotta hit the pedal.

On a roll on run/workout goals, hitting all of them consistently! Went for a couple squash and skate sessions too, even bought a brand new skateboard from Decathlon. Its so much more fun, skateboarding might be the closest thing to actual flying :p

I attended an awesome skateboarding competition in Play Arena, Jugaad 2017! Spent 6-7 hours just watching the pros go at their tricks, fall and then stand back up, cheering each other, it was a sporting treat. I was left super-inspired, there were 12 year old boys kicking ass on the boards, giving me goosebumps as they landed kickflips and nollies so nonchalantly. There was a different sense of camraderie within the competitors, something i haven't seen in other sports -- its special to see your opponent applauding you on your trick just before going in on his, rare to see in tennis too. I could see there was an insane amount of practice the pros had put in, and there was always that desire to improve, to hit that trick. Reminds me of the platitude Casey always shares, 
	
	*"With every success, comes a bigger and more ambitious goal. You never arrive."*

There is no finish line.
