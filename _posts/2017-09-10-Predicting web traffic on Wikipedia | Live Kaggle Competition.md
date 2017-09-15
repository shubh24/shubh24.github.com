---
layout: post
section-type: post
title: Predicting web traffic on Wikipedia | Live Kaggle Competition!
category: math
tags: [ 'kaggle', 'data science', 'report' ]
---

<!-- <pic>
 -->
This is a documentation of my take on the [WTF Competition](https://www.kaggle.com/c/web-traffic-time-series-forecasting/) on Kaggle, well its short for Web Traffic Forecasting! A month of erratic pipeline building, some frustrated weekends, 40 commits and 22 submissions later, i'm still not where i'd hoped for. Learnt quite a lot though, and this report is an attempt at organizing the learnings. 

*That being said, a warning -- This blog is gonna be slightly technical :)*

This is a live competition, hosted on Kaggle and posted by Google -- The web traffic on 145K Wikipedia page is to be predicted for the period of Sept to Nov 2017, which implies, the accuracy of our submissions will be calculated in real-time -- depending on how the future plays out! The training data consisted of day-by-day view counts on the wiki pages, for the past two years. 

Sounds like a pretty standard time-series problem, right? Couldn't be more wrong!

**My Approach**

Having an xgboost-oriented strategy at the back of my head doesn't always work well, this competition put me out of my comfort zone! Naturally, i looked up the discussions/kernels on how the ARIMA models were performing -- Apparently, auto-regressive models don't generalize well to unknown ranges of the target variable(which is a very possible scenario in our problem). 

A couple approaches stood out:
 - Modelling the time-series problem as a regression problem, every page-date pair being treated as a row.
 - Using Prophet by Facebook, their new forecasting tool.

Upon the advice of some top kagglers, i decided to take up the regression model -- Melt the time-series based dataframe into 
a traditional *page-date-features per row* dataframe. Run an xgb, and predict on a similarly melted test dataframe.

**Feature Engineering**

*Overall Mean/Median* -- A simple constant submission with the mean/median over the last 8 weeks turned out pretty tough to beat in Stage 1. Included them as features too. 

*Rolling means and rolling medians* -- These were some of the most obvious features that came to my head, however they weren't as simple to implement. Agreed, the rolling mean of the last 7 days would be an important feature while predicting today's traffic, but the challenge is asking us to predict the traffic data for the next three months. 

How'll you find the weekly rolling mean of 1st November, when the current date is 14th of September?

Thus, features like rolling mean performed really well in validation but not on the public leaderboard. Finally, i went ahead with rolling means and medians of the last 30 and 60 days. For dates where i couldn't calculate these features, i went ahead with the proxy of the last available calculated feature in the time series.

Later on, i included more features like rolling standard dev, rolling min/max etc.

*Weekday-based mean/median* -- These features turned out to be one of the most important ones! Well obviously, a lot of Wikipedia clicks are weekday/weekend-dependent -- i tried to capture that by taking the rolling weekday-aggregated mean and median over the last six months. 

*Language and Source* -- I tried incorporating statistics derived from the language of the page, or the source(Crawler, Spider etc), but those didn't get me a boost on a vanilla xgboost. Dropped them for the sake of simplicity. 

**Last day's visits** -- Features like the **last day's visits** were incredibly useful while doing a validation run. Not so with the testing data, because of the live nature of the competition. I have to submit predictions for all pages over the next two months -- Clearly, using last day's visits is stupid!

**Pipelining**


After a lot of reading up on the kernels and discussion forums, i stuck with the strategy of many top kagglers: 
 
 - Train One Xgboost model on all pages. This will help us identify a general trend over all of Wikipedia. 
 - Test the model on all future dates of the web-pages.

An alternative was to train an xgboost on every page separately, personalizing the algorithm. This is very time-consuming, and might not generalize well. 

*The Model**

**Challenges & Mistakes**
 - RAM, taking subsets
 - Rolling stats not found -- NAN?
 - Debugging was such a pain!
 - Shallow/deep copy 

**Learnings & Conclusions**

