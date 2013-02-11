---
layout: post
title: "Shorter exception declarations in Ruby"
date: 2013-02-10 19:31
comments: false
categories:
---

<a href="http://steveklabnik.com/">Steve Klabnik</a> recently wrote a <a href="http://blog.steveklabnik.com/posts/2012-09-09-random-ruby-tricks--class-new">post</a> on Class.new, especially as it relates to a terser syntax for declaring Exception classes.

I use an even terser, albeit more magical syntax.
<!-- more -->

This is a bit of code that creates a class in ruby, you can find it all over the internet.

``` ruby
def create_class(class_name, superclass, &block)
  klass = Class.new superclass, &block
  Object.const_set class_name.to_s, klass
end
```
Very cool, but I use this only for creating exception classes and so prefer something a bit more explicit. Luckily it is trivial to get what I want from this code.

``` ruby
def new_exception(exception_name)
  klass = Class.new Exception
  Object.const_set exception_name.to_s, klass
end

new_exception "CannotFindPants"
new_exception :FlobbetsAreFlumoxed
```

Viola!

If you wanted to go further, you could modify the code to take multiple arguments, loop through them to create the classes.

