---
title:  How to make a blog like this?
description: This post explains how to make a website or blog with Jekyll
categories:
  - Jekyll
tags:
  - Jekyll
  - Liquid
---

Whenever we hear about blogs we think more often about WordPress or BlogSpot blogs. [WordPress](https://wordpress.com/) is more popular once right now. It is an open source online website creation tool, which was written in PHP and MySQL.

Lots of people complain about their WordPress blog getting infected with malware or hacked, or being slow etc. Let us learn about Jekyll and how it overcomes the problems mentioned above.



##  Introducing Jekyll

Jekyll transforms plain text into static websites. It is a simple static site generator, and takes a source file (written in markup language) for creating a static website.
It supports all kinds of file formats and is good for quickly creating a blog.  

> In 2009, Jekyll was written in Ruby, by [Tom Preston-Werner](http://tom.preston-werner.com/), GitHub's co-founder.

Though it needs some technical background and a good knowledge of [Markdown](https://www.markdownguide.org/getting-started) and the [Liquid](https://shopify.github.io/liquid/) templating language, which is easy to learn if you have some basics of HTML. Ever since it is getting popular and glimpse of Jekyll popularity can be seen on [Showcase](https://jekyllrb.com/showcase/) and [wiki](https://github.com/jekyll/jekyll/wiki/sites).


For this blog, I preferred [Jekyll](https://jekyllrb.com/) because of the following reasons.


1. **Performance:** Extremely fast as web server only returns static files.

2. **Secure:** There are only static files which means content is not produced dynamically, so there is no chance for it to get exploited or hacked. Until someone hacked the server.

3. **Less costly:** It requires less resources which reduces its operative cost.

4. **Easy to learn:** If you know HTML, CSS and JavaScript then only learning a new templating language called [Liquid](https://shopify.github.io/liquid/) will suffice.

5. **Low maintenance:** With first-class support for Markdown, and the Liquid templating language, making a blog is as easy as running two commands. It takes less then five minutes for setting up Jekyll and the maintaining cost is minimum.

6. **Big community:** Jekyll has big active community and a team of Core maintainers which is working hard to maintain it. They have documented Jekyll very well.

7. **New Learning Experience:** Blogging is a the best way to learn and share about new technologies. We learn more by teaching others and while getting your hands dirty with real world problems.




### TL;DR Procedure for creating a blog on Jekyll like this one:
---
1. Install [Ruby](https://rubyinstaller.org/).
2. Install [Jekyll](https://jekyllrb.com/docs/installation/) and [bundler gems](https://jekyllrb.com/docs/ruby-101/#bundler).
3. Download the [theme](https://github.com/mmistakes/minimal-mistakes).
4. Modify the **GEMFILE**.
5. Modify **_config.yml** file.
6. Run the server.



Jekyll is written in Ruby so we have to install Ruby as well and it is one of the [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems).
This [stackoverflow  answer on Gem](https://stackoverflow.com/questions/5233924/what-is-a-ruby-gem) explains very well about Gem.
>  RubyGems is a package manager for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries (in a self-contained format called a "gem"), a tool designed to easily manage the installation of gems, and a server for distributing them.

We can find the detail installation process on the Jekyll website [here](https://jekyllrb.com/docs/installation/) but nevertheless we can find the procedure below as well.

Since I used Windows(O.S) I will follow

We can download the repository by two ways.


1.
  a. Click on the link  and  download the repository. Save the file in the desired folder and unzip it.

  b. Open Git bash and clone the repository like this.

You have to install Ruby for Jekyll. If you don't have Ruby installed on your pc then download from here.


2. Go inside the folder. Find the Gemfile and modify it like this

``` source 'https://rubygems.org'
gem "minimal-mistakes-jekyll"
gem 'jekyll-include-cache'
gem 'jekyll-archives'
```
  Save the file.

3. Open the file __config.yml  
   search for "plugins" (line - 225) and add the following lines
    -jekyll-include-cache
    -jekyll-archives

    search for jekyll-archives and uncomment the lines from 262 till 270


4. Open the bash



ATOM

markdown-preview



---
#### REFERENCES
1. https://jekyllrb.com/
2.  https://github.com/jekyll/jekyll/wiki/sites
3.  https://jekyllrb.com/showcase/
4. https://rubyinstaller.org/
4.  https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet#emphasis
5. https://jekyllrb.com/docs/ruby-101/#gems
