---
title:  How to use Jupyter more effectively?
permalink: /How-to-use-Jupyter-more-effectively/
description: Jupyter is a very useful tool for machine learning, data science, visualizations as it can contain code, equations, visualizations etc in one place.
excerpt: Jupyter is a browser-based graphical interface of Ipython shell. It is an open-source web application which allows a user, to create and share documents, which can execute on their systems.It is a very useful tool for machine learning, data science, visualizations as it can contain code, equations, visualizations etc in one place. It blends two things, Python(a simple scripting programming language) and Wiki pages.

header:
    overlay_filter: "0.1"


tags:
  - Data Science

---

IPython is about using Python effectively for interactive scientific and data-intensive computing. There are two methods of using it; the IPython shell and the IPython notebook.

### IPython shell ###

IPython interpreter can be launched by typing:

```
$ ipython

```
 on the command line. It will look like

![ipython](/assets/images/2018-12-15-Data-Science/3_ipython.png)

*<sub>ipython shell</sub>*

### IPython notebook ###

[Jupyter](https://jupyter.org/) is a browser-based graphical interface of Ipython shell. It is an open-source web application which allows a user, to create and share documents, which can execute on their systems.

It is a very useful tool for machine learning, data science, visualizations as it can contain code, equations, visualizations etc in one place. It blends two things, Python(a simple scripting programming language) and Wiki pages.

To run IPython notebook, it is very easy just by typing the following on system shell:

```
jupyter notebook

```
It will appear as:

![Jupyter](/assets/images/2018-12-15-Data-Science/05_startingJupyter.png)
*<sub>starting jupyter notebook</sub>*


A local web server and browser will automatically open and navigate to the local URL. If not, manually, it could be accessed at http://localhost:8888 on the browser.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/06_jupyter_browser.png)
*<sub>Jupyter notebook on the browser at local localhost</sub>*


## Basics of Jupyter Notebook ##

Click on the New > Python 2, for creating a new notebook. For giving it a name, click on the "untitled" and change it. The jupyter notebook is made up of cells where the python code is written as shown:

![Jupyter browser](/assets/images/2018-12-15-Data-Science/07_Hello World2.gif)
*<sub>Hello World on jupyter</sub>*

You can find the source code of the previous program here:
```
print "Hello World"
```

The cell is executed by clicking Cell > Run Cells or by ``` Shift + Enter```.

> ```Shift + Enter```execute the cell and create a new cell below it.
> ```Crtl + Enter```execute the cell only.


Markdown is used for formatting the cells. To convert it, go to Cell > Cell Type > Markdown or type ```Esc + M```.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/08_Formating_Text.gif)
*<sub>Formating text on jupyter</sub>*


> In Markdown language: # is used for H1 Heading like in HTML and ## like H2, only the font size decrease.


**Create a variable**

Python is a scripting language. Variables are created on the fly, there is no need to declare it before or their types, like in another language like C. Any global variable which is created can be used in another cell.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/09_Type_variable.gif)
*<sub>Creating variable in jupyter</sub>*

Source code of the above program:
```
i = 15
type(i)
```

Different variables can be created in the Jupyter notebook as follows:

![Jupyter browser](/assets/images/2018-12-15-Data-Science/10_types.gif)
*<sub>Creating variable in jupyter</sub>*


## Some advanced level python ##
### List ###
The list is made by comma-separated values between square brackets[]. To access values in lists, use square brackets with the index number.
 * List is mutable, which means they can be changed.
 * It is an ordered collection of objects, the order in which elements are defined is maintained like that.

### Dictionary ###
Dictionary is made by placing the values inside the curly brackets{} separated by a comma. It is a pair that consists of a key and value. To access the 'value', the 'key' is put in the square brackets [].
 * It is mutable.
 * Dictionaries are unordered.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/11_list_and_dictionary.gif)
*<sub>List and dictionary in jupyter</sub>*

You can find the source code of the previous program here:

```
l = [1,3,5,7,9] # list
print l
print l[2]

dic = {'firstValue':1,'secondValue':2,'thirdValue':3}
dic['firstValue']
```

