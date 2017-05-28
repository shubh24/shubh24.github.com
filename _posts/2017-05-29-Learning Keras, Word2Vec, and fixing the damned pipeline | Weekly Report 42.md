---
layout: post
section-type: post
title: Learning Keras, Word2Vec, and fixing the damned pipeline | Weekly Report 42
category: report
tags: [ 'kaggle', 'data science', ]
---

My weekly report from the 22nd of May to the 28th of May -- climbed up on the Leaderboard, still a long way to go! Also, 42nd Weekly Report - calls for a celebration eh!

Let's jump straight into QuoraDup -- after a couple of days of pulling my hair, i finally fixed the pipeline. I haven't done a root cause analysis of the issue, but a restart with a new ipynb saved the day, and my sanity. The new magic features, namely the neighbor intersection count, and my own features like degree of separation and second degree neighbors has put me in the Top 15-20% range. 

I also went into the sent2vec features(vector similarities) with the w2v embeddings, but those didn't give a lot of gain. Also tried getting a keras lstm to run with the word2vec embeddings, but my ram just ain't good enough :( Understanding Keras and its layers was a good learning curve though! I'm currently working on extracting some insights from the QID and the temporal features, just made a terrible linear regression model. Will look into it tomorrow!

With the end to the competition approaching, new features are being released -- weighted graph and a pagerank model are on the to-do list already! A Top 10% position might be realistic :) 

At work, i've been expanding on building an insights model -- currently analysing the search string patterns. Which parameters in a string gave the best output, and whether the search strings can be recommended to similar jobs. I'll also be learning spark to implement a real-time alerting system for the Customer Success teams, excited!

Went for a 3k run this weekend, the recovery is strong! I'm starting a Half-Marathon plan on Nike from this week -- 16 weeks to race day! Also went for a sunday cubbon park trip, boy that place is beautiful!

That's it folks. Later!