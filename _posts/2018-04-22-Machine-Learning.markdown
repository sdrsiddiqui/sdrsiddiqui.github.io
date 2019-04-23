---
title:  Basics of Machine learning.
description: Nowadays we are hearing machine learning all the time and how it is present everywhere. Many of you tried to find it's definition on the web and came up with the following classic definition by Tom Mitchell, which he gave in 1997 in his book "Machine Learning".
excerpt: Nowadays we are hearing machine learning all the time and how it is present everywhere. Many of you tried to find it's definition on the web and came up with the following classic definition by Tom Mitchell, which he gave in 1997 in his book "Machine Learning".

header:
    overlay_filter: "0.1"


tags:
  - Machine learning

---

![Machine learning](/assets/images/2018-04-22-Machine-Learning/1_ML.jpg)


Nowadays we are hearing machine learning all the time and how it is present everywhere. Many of you tried to find it's definition on the web and came up with the following classic definition by Tom Mitchell, which he gave in 1997 in his book [Machine Learning](https://amzn.to/2GqWA4E)<sup>[1](#reference1)</sup>.

*" A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E".*

Are you wondering what is this E, T, P, etc? At once, it looks so complicated and weird.  At least, this is how I felt. In simple terms it can be defined as "Machine learning is learning from data or examples".  We use data to learn some sort of patterns and once we learn these patterns then we can do some sort of predictions. In other words, in machine learning, we take data, learn the pattern and then use this pattern to make predictions.

For example, spam email filter is a machine learning program.

> "Machine learning is learning from data or examples".

**Training data:** The data which are used to understand or learn the pattern is called training data. It is composed of two components:
1. Input features: Input features are also called predictors because they are used to predict the output.
eg: Taking our spam email example, it is sender URL, email content is input features.

2. Output features: output features is called response or outcome.
eg:  whether it is spam or not.


If we want to detect if a new email is a spam or not. This new email has only input features and we want to predict the output features, based on the learned pattern.
These unseen cases are called test data.

**Test data:** In test data, we have only input data/features and we predict the output data.

---
### Problems which can be solved by machine learning
A very good article <sup>[2](#reference2)</sup> explained the problems which can be solved by machine learning. For the sake of completing this tutorial, I copy some of them here.

1. Manual data entry
2. Detecting spam
3. Product recommendation
4. Medical Diagnosis
5. Financial analysis
6. Image recognition (computer vision)

---
### How to know if a problem is a machine learning problem?
Not every problem is a machine learning problem. The following three factors determine if machine learning can be used to solve a problem:
1. There are data available.
2. A pattern should exist
3. It could not be solved mathematically.

Always look for these three factors to decide if machine learning is a tool to solve a particular problem.


---
## Types of machine learning.
There are various types of the machine learning system, here will focus only supervised and unsupervised.

**Supervised learning:** If we have both input and output features in a training data is called supervised learning. It is called supervised because we already have the output features, which we want to predict by using machine learning.
Eg: If we want to predict whether an email is a spam <sup>[3](#reference3)</sup>  or not. We will use various input features in order to determine it. We already know the output of our prediction, it will be either spam or not spam. This kind of problems is called a classification problem. Here we are classifying the output into two parts. So, it is a binary classification problem.

Another problem could be where we want to predict a house price or salary based on various input features. Instead of predicting labels, we predict a value which is continuous in nature(if it is a positive value). This sort of task is called regression.
In other words, problems, where output is a continuous variable, is called a regression problem.


**Unsupervised learning:** Machine learning problems where we only have input features in the training data is called unsupervised learning. In other words, we try to find a pattern in the training data and then apply that pattern on test data or we can say we are trying to learn with a teacher.

Eg: Customer segmentation: We want to group people who are reading your blog based on the topic they are reading on your post, this is an example of clustering.


---
## Conclusion:

In this post, I tried to explain machine learning in a simple way. We saw what is train data, test data and types of machine learning, supervised and unsupervised learning. We also learn what is classification and regression problem.

In the following post, we will learn more about different types of algorithms and how to approach a machine learning problems until then explore more through the references.


---
### <ins> References and further reading list </ins>
<a name="reference1">1</a>: [Machine Learning](https://amzn.to/2GqWA4E)

<a name="reference2">2</a>: https://www.marutitech.com/problems-solved-machine-learning/

<a name="reference2">3</a>: [Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems](https://amzn.to/2USvFZu)

<div id="amzn-assoc-ad-6c607667-0546-4b15-8490-17601f30f7c0"></div><script async src="//z-na.amazon-adsystem.com/widgets/onejs?MarketPlace=US&adInstanceId=6c607667-0546-4b15-8490-17601f30f7c0"></script>
