---
layout: post
title: "Compiling Vim with Ruby"
date: 2013-03-25 10:42
comments: true
categories: vim, linux, ruby
---

A very quick one to document the vim configuration I use

./configure --with-features=HUGE --enable-multibyte=yes --enable-cscope=yes --enable-fontset --enable-rubyinterp --with-ruby-command=/home/mcgain/.rvm/rubies/ruby-1.9.3-p286/bin/ruby

I did hit a stumbling block with my --with-ruby-command=. This needed to be last, as it was slurping up any arguments after it, causing the ruby version check to fail.
