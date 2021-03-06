---
toc: false
comments: true
layout: post
description: My experience with the Titanic Competition on Kaggle.
categories: [markdown]
title: The Titanic Competition
---

# The Titanic Competition

The titanic competition on Kaggle is one of the most popular starting point for many data scientists to tinker, explore, and apply what they have learned in a somewhat real context (that claim is merely an educated guess). I created an account on Kaggle and went ahead to look at the competition. I realized that there may be more to it than just applying what I had learned on the fastai course. 

I did the next most natural thing, which is to learn how data science is done on Kaggle! I explored the learning resources and courses on there and found that most of what I had learned through the fastai course (which I wasn't yet done with anyway) was helpful, however I hadn't reached the chapter on tabular data! I decided to go ahead and try out the machine learning courses, both the introduction and the intermediate courses.

It was challenging.

I understood most of what was written to a large extent, but I had no idea about most of the concepts related to tabular data classification (more on the classification issue later!). I went ahead anyway and did my best to put a plan and solve the Titanic competition and submit a prediction to get an initial score. It did not go as I expected. 

The first concept that confused me was the filling of missing data. Here I was thinking to myself, why should I make up information or guess information that wasn't there! However, of course, after much reading I have found that working with guessed data is better than working with no data so the odds of getting a working model based on guessed data was actually legit and was actually standard in real world applications! 

The next problem I faced was putting together a prediction workflow that worked. I applied what I had learned in the courses and was happy when the mean square error reported 0.2. I thought to myself, this is a good start, let me submit and see what score I get. 

To my dismay and disappointment, my score was 0.00000 (as if one 0 wasn't enough). I was so shocked, disappointed, and surprised that all the hours I had put into cleaning and arranging the data was not working out for me. I tried several times to edit the features, the model settings, the optimizer, but to no avail. Each attempt was failure after failure. I kept getting a zero score even after about 4 or 5 submissions.

When I looked at my prediction results on the test data I found that the results were displayed as floats. So I thought, isn't the survived data either a true/false or 0/1 and not an approximation of survival? I tried casting the results to integer but still, I was getting nowhere, and I switched my architecture from XGboost to a RandomForest, but still it wasn't working, I kept on getting floating point predictions. 

After much research into the issue, it turns out that RandomForrest has a regression and classification architecture, and I was using the regression mode which produced floating points instead of integers. After much further editing, and weeks since I had begun working on the competition I finally managed to submit and receive a score of 0.7, which wasn't bad at all in my opinion, I was still in the low-scoring end but at least I managed to get it up from 0 which is an accomplishment in itself.

I do plan on working more on it and at least get a score in the 0.80s or 0.90s but we shall see! The experience has so far been a success and I believe the persistence to learn and get better always yields positive results.   