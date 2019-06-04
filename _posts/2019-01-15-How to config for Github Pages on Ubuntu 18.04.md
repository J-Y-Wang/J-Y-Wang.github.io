---
title: 'How to config for Github Pages on Ubuntu 18.04'
date: 2019-01-15
permalink: /posts/2019/01/blog-post-2/
tags:
  - Ubuntu
categories:
  - English
---

Well, I build my Github Pages through my Macbook, and when I would like to maintain it on my Ubuntu 18.04 laptop, the following is a step-by-step tutorial.

**Step 1. Install ruby environment for jekyll**

Use command: `sudo apt-get install ruby2.5-dev`  
You could use Tab after input `ruby2.` for suggestions of latest ruby version with `-dev`  
Input `ruby -v` to check the installation status, and the return is `ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-linux-gnu]` in my case.

**Step 2. Install nodejs for gem of ruby**

First check with `gem -v`, and the return is `2.7.6` in my case.  
If not, use command: `sudo apt-get install nodejs` to install.  
Reinput `gem -v` to check for version.

**Step 3. Install jekyll to run locally**

Use command: `gem install jekyll`  
Unfortunately, my return is:
>Fetching: public_suffix-3.0.3.gem (100%)  
ERROR:  While executing gem ... (Gem::FilePermissionError)  
    You don't have write permissions for the /var/lib/gems/2.5.0 directory.

So it seems we need `sudo`, but when I input `jekyll -v` the return is:
>Command 'jekyll' not found, but can be installed with:
sudo apt install jekyll

Hence I decide to use apt directly. And it worked.
The site will run with the following command:
>`gem install jekyll`  
`jekyll new my-awesome-site`  
`cd my-awesome-site`  
`jekyll serve`
  
Now browse to `http://localhost:4000`.

**Step 4. Install git**

Use command: `sudo apt install git`  
Input `git --version` to check the installation status, and the return is `git version 2.17.1` in my case.

**Step 5. Build your git repo and clone it**

Build your git repo with the name `yourusername.github.io`  
Or you may fork a template and rename it to be `yourusername.github.io`  
Clone it with command:
`git clone https://github.com/yourusername/yourusername.github.io`  
Then run it locally:  
`cd yourusername.github.io`  
`jekyll serve`

It there is warning of dependency of `jekyll-sitemap`, install bundle using `sudo apt install ruby-bundler` or `sudo gem install bundler`  
For error of concurrent-ruby, install using command `sudo gem install concurrent-ruby`, but still not working.  
With the error about `commonmarker 0.17.13`, I struggled for the weekend and tried `sudo apt install gcc g++ make` to install gcc, g++ and make. I don't know which one or ones are the critical elements(which I guess related to Ruby environment, but it worked. By the way, my Ubuntu 18.04 laptop is newly installed.

Woops, another error!  
>An error occurred while installing nokogiri (1.10.1), and Bundler cannot continue.  
Make sure that `gem install nokogiri -v '1.10.1' --source 'https://rubygems.org/'` succeeds before bundling.

But it seems familiar, my best guess is related to Ruby again.  
In the `mkmf.log` file, it says  
`conftest.c:3:10: fatal error: zlib.h: No such file or directory`  
Try to install using `sudo apt install zlib1g-dev`  
After this, my `sudo bundle install` succeed.

Run `bundle exec jekyll build`, but it shown:
>/var/lib/gems/2.5.0/gems/jekyll-3.7.4/lib/jekyll/drops/document_drop.rb:8: warning: already initialized constant Jekyll::Drops::DocumentDrop::NESTED_OBJECT_FIELD_BLACKLIST
/usr/lib/ruby/vendor_ruby/jekyll/drops/document_drop.rb:8: warning: previous definition of NESTED_OBJECT_FIELD_BLACKLIST was here
/var/lib/gems/2.5.0/gems/jekyll-3.7.4/lib/jekyll/drops/drop.rb:8: warning: already initialized constant Jekyll::Drops::Drop::NON_CONTENT_METHODS
/usr/lib/ruby/vendor_ruby/jekyll/drops/drop.rb:8: warning: previous definition of NON_CONTENT_METHODS was here
/usr/lib/ruby/vendor_ruby/jekyll/hooks.rb:56: warning: constant ::Fixnum is deprecated
Configuration file: /home/jywang/j-y-wang.github.io/_config.yml  
jekyll 3.1.6 | Error:  undefined method `really_windows?' for Jekyll::Utils::Platforms:Module

Then try to uninstall jekyll and reinstall jekyll, it works.

**Step6. Push git use the command**

run `git config --global user.email "you@example.com"`

`git add --all`  
`git commit -m "Initial commit"`  
`git push -u origin master`  

There is a detailed [website](http://jmcglone.com/guides/github-pages/) for reference.