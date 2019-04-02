---
title:  Create a Jekyll blog in five steps
permalink: /Create-Jekyll-blog-in-five-steps/
description: This post explains how to make a website or blog with Jekyll
excerpt: "Jekyll transforms plain text into static websites. In other words, it is a simple static site generator which takes a source file for creating a static website."
header:
  image: /assets/images/2018-11-29-Create Jekyll blog in five steps/0_logo-2x.png
  overlay_color: "#000"
categories:
  - wilt
tags:
  - Jekyll
  - Liquid
---

Whenever we hear the word blog, WordPress or BlogSpot blogs cross our mind. Out of which [WordPress](https://wordpress.com/) is more in demand right now. It is an open source online website creation tool, which was written in PHP and MySQL.

But lots of people complain that WordPress blog is getting infected with malware or hacked, or being slow etc. So to overcome this problem, bloggers are migrating towards Jekyll.
In the next section, Jekyll is explained as well as and how it overcomes the problems which WordPress is encountering.


##  Introducing Jekyll

[Jekyll](https://jekyllrb.com/) transforms plain text into static websites. In other words, it is a simple static site generator which takes a source file (written in the markup language) for creating a static website. It supports all kinds of file formats and is good for building a blog quickly.  

> [Tom Preston-Werner](http://tom.preston-werner.com/), GitHub's co-founder, wrote Jekyll in Ruby in the year 2009.

Though it needs some technical background and a good acquaintance of [Markdown](https://www.markdownguide.org/getting-started) and the [Liquid](https://shopify.github.io/liquid/) templating language, which are easy to learn if you have some elementary knowledge of HTML. The popularity of Jekyll could be seen on [Showcase](https://jekyllrb.com/showcase/) and [wiki](https://github.com/jekyll/jekyll/wiki/sites).


[Jekyll](https://jekyllrb.com/) is preferred because of the following reasons.

1. **Performance:** Jekyll is tremendously fast because static files are returned by the web server.

2. **Secure:**  As content is static files which makes it more secure until someone hacked the server.

3. **Less expensive:** It requires fewer resources which cuts its operative cost.

4. **Easy to learn:** Basic knowledge of HTML, CSS, and JavaScript is suffice for learning [Liquid](https://shopify.github.io/liquid/) which is a templating language.

5. **Low maintenance:** It takes less than five minutes for setting up Jekyll and the maintaining cost is minimum because of superb support for Markdown, and the Liquid templating language, making a blog is as easy as running two commands.

6. **Big community:** Jekyll has an immense active community as well as a team of Core maintainers which is working hard to maintain and document Jekyll very well.

7. **New Learning Experience:** Blogging is the best way to learn and share new skills in terms of technology. We learn more by teaching others and while getting your hands dirty with real-world problems.




### TL;DR Five steps for creating a Jekyll blog:
---
1. Install [Jekyll](https://jekyllrb.com/docs/installation/).
2. Download the [theme](https://github.com/mmistakes/minimal-mistakes).
3. Modify the **Gemfile**.
4. Modify the **_config.yml** file.
5. Build the site and run the server.

---

The above steps are explained below in details.


### Installing Jekyll ###

First Install [Jekyll on windows](https://jekyllrb.com/docs/installation/windows/)
(other OS installation procedures could be found on Jekyll website).

<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/1_Jekyll.png" alt="Jekyll for windows">
  <figcaption>Jekyll for windows</figcaption>
</figure>

According to the Jekyll official [documentation](https://jekyllrb.com/docs/installation/windows/): The easiest method to run Jekyll is by using the [RubyInstaller](https://rubyinstaller.org/) for Windows.
<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/2_Ruby_installation.png" alt="Ruby installation">
  <figcaption>Ruby for windows</figcaption>
</figure>

Jekyll is a [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems). The best explanation is found on [stackoverflow](https://stackoverflow.com/questions/5233924/what-is-a-ruby-gem)  as:
> Gem is a package manager for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries, a tool designed to easily manage the installation of gems, and a server for distributing them.



### Download the theme ###

The minimal mistake [theme](https://github.com/mmistakes/minimal-mistakes) is used on this blog because of its simplicity and elegance. This theme is very well [documented](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) by its creator Michael Rose.
Download the theme directly from the [link](https://github.com/mmistakes/minimal-mistakes) above and save it.
Another way is just by typing the following command on [Git bash](https://git-scm.com/download/win):

 ```
 $ git clone https://github.com/mmistakes/minimal-mistakes
```
<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/3_Git.png" alt="Git">
  <figcaption>Downloading minimal mistake theme with Git bash</figcaption>
</figure>

Change into the minimal-mistake directory and install Bundler.

 ```
$ cd minimal-mistakes/
$ bundle install
 ```

<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/4_Bundle_install.png" alt="Install Bundle with the command">
  <figcaption>Installing Bundle with Git bash</figcaption>
</figure>

> Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.


### Build the site  ###

Build the site and make it available on a local server.

```
$ bundle exec jekyll serve
```

<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/5_Build_the_site.png" alt="Build the Jekyll site by simple command">
  <figcaption>Build the Jekyll site </figcaption>
</figure>

Browse to http://localhost:4000 to see your site.

<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/6_Localhost_site.png" alt="Jekyll site">
  <figcaption>Jekyll site on local host </figcaption>
</figure>


### Modify the  **Gemfile** ###

Copy paste the following code to the **Gemfile**
```
source 'https://rubygems.org'
gem "minimal-mistakes-jekyll"
gem 'jekyll-include-cache'
gem 'jekyll-archives'

```

### Modify the **_config.yml** file ###

In the config.yml file, some modifications are to be done.

Search plugins section (at line 225) and add the following line  
```
- jekyll-archives
```
The final plugins will appear as follows:

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

Uncomment the jekyll-archives (at line 254) till the tag section (the line 263). The final Jekyll-archives will appear as follows:

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

Add the following lines at the defaults section (starting at line 287)
```
# _pages
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: true
```

The final defaults section will appear as follows:

```
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments:  true
      share: true
      related: true
  # _pages
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: true
```


In Site Settings, title(at line 19), name(at line 21), and description(at line 22) could be changed according to the requirements.
Activate breadcrumbs (at line 27) by making it true as follows:

```
breadcrumbs              : true # true, false (default)
```


In the Site Author section, author name (at line 106), bio (at line 108), location (at line 109), links (line 111 onwards) to email, twitter, facebook etc could be changed according to the requirements.



### Build the site  ###

Build the site and make it available on a local server

```
$ bundle exec jekyll serve
```

<figure>
  <img src="/assets/images/2018-11-29-Create Jekyll blog in five steps/5_Build_the_site.png" alt="Build the Jekyll site by simple command">
  <figcaption>Build the Jekyll site </figcaption>
</figure>

Now browse to http://localhost:4000 to see your site.


## Conclusion ##

We have learned about Jekyll, its various advantages over other blogging systems. We have also seen how to make a Jekyll blog. It is a very powerful tool which is widespread for blogging and creating a website. It is getting lots of attention which opens new ways to make a website faster and secure.


---
### <ins> References and further reading list </ins>

1. [Jekyll](https://jekyllrb.com/)
2. [Wiki](https://github.com/jekyll/jekyll/wiki/sites)
3. [Showcase](https://jekyllrb.com/showcase/)
4. [RubyInstaller](https://rubyinstaller.org/)
4. [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems)
