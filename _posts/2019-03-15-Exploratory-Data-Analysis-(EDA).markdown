---
title:  Basic six steps to follow in any data science project
description: Exploratory Data Analysis (EDA) phase of a data science project helps us to analyze our datasets, summarize their main characteristics, understand their variables and relationships between them, in order to formulate some sort of hypotheses.
excerpt: Exploratory Data Analysis (EDA) phase of a data science project helps us to analyze our datasets, summarize their main characteristics, understand their variables and relationships between them, in order to formulate some sort of hypotheses.


tags:
  - Data Science

---


![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/front.jpg)

Before starting any data analysis tasks, we must have a clear goal about our results or output.We need to understand the data and problem to get meaningful results from our analysis.

Exploratory Data Analysis (EDA) phase of a data science project helps us to analyze our datasets, summarize their main characteristics, understand their variables and relationships between them, in order to formulate some sort of hypotheses. In this post, we will delve in important EDA techniques which are used by every data scientist/analyst.

## Step 1 : Import all the required libraries.
We will import numpy and padas

```
#import the libraries
import numpy as np  # we will use np as an alias for numpy
import pandas as pd # very well accepted alias for pandas is pd
```

**Numpy:** It is a fundamental tool for scientific computing. It has a very efficient array of operations and provided high-level mathematical functions. It is very good for homogeneous data types but in the real world, we have heterogeneous datasets( numerical as well as categorical features).

To tackle this heterogeneous dataset, we use pandas.

**Pandas:** is built on top of Numpy which allows operations on tabular data. The tabular data structure consists of rows and columns. In terms of pandas, we call it a data frame. On the data frame, we use different kinds of functions and joints.

>In Pandas: Rows is an observation and column is features or attributes.

## Step 2: Read the data
Once the data is imported, we will read the data in the data frame. In our case, we will read two excel files and load them into our data frame.

```
df_08 = pd.read_excel("data/all_alpha_08.xls", sheet_name=0)
```

### Step 2.1 : Learn more about the data
Once we have data in our data frame, we will learn about the data by using some functions on it. Following functions are very common for this purpose.

1. ```head()```

2. ```info()```

3. ```duplicated()```

4. ```describe()```

5. how many rows have missing values

Pandas documentation is the best place to discover and understand these functions. For the sake of completing this course, I will copy and paste about them.

### 1.  ```head()```
DataFrame.[head(n=5)](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.head.html)<sup>[1](#reference1)</sup> returns the first n rows for the object based on position. It is useful for quickly testing if your object has the right type of data in it.
> n: int, default 5

```
df_08.head()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/1_head.PNG)


### 2. ```info()```
This method <sup>[2](#reference2)</sup> prints information about a data frame including the index type and column types, non-null values and memory usage.
```
df_08.info()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/2_info.PNG)


### 3. ```duplicated()```
Return <sup>[3](#reference3)</sup> boolean Series denoting duplicate rows, optionally only considering certain columns. For finding the number of duplicated rows, we will use the sum function on the data frame.
   *example:* ```sum(df_08.duplicated())```
```
#no of duplicated rows in df_08
sum(df_08.duplicated())
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/3_duplicate.PNG)


### 4.```describe()```
Generate descriptive <sup>[4](#reference4)</sup> statistics that summarize the central tendency, dispersion and shape of a dataset’s distribution, excluding NaN values.

```
df_08.describe()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/4_describe.PNG)


### 5. Find how many rows have missing values
```isnull()
```
This function <sup>[5](#reference5)</sup> takes a scalar or array-like object and indicates whether values are missing (NaN in numeric arrays, None or NaN in object arrays, NaT in datetimelike).

In order to find all the rows, which has missing values, we will do a sum over it, as shown below.
```
# numbers of rows which have missing values
sum(df_08.isnull().any(axis=1))
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/5_isnull.PNG)


```
# nunique() returns number of unique elements in the object.
df_08.nunique()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/6_nunique.PNG)


## Step 3 : Drop unnecessary columns

Drop all the unnecessary columns which we don't need by using ```drop``` function.

We use ```inplace=True``` which tells the Dataframe, to copy the data frame back into the original df object.

```
df_08.drop(columns=["Stnd", "Underhood ID","FE Calc Appr","Unadj Cmb MPG"], inplace= True)
df_08.info()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/6_nunique.PNG)


## Step 4: Rename all column labels to replace spaces with underscores and convert everything to lowercase(Underscores can be much easier to work with in Python than spaces).
Being consistent with lowercase and underscores also helps make column names easy to remember.

```
df_08.columns = df_08.columns.str.lower().str.replace(' ','_ ')
df_08.info()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/7_drop.PNG)


## Step 5 : Clean the data

There are three common things to do in this part.
#### 1. Missing data
In every dataset, we have some missing values. It can be handled by imputing or removing them. Imputation is done by mean, median or backward or forward fill.

In case we are doing imputation, we use ```fillna``` function on the data frame for filling the data.

For removing the data we use ```dropna()``` on the dataset.

We will be just removing the missing values.

```
df_08.dropna(inplace=True)
```

#### 2. Duplicates
As discussed earlier, there is a ```duplicated``` function, for checking the duplicated rows. It show's the result in ```True``` or ```False```.

