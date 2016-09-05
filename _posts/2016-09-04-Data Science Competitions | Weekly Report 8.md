---
layout: post
section-type: post
title: "Data Science Competitions | Weekly Report 8"
category: Report
tags: [ 'weekly', 'pilani', 'data science', 'fitness' ]
---

My weekly report - from the 29th of August to the 4th of September. A solid week in terms of productivity and fitness!

Now that I have all the time in the world, I've begun participating in Kaggle and Hackerrank Competitions, related to Machine Learning and Data Science. Have explored the dataset of [Redhat Competition](https://www.kaggle.com/c/predicting-red-hat-business-value/), and made a few preliminary submissions. There are still a couple of weeks left in the competition, and I hope to climb up into the top 10% on the leaderboard! It is an interesting problem in the domain of analyzing business value from each customer's actions on the Redhat Platform.

I spent a majority of the last five days, pushing myself in a week-long [Machine Learning Codesprint](https://www.hackerrank.com/contests/machine-learning-codesprint/) on Hackerrank -- ranked 92nd among 400 odd participants, could have done a lot better! I learnt about [H2O.ai](https://h2o.ai), an awesome tool for predictive analytics which is getting real popular in Kaggle circles. It saves my RAM from the abusive computation it has to do -- build random forests and neural nets on the cloud!

The contest consisted of two problems:
 1. Predicting whether a user will open a certain email from Hackerrank.
 2. Suggesting challenge recommendations for users on Hackerrank.

I did pretty well in the Challenge Recommendation problem (Ranked 38) -- built a hybrid rec. system. To generate similarities between different challenges(for the content-based recommender), I used cosine similarities on the one-hot encoded vectors -- the vectors consisted of the domain/sub-domain, the difficulty level, and the participation count of the particular challenge. I ran a small user-user collabarative filter to get the most similar users and the corresponding challenges in which they participated. Append this to suggestions from the content-based recommender and voila, you have the recommendations! I used R for manipulating the data in the required formats, and python for the number-crunching. This was the first time I'd built a hybrid recommender model -- satisfied with my effort!

The Email Predict challenge had put me in a state of confusion and helplessness, as I was not able to cross a certain score - no matter how many approaches I tried. In the end, I gave up, settling for a rank of 134 -_- I ran neural nets, random forests and ensemble methods and also tried a lot of feature engineering. By means of trial and error, I always came to the conclusion that the new features would lower my score, which was very frustrating. The variables available for the mail-user combo were the the email type, email category, sent time and other metadata. Also available was details of users -- last active time, previous submissions, forum comments, unsubscribed(boolean) -- which I believe would give me user-user similarity. The end result expected was given a mail-user pair, predict whether the mail would be opened. Cross-validated Random Forests, run on H2O gave me an F-Score of 0.436, while the challenge toppers have hit 0.60! I'm really looking forward to studying the approaches of the top scorers and improve my scripts.

You can find my scripts for the contest [here](https://github.com/shubh24/HRCodesprint).

For the past week or so, the Tennis Team has been serious at practice -- our Sports Fest is just ten days away. The fitness sessions have been intense, and it has been a much-needed jolt to me. This will hopefully set the tone for the rest of the semester! Also visited the Birla Museum -- a tick off the psentisem bucket list! 

That's it folks!







