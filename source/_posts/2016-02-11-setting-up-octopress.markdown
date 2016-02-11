---
layout: post
title: "Setting Up octopress"
date: 2016-02-11 14:38:47 -0500
comments: true
categories: [homelab,documentation,github]
---

* To be updated later to make pretty:

OS: Mac OSX 10.10.3 with Developer Tools installed


sudo gem install bundler
cd ~/git
git clone git://github.com/imathis/octopress.git octopress
cd octopress
bundle install
rake install

rake new_post["Setting Up octopress"]

*Stuff*

rake generate
rake deploy
???
Profit!