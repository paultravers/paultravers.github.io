---
layout: post
title: Moving from Octopress to Jekyll
date: 2024-03-12 05:44 +0000
categories:
 - jekyll
 - octopress
 - ruby
 - github
 - github-pages
---

# Migrating to Jekyll from Octopress
This was a long and painful process but ultimately (hopefully) worthwhile

## Setting up a new Jekyll Site
The first order of business was to setup a Jekyll site. I initially tried on my Windows 10 laptop, but this ultimately proved pointless as ruby gems don't seem to want to play nice with Windows (especially some of the more exotic ones that I seemed to need)

I eventually ended up setting up an environment on my ubuntu VM with RVM, Ruby 2.7, and using bundle install to add all of the gems needed (the apt managed packages just seemed to break everything)

After getting a test site up and running locally my first order of business was to copy my previous octopress pages to the new jekyll site. This too proved difficult as I did not have the source markdown code for those posts. I was able to find a ruby file to import the html and generate posts that worked for Jekyll

https://stackoverflow.com/questions/15770341/working-on-an-octopress-blog-from-a-new-computer-without-source-branch

https://gist.github.com/pezholio/5299018

ruby import.rb /path/to/octopress/blog

Moving these files to the new \_posts directory and then testing jekyll again locally to make sure everything worked.

After everything tested OK locally I was ready to commit all of my changes. I was surprised to see the website didn't immediately update but then realized that there was a Github Action on the backend that was actually used to deploy the site. And here we are. I know it's not pretty but it's nice to be able to update a personal site and track my progress as I grow.
