---
layout: post
title: "Shorter exception declarations in Ruby"
date: 2013-02-10 19:31
comments: false
categories:
---

<a href="http://steveklabnik.com/">Steve Klabnik</a> recently wrote a <a href="http://blog.steveklabnik.com/posts/2012-09-09-random-ruby-tricks--class-new">post</a> on Class.new, especially as it relates to a terser syntax for declaring Exception classes.

I use an even terser, albeit more magical syntax.

This is a bit of code that creates a class in ruby, you can find it all over the internet.
<script src="https://gist.github.com/3694734.js?file=gistfile1.rb"></script>

Very cool, but I use this only for creating exception classes and so prefer something a bit more explicit. Luckily it is trivial to get what I want from this code.
<script src="https://gist.github.com/3694817.js?file=gistfile1.rb"></script>

Viola!

If you wanted to go further, you could modify the code to take multiple arguments, loop through them to create the classes.



note: blog under construction at the moment, please excuse the brokenness of most of it.