### Creating functions ###
A function is a group of statements, which perform a specific task. Data(also known as parameters)can be passed into a function which returns a data as a result.

There are two ways to define a function:

* Normal functions are defined by the ```def``` keyword as shown below:

![Jupyter browser](/assets/images/2018-12-15-Data-Science/12_function.gif)
*<sub>Function in python</sub>*

You can find the source code of the previous program here:
```
def mul(a, b):
    return a*b

mul(4,5)
```

* Lambda function also known as anonymous functions. The syntax of a lambda function is ```lambda arguments: expression```. Lambda functions are single-expression functions that can have numbers of arguments.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/13_lambda.gif)
*<sub>Lambda function in python</sub>*

You can find the source code of the previous program here:

```
cube = lambda y : y* y*y

cube(5)
```
---

**Documentation with ?**

Python has a built-in help() function that accesses the docstring (it contains the summary of the object) information and prints the results.

> In IPython, the ? character is a shorthand for accessing documentation for functions or other objects.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/14_doc.gif)
*<sub>Accessing documentation in python</sub>*

You can find the source code of the previous program here:
```
help(len)

len?
```


**Source Code with ??**

Source code can be accessed in IPython just by putting a double question mark ( ?? ) after the function.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/15_source_code.gif)
*<sub>Accessing source code in python</sub>*

You can find the source code of the previous program here:
```
cube??

len??
```
> Sometimes the ?? suffix doesn’t show source code, because that particular object is not implemented in
Python, but in other language or in C. In this case, the output of ?? is the same as the ? suffix.


## Magic Functions ##
Magic functions solve common problems in data analysis using Python. These are of two types.

1. Line magics: operate on a single line of input and have single % prefix.
2. Cell magics: operate on multiple lines of input and have double %% prefix.


### %automagic ###

If the argument is set to 1 then there is no need to type the initial ```%``` before magic functions. It can be deactivated by setting to 0.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/16_automagic_function.gif)
*<sub>automagic function in IPython</sub>*


### %cd ###

It is used to change the current directory. This is a line magic function. A tab can be used to see the different options available. IPython session has *_dh*  variable in which an internal list of directories is stored.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/17_cd_magic_function.gif)
*<sub>cd magic function in IPython</sub>*


### %dhist ###

It is used to see all the directories visited in a current session. It uses the *_dh* variable list to show the list of directory.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/18_dhist_magic_function.gif)
*<sub>dhist magic function in IPython</sub>*


### %run ###

Python script can be run from within IPython shell by %run command.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/19_run.gif)
*<sub>%run magic function in IPython</sub>*

hello.py file of the above %run magic function.

```
def hello():
    return "Hello World"

print( hello())
```


### %timeit ###

[%timeit](https://stackoverflow.com/questions/29280470/what-is-timeit-in-python) is an ipython magic function, which is used to time the execution of a particular piece of code. It can be a single execution statement, or a single method. It belongs to the line magic function.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/20_timeit.gif)
*<sub>%timeit magic function in IPython</sub>*



## Shell Commands in IPython ##

The shell commands can also be used in IPython, just by adding ! character before the command.

![Jupyter browser](/assets/images/2018-12-15-Data-Science/21_shellcommands.gif)
*<sub>Some shell commands in IPython</sub>*

You can find the source code of the previous program here:
```
!ls
!pwd
!echo "Hello"
```

### Some Shortcuts ###
* ```Shift + Enter```: Execute the cell and create a new cell below it.
* ```Ctrl + Enter```: Execute the cell only.
* ```Esp + M```: To get Markdown.
* ```Esp + L```: To get line numbers in long code.


## Conclusion ##
In this post, you learned about IPython. We started with the  basics of Jupyter notebook and covered a little bit of python, magic functions and how to use shell commands in IPython. For being an effective data scientist or software engineer, it is very important to know how to find information about unknown problems through webs search or other means rather than memorizing the tool or the command.



---
### <ins> References and further reading list </ins>

1. [Ipython](http://ipython.org/)

2. [IPython Documentation](https://ipython.readthedocs.io/en/stable/)