We can find the number of rows which are duplicated with the following command:

```
sum(df.duplicated())
```

In order to remove the duplicates we use
```
df_08.drop_duplicates(inplace=True)
print df_08.duplicated().sum()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/8_sum.PNG)

The sum of ```duplicated``` function is zero, which means there are no duplicates rows anymore.

```
df_08.info()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/9_df_info.PNG)

```
df_08.head()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/10_df_head_step.PNG)


In ```cyl``` column, string is attached to the integer. The data is dirty, so we will extract the integer from it, with the following way.

```
#  extract int from string.
df_08['cyl'] = df_08.cyl.str.extract(r'(\d+)', expand=True)
```

#### 3. Incorrect data types:
There are scenarios when the rows are not in the same datatypes. For example, dates are in String type. It will be more convenient to work with the date datatypes. We can change the string datatypes to date datatypes by the following command.

```
df['timestamp'] = pd.to_datetime(df['timestamp'])
```
There are two types of data, numerical and categorical data. All the algorithms understand numerical data. All the data should be converted into numerical data. We need to change some of the data types to float or int.
We will change some of the datatype to ```float``` datatypes.

```
# 2008: convert int to float.
df_08['air_pollution_score'] = df_08['air_pollution_score'].astype('float')
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/11_error.PNG)

```
df_08[df_08['air_pollution_score'] =='6/6'].head()
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/12_polution_score.PNG)

As we can see, this row has two fuels "ethanol/gas" and its air_pollution_score is ```6/6```. It would be better, if we create two different rows of these values by keeping the same values of the other columns.

```
# finding the number of rows which contains '/'.
sum(df_08['air_pollution_score'].str.contains('/'))
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/13_sum.PNG)

```
# copying the data which has two values into a new dataframe
double_fuel_08 = df_08[df_08['fuel'].str.contains('/')]
double_fuel_08_1 = double_fuel_08.copy()
double_fuel_08_2 = double_fuel_08.copy()
```
We will seperate columns which has two values in every rows and then split the data frame into two data frame to store two rows vlaues.
```
columns_to_split = ["fuel","air_pollution_score","city_mpg","hwy_mpg","cmb_mpg","greenhouse_gas_score"]
for col in columns_to_split:
    double_fuel_08_1[col] = double_fuel_08_1[col].apply(lambda x: x.split("/")[0])
    double_fuel_08_2[col] = double_fuel_08_2[col].apply(lambda x: x.split("/")[1])
```
Checking the data frame if it splitted in a desired way
 ```double_fuel_08_1.head()
 ```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/14_double_fuel.PNG)

```
double_fuel_08_2.head()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/15_head2.PNG)

Now we will delete the rows which contains '/'  from ```double_fuel_08``` and add two newly created data frame.

```
double_fuel_08.index
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/16_index.PNG)

```
df_08.info()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/17_in.PNG)


Dropping the rows
```
df_08.drop(double_fuel_08.index, inplace=True)
df_08.info()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/18_after_dropping.PNG)

```
# checking all the rows which contains '/'
df_08[df_08['fuel'].str.contains('/')]
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/19_check.PNG)

Appending the two data frame with two distinct values into one data frame.
```
rows = double_fuel_08_1.append(double_fuel_08_2)
rows.head()
```

![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/20_rows.PNG)

```
df_08 = df_08.append(rows, ignore_index=True);
df_08.shape
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/21_shape.PNG)

##### 3.1 Converting the rest of the columns into float

```
# convert object to float
df_08['air_pollution_score'] = df_08['air_pollution_score'].astype('float')
df_08['air_pollution_score'].dtype
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/22_dtype.PNG)

```
column_list=['city_mpg', 'hwy_mpg', 'cmb_mpg','greenhouse_gas_score']
for col in column_list:
    df_08[col] = df_08[col].astype('float64')

df_08.dtypes
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/23_dtypes_2.PNG)

## Step 6: Exploring with Visuals

For numerical datatypes, to understand the variable visually is with a histogram. To get the histogram of a pandas series, we can use the hist method, as shown below.

```
df_08["cmb_mpg"].plot(kind="hist", title="combined mpg in 2008");
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/24_histo.PNG)

```
#Describe the correlation between displacement and combined mpg.
df_08['displ'].corr(df_08['cmb_mpg'])
```
![EDA](/assets/images/2019-03-15-Exploratory-Data-Analysis-(EDA)/25_corr.PNG)


## Conclusion:

In this post, you learned about Exploratory data analysis(EDA) which is very important in every data science project. These basics steps should be mastered by a data analyst/scientist. As we can see, these steps are easy to remember and practice. Take a data set and practice this method to have more confidence. In case you are not able to remember, then there is no problem. You can always search and find their solutions. As I said in an earlier post, you should know how to find the solutions for problems as a data scientist/analyst. I hope, this helps and motivates you to explore more about EDA and other phases of a data science project.


---
### <ins> References and further reading list </ins>


<a name="reference1">1</a>: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.head.html

<a name="reference2">2</a>: http://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.info.html

<a name="reference3">3</a>: http://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.duplicated.html

<a name="reference4">4</a>: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.describe.html

<a name="reference5">5</a>: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.isnull.html
