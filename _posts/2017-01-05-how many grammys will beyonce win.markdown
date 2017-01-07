---
layout: post
title: how many grammys will Beyonce win?
date: 2017-01-05
---
# how many grammy awards will Beyonce win?

Beyonce is nominated for 9 Grammy awards in 2017.  How many will she win?  __TL;DR: 5.  More, below.__

Adapting a chapter of [ThinkBayes](https://github.com/AllenDowney/ThinkBayes) by Allen Downey, I apply Bayesian statistical methods to estimate how many Grammy's will adorn Beyonce's mantle on Feb 13.

I first looked at the distribution of awards/nomination for artists winning Record of the Year over approximately the last twenty years.  For simplicity I take this as a Gaussian distribution with a mean of 0.404 and stdev of 0.156.  ![figure 1](https://raw.githubusercontent.com/ajtrexler/rando/master/grammy_fig1.png)

I used these parameters to create a Gaussian prior distribution.  I discretize this for 10 values of award/nom to create 10 hypotheses for how winning Beyonce is.  #howwinning is a new hashtag I just created. For the Likelihood function, I model the process using a binomial distribution to calculate the probability of getting k awards from n nominations given a hypothetical probability of success.  I evaluate this for each hypothesis generated in the prior over a dataset comprising Beyonce's win record over the last 15 Grammy Awards.  Using the code built into the thinkbayes.py, this readily generates a posterior probability.  Shown below is the prior and posterior, showing that the data from Beyonce's career does indicate she has better-than-average ability to win Grammy's.

![figure 2]( https://raw.githubusercontent.com/ajtrexler/rando/master/grammy_fig2.png )

Beyonce, awards/nom posterior distribution, binomial model:  
mean= 0.456  
max likelihood= 0.439  
credible interval (90%)= 0.23 to 0.65  

The spread in the credible interval shows there's still a great deal of uncertainty in the model.

A large part of this may be that there is a problem in the model, which is that it assumes that each grammy win is a independent event, which it is unlikely to be.  In fact one could argue that since all the awards are based on the same body of excellent work Beyonce produced in 2016, that if one nomination passes an award threshold then others are __more__ likely to be awarded.  I'm not yet cetain how to model this, or whether Bayesian statistics are a good way to approach it.  We may yet get there in ThinkBayes!

For the sake of the interweb's I'll guess 5, one more than the maximum likelihood of my model given the non-independent behavior likely in the awarding process.

[Here's the code](https://github.com/ajtrexler/rando/blob/master/bayes_beyonce.py), which draws very heavily on the great resource by Allen Downey, ThinkBayes.
