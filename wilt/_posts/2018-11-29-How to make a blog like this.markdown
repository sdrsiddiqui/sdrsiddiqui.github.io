---
title:  5 steps for making a blog with Jekyll
description: This post explains how to make a website or blog with Jekyll
categories:
  - wilt
tags:
  - Jekyll
  - Liquid
---

Whenever we hear about blogs we think more often about WordPress or BlogSpot blogs. [WordPress](https://wordpress.com/) is more popular once right now. It is an open source online website creation tool, which was written in PHP and MySQL.

Lots of people complain about their WordPress blog getting infected with malware or hacked, or being slow etc. Let us learn about Jekyll and how it overcomes the problems mentioned above.



##  Introducing Jekyll

[Jekyll](https://jekyllrb.com/) transforms plain text into static websites. It is a simple static site generator, and takes a source file (written in markup language) for creating a static website.
It supports all kinds of file formats and is good for quickly creating a blog.  

> In 2009, Jekyll was written in Ruby, by [Tom Preston-Werner](http://tom.preston-werner.com/), GitHub's co-founder.

Though it needs some technical background and a good knowledge of [Markdown](https://www.markdownguide.org/getting-started) and the [Liquid](https://shopify.github.io/liquid/) templating language, which are easy to learn if you have some basic knowledge of HTML.
Ever since it is getting popular and glimpse of Jekyll popularity can be seen on [Showcase](https://jekyllrb.com/showcase/) and [wiki](https://github.com/jekyll/jekyll/wiki/sites).


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
1. Install [Jekyll](https://jekyllrb.com/docs/installation/).
2. Download the [theme](https://github.com/mmistakes/minimal-mistakes).
3. Built the site.
4. Modify the files **Gemfile** and  **_config.yml** file.
5. Built the site and run the server.

---

The above steps are explained below in details.


### Installing Jekyll ###

Install [Jekyll on windows](https://jekyllrb.com/docs/installation/windows/). Installation procedures are very well documented on Jekyll website.

<figure>
  <img src="/assets/images/2018-11-29/1_Jekyll.png" alt="Jekyll for windows">
  <figcaption>Jekyll for windows</figcaption>
</figure>

According to the Jekyll official [documentation](https://jekyllrb.com/docs/installation/windows/): The easiest way to run Jekyll is by using the [RubyInstaller](https://rubyinstaller.org/) for Windows.
<figure>
  <img src="/assets/images/2018-11-29/2_Ruby_installation.png" alt="Ruby installation">
  <figcaption>Ruby for windows</figcaption>
</figure>

Jekyll is a  [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems). On [stackoverflow](https://stackoverflow.com/questions/5233924/what-is-a-ruby-gem) Gem is explained.
> Gem is a package manager for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries, a tool designed to easily manage the installation of gems, and a server for distributing them.



### Download the theme ###

I preffered the minimal mistake [theme](https://github.com/mmistakes/minimal-mistakes) created by Michael Rose. I find it simple and elegant theme which is very well [documented](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/).

We can download the theme directly from the link above and save it. I would recommend using Git. Open [Git bash](https://git-scm.com/download/win) and type the following command:

 ```
 $ git clone https://github.com/mmistakes/minimal-mistakes
```
<figure>
  <img src="/assets/images/2018-11-29/3_Git.png" alt="Git">
  <figcaption>Downloading minimal mistake theme with Git bash</figcaption>
</figure>

Change into your new directory. Now, we need to install Bundler in our project folder by the following code.


 ```
$ cd minimal-mistakes/
$ bundle install
 ```

<figure>
  <img src="/assets/images/2018-11-29/4_Bundle_install.png" alt="Install Bundle with the command">
  <figcaption>Installing Bundle with Git bash</figcaption>
</figure>

> Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.


### Built the site  ###

Build the site and make it available on a local server by the following command:

```
$ bundle exec jekyll serve
```

<figure>
  <img src="/assets/images/2018-11-29/5_Build_the_site.png" alt="Built the Jekyll site by simple command">
  <figcaption>Built the Jekyll site </figcaption>
</figure>

Now browse to http://localhost:4000 to see your site.

<figure>
  <img src="/assets/images/2018-11-29/6_Localhost_site.png" alt="Built the Jekyll site by simple command">
  <figcaption>Built the Jekyll site </figcaption>
</figure>


### Modify the files **Gemfile** and  **_config.yml** file ###

Modify your **Gemfile** with the following code
```
source 'https://rubygems.org'
gem "minimal-mistakes-jekyll"
gem 'jekyll-include-cache'
gem 'jekyll-archives'

```

Modify **_config.yml** file

Now we need to modify config.yml file. We need to modify some places.

We start with modifying plugins. Add the following line  
```
- jekyll-archives
```
at line 225. So that the final plugins will look like this

```
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache
  - jekyll-archives

```

Now we will uncomment the jekyll-archives which can be found at line 254. We will uncomment it till line 263. It will look like following:

```
jekyll-archives:
  enabled:
     - categories
     - tags
  layouts:
     category: archive-taxonomy
     tag: archive-taxonomy
  permalinks:
     category: /categories/:name/
     tag: /tags/:name/

```

We will add the following lines at the defaults (line 287)
```
jekyll-archives:
  enabled:
     - categories
     - tags
  layouts:
     category: archive-taxonomy
     tag: archive-taxonomy
  permalinks:
     category: /categories/:name/
     tag: /tags/:name/

```

In Site Settings we will activate breadcrumbs on line 27 by making it true. It will look like as follows:
```
breadcrumbs              : true # true, false (default)
```

We can change the title, name and description as we want.

In the Site Author section we modify the author name, bio, location, links to email, twitter, facebook etc according to our requirements.



### Built the site  ###

Build the site and make it available on a local server

```
$ bundle exec jekyll serve
```

<figure>
  <img src="/assets/images/2018-11-29/5_Build_the_site.png" alt="Built the Jekyll site by simple command">
  <figcaption>Built the Jekyll site </figcaption>
</figure>

Now browse to http://localhost:4000 to see your site.


###Conclusion###

We have learned about Jekyll, its advantages and also about how to make a blog in just five steps. Jekyll is a very powerful tool which is becoming very powerful for blogging which opens new ways to make a website faster and more secure.

---
#### REFERENCES
1. [Jekyll](https://jekyllrb.com/)
2. [Wiki](https://github.com/jekyll/jekyll/wiki/sites)
3. [Showcase](https://jekyllrb.com/showcase/)
4. [RubyInstaller](https://rubyinstaller.org/)
4. [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems)
