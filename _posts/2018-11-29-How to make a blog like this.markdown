---
title:  How to make a blog like this?
description: This post explains how to make a website or blog with Jekyll
categories:
  - Jekyll
tags:
  - Jekyll
  - Liquid
---


How to make a blog like this?



The decisions depends mainly on various criteria?
1. Why we are creating a website?
2. resources or expertise on the languages
3. desire of learning a new language

For me it was the
I decided Jekyll because of the following reason.
The blog is made on Jekyll.  Jekyll transforms plain text into static websites and blogs. It is also known as a static site generator, which means it takes source files and generates a static website.
It is written in Ruby in 2009 by the co-founder of GitHub. It uses Liquid as templating language, which is also open source.. The input is in the format of Markdown and the out put is in HTML.

1. Easy to learn: if you are aware of HTML, CSS and Javascript. Only you have to learn a new templating language called Liquid(https://shopify.github.io/liquid/).
2. Fast : Extremely fast as web server only returns static files. loading static files on server is fast as well. It used Markdown which
3. Secure : There are only static files and a web server, nothing dynamic which could be exploited.
4. Big community and well documented.


There are many themes which are available for the website, which could be found here.
I prefered .......because of its simplicity. Please check this out


Procedure :

We can download the repository by two ways.

1.
  a. Click on the link  and  download the repository. Save the file in the desired folder and unzip it.

  b. Open Git bash and clone the repository like this.

You have to install Ruby for Jekyll. If you don't have Ruby installed on your pc then download from here.


2. Go inside the folder. Find the Gemfile and modify it like this

source 'https://rubygems.org'
gem "minimal-mistakes-jekyll"
gem 'jekyll-include-cache'
gem 'jekyll-archives'

  Save the file.

3. Open the file _config.yml  
   search for "plugins" (line - 225) and add the following lines
    -jekyll-include-cache
    -jekyll-archives

    search for jekyll-archives and uncomment the lines from 262 till 270


4. Open the bash
