---
layout: post
title: Moving To Jekyll 
categories:
- blog
---

> New year new resolution. Or for me, new blog.

After a while of using Squarespace as my blog hosting provider (and realised I'm not using it that much), I've finally moved to Jekyll.

You ask for reason ? It's because I'm simplifying my life. Want to write something ? Use Markdown + Github push. Done.

However, as is with everything tech, it's not always that simple.

My original work flow of writing moving my blog is as follows :

+ Find out how to install Jekyll (last time I've checked on Jekyll was 2015)
+ Find a good Jekyll theme
+ Install it on my local computer
+ Modify and push it to Github Pages
+ Apply custom domain
+ Done !

It should not take more than 1-2 hours.
Apparently, it took me about 4 hours, or 2x the time.

It become somewhat like this (I'm using OS X):

+ Install Jekyll using gem
+ Find a good theme and clone it to local
+ Try to build theme, got some package error
+ Try to install needed package, got ruby version error
+ Try to update ruby, using gem --update system. Not working.
+ Spent time Googling stack overflow to look for answers.

Googling "How to update Ruby OS X" brings me to this [Stack Overflow page](http://stackoverflow.com/questions/38194032/how-to-update-ruby-version-2-0-0-to-the-latest-version-in-mac-osx-yosemite). There are several solutions, but what I've found really works for me is using Rubyenv, a environment manager for Ruby like virtualenv is for Python.

And off we go :

+ first install [Homebrew](http://brew.sh) (a super excellent package manager for OS X)
+ install required packages

```bash
brew update
brew install rbenv ruby-build

#add rbenv to bash
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

#choose ruby version
rbenv install --list

#ex. install 2.4.0
rbenv install 2.4.0

#set global
rbenv global 2.4.0

#check
ruby -v
```

All done ! You should be able to update Ruby (and don't have to use `sudo gem update` again...)

If you want to set up a specific Ruby configuration, add a `.ruby-version` to your directory

Once I've installed ruby, it's back to install Jekyll

```bash
gem install Jekyll bundler
```

then go to your Jekyll directory and use 


```bash
bundle exec Jekyll serve
```

Done ! Jekyll has been set up and playing nice with Ruby. Now you can just write and push to Github :)