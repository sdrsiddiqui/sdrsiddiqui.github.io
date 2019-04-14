---
title:  Common Steps to follow in any Data Science project
permalink: /Common-steps-to-follow-in-any-data-science-project/
description: Exploratory Data Analysis (EDA) phase of a data science project us for analyzing datasets to summarize their main characteristics.
excerpt: Exploratory Data Analysis (EDA) phase of a data science project us for analyzing datasets to summarize their main characteristics. It helps to understand the data, variables and relationships between them to formulate some sort of hypotheses.

Before starting any data analysis tasks, we must have a clear goal about our results or outout. We need to understand the data and problem to get a meaningful results from our analysis.

header:
    overlay_filter: "0.1"


tags:
  - Data Science

---


This post is about EDA phase. EDA means Exploratory data analysis. We will learn important EDA techniques which is used by every data Scientist.

Basic structure
Summary structure
Distributions
Grouping
Crosstabs
Pivots

Numpy:
It is a fundamental tools for scientific computing as it has very efficient array operations  and provided high level mathematical functions.
It is very good for homogeneous data types but in real world data set we have heterogenous datasets( numerical as well categorical features).


To tackle this heterogeneous datasets, we use pandas. Pandas is built on top of Numpy which allows operations on tabular data.

Rows is an observations
column is a features or attributes

If we have columns of different data types, pandas help us to deal with such data types in an efficient manner.
The tabular data structure consists of rows and columns and in terms of pandas we call it a data frame. On data frame we can use lots of functions and joints.
Matplotlib is used by pandas for creating visualizations.



Cleaning the data:  There are three common things which are very common.
1. Missing data: We handle this by imputing them. There are various ways to do this like imputing with mean or median.
we use ```fillna``` function on the data frame for filling the data.
```

```

2. Duplicates : there is a ```duplicated``` function for checking which rows are dulplicated.
```
df.duplicated()
```
It will show the result in ```True``` and ```False```.

We can find the number of rows which are duplicated with the following command:

```
sum(df.duplicated())
```

In order to remove the duplicates we use
```
df.drop_duplicates(inplace=True)
```


3. Incorrect data types:
There are scenarios when the rows are not in the same datatypes.
For example dates is in String type. It will be more convenient to work with the date datatypes. We can change the string datatypes to date datatypes by the following command.

```
df['timestamp'] = pd.to_datetime(df['timestamp'])
```

### Basic plotting with Pandas






Functions act as stand alone segments of code that usually take an input, perform some processing, and return some output. When we're working with Python lists, we can use the len() function to calculate the length of a list, but if we're working with Python strings, we can also use len()

In contrast, methods are special functions that belong to a specific type of object. Python lists have a list.append() method that we can use to add an item to the end of a list.


Summary Statistics
