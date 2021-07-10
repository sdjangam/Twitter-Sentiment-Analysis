# Twitter-Sentiment-Analysis-Project



the dataset from this link   https://www.kaggle.com/kazanova/sentiment140




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
Application
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

# Tools:Scikit Learn

Scikit-learn is a framework for the Python programming language that offers machine learning models as well as tools for performing preprocessing and data analysis.
Transformer objects are an essential part of performing machine learning with Scikit-learn, and are objects that may “clean, reduce, expand, or generate feature representations”.
Scikit-learn provides a framework for pipelining machine learning tools, making it easy to chain tasks such as preprocessing and feature extraction together with a machine learning algorithm in a tidy manner. 
One of the benefits of using the Pipeline framework is that it allows performing a parameter grid search across all the estimators in the Pipeline.

# Tools:Pandas

Pandas is an open-source library providing high-performance data structures and data analysis tools for the Python programming language. 
It also includes tools for efficiently reading and writing data between in-memory data structures and different textual file formats, such as comma-separated value files.

# Dataset Details

Some people build a program to collect automatically a corpus of tweets based on two classes, “positive” and “negative”, by querying Twitter with two type of emoticons:
Happy emoticons, such as “:)”, “:P”, “:­)” etc. 
Sad emoticons, such as “:(“, “:’(”, “=(“.
Others make their own dataset of tweets my collecting and annotating them manually which very long and fastidious.
Our dataset consists of 1600000 tweets in English coming from two sources: Kaggle and Sentiment140.

![image](https://user-images.githubusercontent.com/67232573/111506520-b6078d80-876f-11eb-937b-fc45d1160f79.png)
![image](https://user-images.githubusercontent.com/67232573/111506560-be5fc880-876f-11eb-825b-bba664ded5ba.png)

# Challenges with Twitter data

The presence of acronyms "bf" or more complicated "APL". Does it means apple ? Apple (the company) ? 
The presence of sequences of repeated characterssuch as "Juuuuuuuuuuuuuuuuussssst", "hmmmm". In general when we repeat several characters in a word, it is to emphasize it, to increase its impact. 
The presence of emoticons, ":O", "T_T", ":¬|" and much more, give insights about user's moods. 
Spelling mistakes and “urban grammar” like "im gunna" or "mi". 
The presence of nouns such as "TV", "New Moon".
Furthermore, we can also add, 
People also indicate their moods, emotions, states, between two such as, *\cries*, *hummin*, *sigh*. 
The negation, “can't”, “cannot”, “don't”, “haven't” that we need to handle like: “I don’t like chocolate”, “like” in this case is negative. 

# Exploratory data analysis

![image](https://user-images.githubusercontent.com/67232573/111506802-067eeb00-8770-11eb-89a5-09146d3c2e50.png)

![image](https://user-images.githubusercontent.com/67232573/111506856-11398000-8770-11eb-8c46-c39e8848eb41.png)

![image](https://user-images.githubusercontent.com/67232573/111506891-1ac2e800-8770-11eb-95e2-de8d31995fd0.png)


# Pre-processing the dataset

Cleaning up the HTML entities, and any other HTML tags
Remove @mentions
Remove URLs from tweets
Convert short forms of negation words to their full forms. 
"isn't":"is not", "aren't":"are not", "wasn't":"was not", "weren't":"were not", "haven't":"have not", "hasn't":"has not", "hadn't":"had not", "won't":"will not", "wouldn't":"would not", "don't":"do not", "doesn't":"does not", "didn't":"did not", "can't":"can not", "couldn't":"could not", "shouldn't":"should not", "mightn't":"might not", "mustn't":"must not”
Decode UTF8 encoded symbols
Replace non-alphabetic characters to spaces.
Ignore words of size 1.
Remove punctuations
Perform word lemmatization

# TF-IDF vectorization, train/test split, cross validation

We start by splitting the data randomly into two parts: train and test. We use 80% data for training and the remaining for testing.
We extract TFIDF features from tweets using TFIDF vectorizer. It converts a collection of raw documents to a matrix of TF-IDF features.
Further, we use these features to learn multiple classifiers. For each type of classifier, we first train the classifier on train data and report the accuracy on test data. We also report cross validation accuracy with 10 folds.
We report confusion matrix and accuracy values for each classifier.

![image](https://user-images.githubusercontent.com/67232573/111507262-7c835200-8770-11eb-97bd-a889db4b1189.png)

# Results

![image](https://user-images.githubusercontent.com/67232573/111507414-a3418880-8770-11eb-8366-b918063fb7f1.png)

We obtain the maximum accuracy using Linear SVM. However, also notice that logistic regression and random forests also lead to similar accuracy values. 
However, simple classifiers like decision trees and nearest neighbors somehow cannot provide good results at all. 
We used default hyper parameter settings for all the classifiers as provided by scikit learn. Tuning those hyper parameters can lead to further accuracy boost and we plan to explore that as part of future work.

# Code and data

The code is contained in the Jupyter notebook: TwitterSentimentAnalysis.ipynb
To be able to run this, you must have Jupyter notebook installed on your machine.
It can be run on any platform: Windows, Linux, Mac-OS
The data is supplied as a csv file: TwitterSentimentAnalysis.csv
Installations needed
Anaconda prompt, Jupyter notebook, numpy, pandas, sklearn, NLTK.

# Conclusion

we discussed the problem of classifying whether a tweet is positive or negative.
We performed classification using TF-IDF features and experimented with multiple classifiers.
We used a Python library, Scikit Learn for building classifiers.
The results show that Linear SVMs work well on our dataset.
The solution can be useful for multiple stake-holders.

# Future Work

We could further improve our classifier 
By trying to extract more features from the tweets, 
By trying different kinds of features, 
By tuning the parameters of the classifiers, or 
We could try logistic regression without any regularization or try say L1 regularization. 
For SVMs, we could try SVMs with various kinds of kernels or also vary the complexity parameter C and see the impact. 
For decision trees, we could try different levels of pruning. 
For random forests, we experimented with 100 trees, but we could vary the number of trees and check its impact on accuracy. 
For nearest neighbors, we used k=5. We could try varying the value of k.
By trying more classifiers like deep learning architectures.



