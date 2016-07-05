---
layout: post
title: "Can you beat Federer?!"
description: "A Statistical Approach"
category: Math
tags: [fivethirtyeight, puzzle, tennis]
---
{% include JB/setup %}

This weekend, I came across a puzzle on FiveThirtyEight - [Can you figure out How to Beat Roger Federer at Wimbledon?](http://fivethirtyeight.com/features/can-you-figure-out-how-to-beat-roger-federer-at-wimbledon/)! I just had to dive in! Now this challenge had Monday morning as a deadline, so I decided to pull an all-nighter(gave up by 5 in the morning -_-)! Little did I know, it took me 2 more days to completely understand the problem. 

![Federer](/images/federer.jpg)

So, the problem states that I'm playing Federer, in his prime in the Wimbledon Championship Finals, and I have the liberty to start the match at any score of my choice. I have a 1% chance of winning a point against Federer. I have to decide which point should I start the match and what would be the probability of me winning the match. 

Now, at first glance, the answer is Match Point, two sets to love... but I have to prove it mathematically/computationally.

My initial approach was to code the tennis match and then iterate over the possible scores to evaluate the best score and probability. I decided to use Wimbledon 2008 Finals statistics to get the serve points and receiving points statistics, thanks to [Tennis Abstract](http://www.tennisabstract.com/cgi-bin/player.cgi?p=RogerFederer&f=A2008qqB2E0). When I was through with coding a tennis match simulation of sorts, I hit a dead end. And then hit the realization that I should have done a little research on this.

I came across an excellent research paper, [Forecasting the winner of a tennis match](http://cdata4.uvt.nl/websitefiles/magnus/paper64.pdf), which highlighted the key areas I needed to concentrate on. Ideally, this is not a simulation problem, rather one from Combinatrics. To win a game, I need to win 4 points -- so the probability can be easily calculated. 

![Equation](/images/eqn.png)
Here p is the probability of me winning a point against Federer, assumed to be 0.01.

Thus, the probability to win a set and therefore, a match can similarly be calculated. However, as described in the question, we need to decide the starting score, thus the scores need to be iterated over. 

Post calculation, I could easily see that starting from 2 sets all, 5-0, 40-0 will give me the highest probability to win the match. The calculation can be verified in this [script](https://github.com/shubh24/beat-federer/blob/master/prob.py). The exact value of me winning the third set (from 2-0, 5-0, 40-0) is 0.0100010366568. Considering that I lose that set, there is absolutely no question of coming back -- chances of me winning a new set from Federer are 2.35304918031e-39. Awesome!

I wrote a small script to analyze how the probability of winning a point affects the probability of winning a game, set or match. 

![Prob](/images/prob1.jpg)
`How the chances of a player winning changes with the chances of his winning a point`

Having started work on simulating the match, I decided to verify my results with a measured simulation. So, I'm keeping Federer at - Zero Sets, Zero Games, Zero Points, while I vary my score over the first three sets. For each score, I'm testing over Ten Thousand iterations to have a big enough sample. In the simulation, I've calculated different probabilities for my service and return games - based on Federer's statistics from the ['08 final](https://www.youtube.com/watch?v=-1yfWb0-jqQ). For each iteration, I pick a random number and if it's greater than 0.99(plus minus the service/return factor), I win a point, and thus the match progresses.

![Score](/images/score1.jpg)
`How I'm winning over different starting scores`

Clearly the graph shoots up at Match Point, two sets up -- indicating that I'll win the match 140 times out of the 10K trials. This result is very much in accordance with the probability approach that I'd shown above. The script for the simulation can be found [here](https://github.com/shubh24/beat-federer/blob/master/simulate.py).

Yeah, so that's pretty much it! Waiting for the results to be announced by FiveThirtyEight!

Find the Github repository [here](github.com/shubh24/beat-federer).  

Sources

1. [The Problem!](fivethirtyeight.com/features/can-you-figure-out-how-to-beat-roger-federer-at-wimbledon/)
2. [Data - Tennis Abstract](http://www.tennisabstract.com/blog/category/win-probability/)
3. [Research Paper -- Forecasting the winner of a tennis match](http://cdata4.uvt.nl/websitefiles/magnus/paper64.pdf)





