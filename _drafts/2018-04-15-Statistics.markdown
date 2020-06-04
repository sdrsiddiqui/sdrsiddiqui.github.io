---
title:  Statistics
description:
excerpt:

header:
  overlay_color: "#000"
  categories:
    - wilt

tags:
  - Data Science
  - WILT

---


![DataScience](/assets/images/2018-12-15-Data-Science/0_data_science_front.jpg)

Data :

Data is a pieces of information which we get from various sources like text, videos, audios, data bases etc.

There are two types of data : Quantitative and Categorical.

**Quantitative data:** are numeric values and we can perform mathematical operations on it. Eg: salary of person, age etc

**Categorical data:** are not numerical but are in categories and are used to label a group or set of items. Eg: Marital status

Categorical data are of two types: Ordinal and nominal

**Ordinal:** categorical data that are ranked.
Eg: marks in exams, level of educations, rating on amazon etc

**Nominal:** categorical data that do no have ranked order.
eg: types of food, animals, people etc


Quantitative data are also of two types: Continuous and discrete.

**Continuous data type:** dat that can be split into smaller units. it can be positive as well as negative.
eg: Age, income, distance taken to walk

**Discrete data:** data that are countable. this can be only positive.
eg: how many cars are there in a street, number of actors in a movie etc


> If we add two data in the form of numbers and it give some useful information then it is a  Quantitative else it is a categorical Data.
eg: zip code are numbers but when we add two zip codes it doesn't give nay insight, so it is regarded as categorical data.
so we will consider it as a labels for a group


> we should see if we can split our data into smaller and smaller units then this data type is continuous.


Quantitative data:

we analyze Quantitative data in four ways
1. Measures of Center
  1.1 Mean
  1.2 Median
  1.3 Mode
2. Measure of spread
3. Shape of Data
4. Outliers

  Mean: it is an average value of the dataset.

  Median: It is the middle value of a data set. In order to compute the median we MUST sort our values first.
  for odd, median is the middle value.
  for even, median the mean of two middle values

  Mode: The value which occur most often is called mode.
  No Mode: If all observations in our dataset are observed with the same frequency, there is no mode.

  Many Modes: If two (or more) numbers share the maximum value, then there is more than one mode. I


Boxplot: it is useful to compare the spread of two data sets
Histogram: Most useful for Quantitative datasets.


2. Measure of spread:
  2.1 Range : difference between the maximum and the minimum.
  2.2 Interquartile Range:  the difference between Q3(The value such that 75% of the data fall below) and Q1( value such that 25% of the data fall below)​.
  2.3 Standard deviation :  is defined as the average distance of each observation from the mean. In other words, how far each point varies from the mean of the points.
  2.4 Variance: average square difference  of each observation from the mean.
  Standard deviation is the square root of the variance.
The standard deviation is a measurement that has the same units as the rest of our data, and the units of the variance are the square of our original data.

  The standard deviation is the square root of the variance. In practice, you usually use the standard deviation rather than the variance. The reason for this is because the standard deviation shares the same units with our original data, while the variance has squared units.


    1. Standard deviation is used to compare spread of different groups. higher the value the more it is spread.
    2. High standard deviation means higher risk. eg: if stock prices changes with higher deviation with time is compare more risky then which fluctuates with lower standard deviation.
    3. To compare in a fair way, all data should be in the same units.
    4. Standard deviation is used more often because it shares the same units as the original data set.

standard deviation is used in finance, medical use and finding the errors of results etc.


the variance as:

1n∑i=1n(xi−xˉ)2\bold{\frac{1}{n}\sum\limits_{i=1}^n(x_i - \bar{x})^2}n1​i=1∑n​(xi​−xˉ)2

You will also see:

1n−1∑i=1n(xi−xˉ)2\bold{\frac{1}{n-1}\sum\limits_{i=1}^n(x_i - \bar{x})^2}n−11​i=1∑n​(xi​−xˉ)2


3. Shape of distribution:
A histogram help us in identifying the shape of distribution.
there are three Shape
1. right-skewed
2. left-skewed
3. symmetric

symmetric distribution:
one of the common symmetric distribution is called Normal distribution. It is also called the bell curve. In this case, mean = median = Mode. Mode(no. of times a value occur) is the tallest bar in the histogram.

right-skewed: mean > median

left-skewed : mean < median

When we have data that follows a normal distribution, we can completely understand our dataset using the mean and standard deviation.

However, if our dataset is skewed, the 5 number summary (and measures of center associated with it) might be better to summarize our dataset.
Mode is the tallest bar in the histogram. There can be more than one tallest bar.



4. Outliers :
These are the values which are extreme values. There are various ways of finding them. We can see the outliers with the simple histogram.
or with the median or standard deviation.
There are various ways to handle them.
1. Plot the data
2. handle the data with the following ways.
  1. we can remove them if they are some typing errors.
  2. we can accept the fact that there can be an Outliers.
  3. we can figure out the outliers with histogram or Boxplot.
  4. we need to find their impact on the summary Statistics
  5. use the describe function in numpy which gives us min, max, mean, 1st quartile, 2nd quartile, 3rd quartile, 4rth quartile.






 Categorical data is analyzed usually be looking at the counts or proportion of individuals that fall into each group


Probability :
we predict about future events based on the models. In this, we are predicting data.

Statistics : we analyze the data from past events to infer those model causes could be. we are using data to predict




---
## Conclusion:

In this post, you learned about Data Science and learn why Python is preferred for it. We also explored different steps for starting data science projects and finally, we saw the environment which is required for a data science project. I hope it helps to understand some basics concepts of data science. In the coming tutorials, we will explore more about data science and the various algorithm used for it, till then explore more go through the references.


---
### <ins> References and further reading list </ins>


<a name="reference1">1</a>: https://www-01.ibm.com/common/ssi/cgi-bin/ssialias?htmlfid=WRL12345USEN

<a name="reference2">2</a>: en.wikipedia.org/wiki/Data_science

<a name="reference3">3</a>: http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram

<a name="reference4">4</a>: https://www.anaconda.com/
