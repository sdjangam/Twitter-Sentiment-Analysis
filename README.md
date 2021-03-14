# Twitter-Sentiment-Analysis-Project

# Abstract
The blast of Web 2.0 has prompted expanded action in Podcasting, Blogging, Tagging, Contributing to RSS, Social Bookmarking, and Social Networking. 
Subsequently there has been a sudden increase of enthusiasm for individuals to mine these tremendous assets of information for suppositions. Sentiment analysis or Opinion Mining is mining of sentiment polarities from online social media. 
In this project we will talk about a procedure which permits use and understanding of twitter information for sentiment analysis. 
We perform several steps of text pre-processing, and then experiment with multiple classification mechanisms. 
Using a dataset of 50000 tweets and TFIDF features, we comparison the accuracy obtained using various classifiers for this task. 
We find that linear SVMs provide us the best accuracy results among the various classifiers tried. 
Sentiment analysis classifier could be useful for many applications like market analysis of different features of a new product or public opinion for a new movie or speech by a political candidate.

# Introduction

Sentiment analysis (SA), also known as opinion mining is the process of classifying the emotion conveyed by a text, for example as negative, positive or neutral.
Also called as Opinion extraction, Opinion mining, Sentiment mining, Subjectivity analysis
Applications
Movie:  is this review positive or negative?
Products: what do people think about the new iPhone?
Public sentiment: how is consumer confidence? Is despair increasing?
Politics: what do people think about this candidate or issue?
Prediction: predict election outcomes or market trends from sentiment.

# Large data for sentiment analysis on Twitter

A popular social medium is Twitter, a micro-blogging site that allows users to write textual entries of up to 140 characters, commonly referred to as tweets.
As of June 2015, Twitter has over 302 million monthly active users according to their homepage, whereof approximately 88 % have their tweets freely readable. 
Data created by Twitter is made available through Twitter’s API, and represents a realtime information stream of opinionated data.

# Challenges in handling Twitter data

Tweets often contain misspellings, and the constrictive limit of 140 characters encourages slang and abbreviations. 
Unconventional linguistic means are also used, such as capitalization or elongation of words to show emphasis. 
Additionally, tweets contain special features like emoticons and hashtags that may have an analytical value. 
Hashtags are labels used for search and categorization, and are included in the text prepended by a “#”. 
Emoticons are expressions of emotion, and can either be written as a string of characters e.g., “:-)”, or as a unicode symbol. 
Finally, if a tweet is a reply or is directed to another Twitter user, mentions can be used by prepending a username with “@”.


# Problem Definition

Given: Tweet
Predict: Sentiment polarity of the tweet – positive vs negative.

# Basic ML and NLP techniques and tools needed for Twitter Sentiment Analysis

# Approaches: Machine Learning (Decision Trees)

![image](https://user-images.githubusercontent.com/67232573/111080341-0f7b7c80-8524-11eb-98f1-0ab48442a434.png)


![image](https://user-images.githubusercontent.com/67232573/111080364-2b7f1e00-8524-11eb-8b18-af0f03005ce5.png)


Predict whether a person will cheat or not?


# Approaches: Machine Learning (KNNs)

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


# Approaches: Machine Learning (SVMs)

![image](https://user-images.githubusercontent.com/67232573/111080445-86b11080-8524-11eb-9574-32247c1144d1.png)


SVM searches for the hyperplane with the largest margin, i.e., maximum marginal hyperplane (MMH) using constrained convex quadratic optimization
Pros: 1. High accuracy 2. Nice theoretical guarantees regarding overfitting 3. With an appropriate kernel they can work well even if your data is not linearly separable in the base feature space 4. Good for high-dimensional data (like text)
Cons: 1. Memory-intensive 2. Hard to interpret 3. Annoying to run and tune (long training time) 4. Not easy to incorporate domain knowledge (priors)
Kernel Trick.

# Approaches: Machine Learning (Ensemble Learning)

Use a combination of models to increase accuracy
Popular ensemble methods
Bagging: averaging the prediction over a collection of classifiers
Boosting: weighted vote with a collection of iteratively learned classifiers
AdaBoost
Gradient Boosting
Random Forest: Each classifier in the ensemble is a decision tree classifier and is generated using a random selection of attributes at each node to determine the split
Pros: Highly effective in presence of large amount of training data
Cons: Take long time to train.

# Approaches: Machine Learning (Logistic Regression)

![image](https://user-images.githubusercontent.com/67232573/111080613-44d49a00-8525-11eb-8275-c1fdd8bcac09.png)


# Approaches: Machine Learning (Naïve Bayes)

![image](https://user-images.githubusercontent.com/67232573/111080651-72214800-8525-11eb-8588-f68da73686dd.png)

# Approaches: NLP (TF-IDF)

Term frequency-inverse document frequency (TF-IDF) is a common term weighting scheme for the bag-of-words model, which lets us identify words in a collection of documents that can guide in deciding a document’s topic. 

![image](https://user-images.githubusercontent.com/67232573/111080681-9e3cc900-8525-11eb-89cb-2a978d2c0831.png)


![image](https://user-images.githubusercontent.com/67232573/111080687-a6950400-8525-11eb-8280-ee9042370538.png)

Here D is the entire corpus of documents, and N is the total number of documents in the corpus. As the number of documents where a term appears increases, the ratio inside the logarithm will decrease towards 1, making the idf approach 0.




