---
layout: post
section-type: post
title: Federer Vs Nadal -- Statistically!
category: math
tags: [ 'data science', 'kaggle', 'tennis', 'federer', 'nadal' ]
---

![fedal]({{site.baseurl}}/images/fedal/fedal.jpg)

**Roger Federer Vs Rafael Nadal** is arguably the greatest rivalry in all of sports. With both Roger and Rafa getting older by the day, every Fedal feels like a treat these days! Having witnessed three incredible matchups in 2017 already, these rare sporting events have been super-hyped in media. Even more in my mind ;)

Thanks to Kaggle Datasets, i came across a dataset of all ATP matches from 1968-2016.  - Roger's 1345 matches pitted against Rafa's 1001. I've analyzed both players' performances over the years, on different surfaces, and against each other!

Specifically, we'll look at:

 - Year-over-Year Win %
 - Year-over-Year Seeds
 - Surface sensitivity of both players
 - Favourite/worst Opponent
 - % Straight Set Wins (Dominance of wins) 
 - Serve Analysis
 - Year-over-Year Fedal clashes
 - Fedal on different surfaces
 - Where can Rafa beat Roger?

**YoY Win Percentage**

![win_ratio_yoy]({{site.baseurl}}/images/fedal/win_ratio_yoy.png)

It's kinda funny how the minimum value on y-axis is 40% :) Anyways, it's interesting to note the rise of Rafa was much steeper than Roger, then stagnated till 2014 at around 80-90%. Post 2014, both players have been a little unpredictable, facing upsets in Grand Slams. 

**Players' Seeds over the years**

![seeds_yoy]({{site.baseurl}}/images/fedal/seeds_yoy.png)

These seeds as per the year-end dates(on which the seeds were updated). As expected, Federer maintains No.1 for a long 5-6 years and Nadal trails at No.2, creeping up a couple of times as well.

**Surface Sensitivity**

Now lets look at both players' performance on the different surfaces. King of Clay versus Emperor of Grass!

![rafa_surface_sensitivity]({{site.baseurl}}/images/fedal/rafa_surface_sensitivity.png)

Just look at the red line hovering around the 100% mark -- Mind blown. Interesting note -- the 2014 dip on Grass is because of the first round exit in Wimbledon '14, Steve Darcis the spoilsport! Similar pre-quarters exit in 2014 by Nick Kyrgios.

![roger_surface_sensitivity]({{site.baseurl}}/images/fedal/roger_surface_sensitivity.png)

If you were surprised by Rafa's red line, Roger's green line will leave you numb. At 100% for five straight years('03-'07)! 

**Favourite Tournaments**

Wonder which tournaments both the players have dominated? A look at the top win ratios for different tourneys(at least 10 matches must be played by the player at that tourney).

![roger_tourney]({{site.baseurl}}/images/fedal/roger_tourney.png)

{:.image-caption}
Roger's fav tourneys

![rafa_tourney]({{site.baseurl}}/images/fedal/rafa_tourney.png)

{:.image-caption}
Rafa's fav tourneys

**Tough Opponents**

Who has troubled Roger the most?!

![roger_opponent]({{site.baseurl}}/images/fedal/roger_opponent.png)

{:.image-caption}
Roger's nemeses - Tim Henman was a surprise!

![rafa_opponent]({{site.baseurl}}/images/fedal/rafa_opponent.png)

{:.image-caption}
Rafa's nemeses - Clearly, Rafa doesn't have as many nemeses as Roger does! 

**Dominance on different surfaces**

To analyze the dominance of a win, i've analysed the percentage of straight set wins on the different surfaces.

![dominance]({{site.baseurl}}/images/fedal/fed_rafa_dominance.png)

Except clay, Federer leads Nadal in all surfaces. What is surprising to see is, even though 
Federer is the best on Grass, he is most dominant on Hard Courts.  

**Serve Analysis**

It's known that Federer has an impeccable serve, while Rafa relies more on his groundstrokes. But what about double faults, %points won on second serve and break points saved?!

![radar]({{site.baseurl}}/images/fedal/Rplot.png)

{:.image-caption}
Serve Analysis -- Federer(blue) Vs Nadal(red) 

As visible from the radar charts, Nadal serves far less aces than Federer, though both shoot them up on the grass courts. Perhaps as a result, Nadal puts in fewer double faults on both clay and hard, almost equal on grass. Nadal's overall first serve percentage is also marginally higher than Federer's, though Federer leads in the rest of the metrics(very slightly). 

Note -- the maximum "ace" value on the charts is 10, and maximum "double faults" is 3. The other metrics are percentages(maximum is 100). 

**Fedal - The Rivalry**

Federer-Nadal have played 37 ties, of which Rafa has come out winning 23 of the times. But this stat shouldn't bias us towards Rafael -- First have a look at the Head-to-Head Fedal on different surfaces.              

![h2h_surface]({{site.baseurl}}/images/fedal/h2h_surface.png)

{:.image-caption}
Clearly, they have played a lot more matches on clay, compared to grass -- which gave Rafa the massive lead! 

My hypothesis -- Nadal didn't advance as much on grass to play with Federer, resulting in fewer Fedal clashes on grass. This suggests, Nadal is worse on grass than Federer is on clay. Just a hypothesis though :)

Lets have a look at Fedal clashes over the years, over different surfaces -- 

![fedal_surface]({{site.baseurl}}/images/fedal/fedal_surface_yoy.png)

Now, lets have a look at the upsets (Federer's wins on clay, and Rafa's wins on grass)

![fed_win_upsets]({{site.baseurl}}/images/fedal/fed_win_upsets.png)

{:.image-caption}
Federer's wins on Clay against Nadal -- Not in a Grand Slam though :p

![nadal_win_upsets]({{site.baseurl}}/images/fedal/nadal_win_upsets.png)

{:.image-caption}
Nadal's win on Grass against Fed -- Just one. The Legend. The Epic :)

**Where can Rafa beat Roger in 2017?**

Given the past head-to-heads, Nadal has the best chances to beat Roger on clay. He's beaten him five times in the Roland-Garros finals, thrice in Monte Carlo and twice in Rome. With Federer coming back only in the French Open, that might be the only chance for Rafa this year. 

**Conclusions**

 - Nadal's rise to the top was much steeper than Roger's. Both maintained their positions till 2013, till some major upsets hit them.
 - Nadal on clay has an incredible record -- Greater than 90% win record for a continuous 8 year streak.
 - Federer on grass was even better -- 100% win record for 5 straight years.
 - Federer excels at Dubai, Halle, Wimbledon and US Open  -- Grass and Hard Courts
 - Nadal excels at Roland-Garros, Barcelona, Monte Carlo and Rome -- all clay!
 - Roger had poor win ratios against a few particular players(Nadal, Djokovic, Henman, Murray), while Nadal didn't have many(Davydenko and Djokovic)
 - Nadal is heavily dominant on clay(straight set wins), while Federer is most dominant on hard courts. 
 - Federer serves a lot more aces, while Nadal has a higher percentage of first serves in. Grass courts attract almost double the aces.
 - Nadal leads 23-14 against Federer, of which 13-2 comes from clay!
 - With Federer back in kickass form, the single chance where Nadal can beat him is Roland-Garros finals!


So that's that. Let me know if you liked it! 