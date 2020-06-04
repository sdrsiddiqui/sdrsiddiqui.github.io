---
title:  Tweeter Sentiments
description:
excerpt:

header:
  overlay_color: "#000"
  categories:
    -

tags:
  - Data Science

---

Sentiment Analysis


Rule based approaches:
we make rules based on vocabularies, features and pattern which you made. We will check the document according to that rules we will determine the polarity or semantic orientation of a document.

We will look at all the words in the text and classify each of them as positive or negative.

If there are more positive words than negative words, we will classify the document as positive.
For classifying each words as positive and negative words, we need a lexicon. A lexicon is a resource where all words are classified as positive or negative.

This is a huge task to collect all these words and classify them. We will look into some lexicons already written by some researchers and university.

Sometimes we can read all the sentences and add all the positive words but in reality the sentences is a negative.
eg: I love the way you cook, the utensils are amazing but the food sucks.
In this sentence we have two positive words and one negative word, but the overall it is  a negative sentences.


Machine learning based approaches:
These are based on Statistics and machine learning techniques. These learn themselves
This is a classification problem as are going to classify a document or a sentence as a positive or negative.

There are two commonly machine learning techniques used for sentiment Analysis.
1. Naive Bayes classification
2. Support vector machines

In a machine learning problem we have to tackle two problems
1. What are the training Data
2. What are the features which we will use:
  The simplest way is to look at the individual words in the document which is known as bag of words model.



In SVM, each document is a vector and can be represented as [x1,x2,x3..xn]
all the words in all the documents are [w1,w2,w3,...wn]

it works like, if w1 is present in the document, x1 = 1 else x1 = 0
we can also use the weights on it to see how much positive and negative the word is.

In some cases, we look at combinations of words. These are bi-grams or n-gram.

there are various lexicons
MPQA lexicon  <sup>[1](#reference1)</sup>
LIWC  <sup>[2](#reference2)</sup>  
Inquirer  <sup>[3](#reference3)</sup>
SentiWordNet<sup>[4](#reference4)</sup> containing opinion information  on  terms  extracted  from  the  WordNet  database  and  made  publicly  available  for  research purposes.
A (word,  meaning) pair is called a lemma.


Regular expression:

We will be using regular expression for extracting words from twitter.
We will use ```re``` module of python for that.
We will find the position where the pattern occurs by using ```re.search()```. It returns the first occurrence of the pattern else it returns none if the pattern does not occur.
```re.findall()``` it returns a list of string wherever the pattern is matched.
```re.finditer()``` : it returns the position of patterns as well as the text.


Following are the steps which we will use.
1. We will take input and search about it on twitter.
  Twitter provides a REST API for mining tweets. In python we have a module for this purpose called ```python-twitter``` module.
2. We will use machine learning classifier to classify it as positive/negative tweets. For which we will follow the following steps.
    1. Download a corpus to use a training database
        convert all the tweet to lower case
        replace links with the string 'url'
        replace @ with 'at_user'
        replace # word with the word
        remove stopwords(words like the, in , at etc)
        tokenize the tweet into words
    2. Extract features from both the test data and the training data.
       We will classify in two ways.
       - Naive bayes classification
       - Support vector machines

       Naive Bayes classification:
        1. Build a vocabulary(list of all the words in all the tweets in the training data).
        2. Represent each tweet with the presence/absence of these words in the tweet.
        3. Use nltk built in Naives bayes classifier to train the classifier


        Support Vector Machines:
        1. Build a vocabulary (list of all the words in all the tweets in the training data).
        2. represent each tweet with the presence/absence of these words in the tweet.
        3. weight each words with SentiWordNet subjectivity score.



3. Train a classifier on the training data
4. Use the classifier to classify the problem



---
## Conclusion:



---
### <ins> References and further reading list </ins>


<a name="reference1">1</a>: :https://mpqa.cs.pitt.edu/lexicons/
