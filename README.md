# Twitter-Sentiment-Analysis-Project

# Abstract
The blast of Web 2.0 has prompted expanded action in Podcasting, Blogging, Tagging, Contributing to RSS, Social Bookmarking, and Social Networking. 
Subsequently there has been a sudden increase of enthusiasm for individuals to mine these tremendous assets of information for suppositions. Sentiment analysis or Opinion Mining is mining of sentiment polarities from online social media. 
In this project we will talk about a procedure which permits use and understanding of twitter information for sentiment analysis. 
We perform several steps of text pre-processing, and then experiment with multiple classification mechanisms. 
Using a dataset of 50000 tweets and TFIDF features, we comparison the accuracy obtained using various classifiers for this task. 
We find that linear SVMs provide us the best accuracy results among the various classifiers tried. 
Sentiment analysis classifier could be useful for many applications like market analysis of different features of a new product or public opinion for a new movie or speech by a political candidate![image](https://user-images.githubusercontent.com/67232573/111080203-62a0ff80-8523-11eb-81aa-75fbe61db9a3.png)

# Introduction

Sentiment analysis (SA), also known as opinion mining is the process of classifying the emotion conveyed by a text, for example as negative, positive or neutral.
Also called as Opinion extraction, Opinion mining, Sentiment mining, Subjectivity analysis
Applications
Movie:  is this review positive or negative?
Products: what do people think about the new iPhone?
Public sentiment: how is consumer confidence? Is despair increasing?
Politics: what do people think about this candidate or issue?
Prediction: predict election outcomes or market trends from sentiment
![image](https://user-images.githubusercontent.com/67232573/111080230-86fcdc00-8523-11eb-8868-8127d55510bb.png)


# Large data for sentiment analysis on Twitter![image](https://user-images.githubusercontent.com/67232573/111080242-967c2500-8523-11eb-9364-23941bedca84.png)

A popular social medium is Twitter, a micro-blogging site that allows users to write textual entries of up to 140 characters, commonly referred to as tweets.
As of June 2015, Twitter has over 302 million monthly active users according to their homepage, whereof approximately 88 % have their tweets freely readable. 
Data created by Twitter is made available through Twitter’s API, and represents a realtime information stream of opinionated data.
![image](https://user-images.githubusercontent.com/67232573/111080253-a4ca4100-8523-11eb-9d7c-f3efbc31a3f3.png)

# Challenges in handling Twitter data![image](https://user-images.githubusercontent.com/67232573/111080269-b7447a80-8523-11eb-9c50-40d5f37708ef.png)

Tweets often contain misspellings, and the constrictive limit of 140 characters encourages slang and abbreviations. 
Unconventional linguistic means are also used, such as capitalization or elongation of words to show emphasis. 
Additionally, tweets contain special features like emoticons and hashtags that may have an analytical value. 
Hashtags are labels used for search and categorization, and are included in the text prepended by a “#”. 
Emoticons are expressions of emotion, and can either be written as a string of characters e.g., “:-)”, or as a unicode symbol. 
Finally, if a tweet is a reply or is directed to another Twitter user, mentions can be used by prepending a username with “@”.

![image](https://user-images.githubusercontent.com/67232573/111080283-c0354c00-8523-11eb-87e9-4afcb621e8f0.png)

# Problem Definition![image](https://user-images.githubusercontent.com/67232573/111080298-d2af8580-8523-11eb-8cb5-8598d8fa7b47.png)

Given: Tweet
Predict: Sentiment polarity of the tweet – positive vs negative.
![image](https://user-images.githubusercontent.com/67232573/111080305-df33de00-8523-11eb-87d2-7342e3e7701a.png)

# Basic ML and NLP techniques and tools needed for Twitter Sentiment Analysis![image](https://user-images.githubusercontent.com/67232573/111080319-f4a90800-8523-11eb-91da-f5f8fdd9078e.png)

# Approaches: Machine Learning (Decision Trees)![image](https://user-images.githubusercontent.com/67232573/111080334-05597e00-8524-11eb-8fc7-bdd2f011fb90.png)

![image](https://user-images.githubusercontent.com/67232573/111080341-0f7b7c80-8524-11eb-98f1-0ab48442a434.png)


![image](https://user-images.githubusercontent.com/67232573/111080364-2b7f1e00-8524-11eb-8b18-af0f03005ce5.png)


Predict whether a person will cheat or not?
![image](https://user-images.githubusercontent.com/67232573/111080381-3c2f9400-8524-11eb-8e34-4a640fd7b611.png)


# Approaches: Machine Learning (KNNs)![image](https://user-images.githubusercontent.com/67232573/111080397-49e51980-8524-11eb-8ff1-374449c94609.png)

![image](https://user-images.githubusercontent.com/67232573/111080404-51a4be00-8524-11eb-9ece-446e6081ea4e.png)


Pros:
Simple process
Quick to train
Cons
Curse of dimensionality 
Slow to test
Requires more memory
Missing values need to be handled separately
![image](https://user-images.githubusercontent.com/67232573/111080421-6aad6f00-8524-11eb-946d-c855d2831e31.png)


# Approaches: Machine Learning (SVMs)![image](https://user-images.githubusercontent.com/67232573/111080441-7c8f1200-8524-11eb-99e6-f66fbbd30af9.png)

![image](https://user-images.githubusercontent.com/67232573/111080445-86b11080-8524-11eb-9574-32247c1144d1.png)


SVM searches for the hyperplane with the largest margin, i.e., maximum marginal hyperplane (MMH) using constrained convex quadratic optimization
Pros: 1. High accuracy 2. Nice theoretical guarantees regarding overfitting 3. With an appropriate kernel they can work well even if your data is not linearly separable in the base feature space 4. Good for high-dimensional data (like text)
Cons: 1. Memory-intensive 2. Hard to interpret 3. Annoying to run and tune (long training time) 4. Not easy to incorporate domain knowledge (priors)
Kernel Trick
![image](https://user-images.githubusercontent.com/67232573/111080455-93cdff80-8524-11eb-9027-9fddf0b96190.png)


# Approaches: Machine Learning (Ensemble Learning)![image](https://user-images.githubusercontent.com/67232573/111080472-a34d4880-8524-11eb-9493-415ffb24e8f3.png)




