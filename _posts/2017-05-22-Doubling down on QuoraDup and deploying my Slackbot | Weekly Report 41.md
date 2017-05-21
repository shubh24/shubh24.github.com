---
layout: post
section-type: post
title: Doubling down on QuoraDup and deploying my Slackbot | Weekly Report 41
category: report
tags: [ 'kaggle', 'data science', 'slackbot' ]
---

My weekly report from the 15th of May to the 21st of May -- weeks are literally flying by at this moment ;) Can't seem to recollect this week's exploits, probably a case of recency bias.

A poster on one of the walls in Belong says -- "Prioritize ruthlessly & Double Down on what's working!". Trying to do just that in the Quora challenge on Kaggle, i had been building nlp-based features for a while(without submitting). This week, i built out a testing framework(had to split the test data into parts because of its size!) and climbed about a 1000 places on the leaderboard. 

Another "data leak" was released by kagglers, which i'll be testing out soon -- it's based on the network effects of the questions on Quora, basically the intersection of neighbor(related) questions. I have some other network(graph)-based features in mind, but most overfit because of the introduction of the target variable -- This has been a major learning for me. Always disregard the target when feature engineering. I read up on the Word2Vec models but implementing Keras has been on the to-do list for a while now. The initial curve is haunting me again, gotta take it head-on. 

At work, i implemented a Celery+Redis framework to make my slackbot asynchronous -- Had some issues with postgres connections initially but figured it out eventually. Got the basic 0.1 version deployed and working, also demo-ed it to the company. Some more details need to be fine-tuned, will ship it soon :) The concept of such a bot has inspired us to take upon a difficult task -- generating dynamic Call-to-Actions for CSMs based on product usage & targets. There might be a hundred metrics that we might track, but which 5 matter the most and require the CSM's attention -- Very important to tackle this as we scale!

On the personal learning front, it's been slow -- Have to make plans to learn DL and Spark. Casey Neistat has inspired me to start a book review blog, -- i'll try and finish a book within a month and push out a review blog. Have already begun seeing dividends as i rush up on the chapters :)

Went for my first 2k run in a more than two months, felt pretty strong. The September half-marathon looks iffy still, but will give it the best shot! Workouts are also running along smoothly, need to sneak quite a lot within the rest of the month. 

So yeah, cya!