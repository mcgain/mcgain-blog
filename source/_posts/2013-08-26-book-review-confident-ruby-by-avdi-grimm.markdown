---
layout: post
title: "Book Review: Confident Ruby by Avdi Grimm"
date: 2013-08-26 12:36
comments: false
categories:
---

Sometimes, the metaphors of and the analogies to, the act of programming are as important and insightful as any technical tip. Many books concern themselves with only these stories, best among them [The Pragmatic Programmer](http://www.amazon.com/gp/product/020161622X/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=020161622X&linkCode=as2&tag=richardmcgain-20) and [Practices of an Agile Developer](http://www.amazon.com/gp/product/097451408X/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=097451408X&linkCode=as2&tag=richardmcgain-20). Although [Confident Ruby](http://devblog.avdi.org/2013/08/26/confident-ruby-is-finished/) is not one of these books, Avdi Grimm opens with a particularly nice one. He compares reading code and reading a choose your own adventure novel, arguing that many methods read like one of these branching story novels, read from front to back, instead of following the correct route. It is the power of these stories that sometimes illuminate a problem far better than just looking at some messy code and this one nicely illustrates the problem Grimm tackles in his book.

Grimm's point then, is that code should read like a narrative. The rest of the book is dedicated to techniques to make code flow better.

This is not a new idea, the single level of abstraction rule has this goal and it has been discussed at length [Clean Code](http://www.amazon.com/gp/product/0132350882/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=0132350882&linkCode=as2&tag=richardmcgain-20) but Grimm tackes this problem with practical, in-depth examples, something has other books often avoid. The book does give you high level strategies for achieving flow, but also practical examples on how to implement them.

Grimm's main strategy to making methods flow, is to separate out the acts of collecting input, performing work, delivering output and handling failures. Once this is done, different techniques are used on the different areas of the method, and so the main portion of the book is split into sections covering these acts.

A good insight into the type of techniques that are discussed in the book is that implementing the various to_a, to_s conversion functions gives code a huge amount of flexibility. File.open for example, calls to_path and to_s on its argument so you don't just have to pass in a string, but anything that responds to to_s. I can easily imagine adding extra information to a Filename class, but being able to pass it directly into File.open without worrying about passing a different type. Grimm recommends that we should all be accepting input in this way so that unforeseen uses of our code is easier. This is typical of the examples in the book, an easy tip to implementm but backed by some deep thinking.

Some tips along similar lines peppered across the internet bring up some very obscure ruby internals. RubyTapas are a prime example here. Although Grimm clearly doesn't intend many of the weird and wonderful code he presents to be used, I thought there might be a danger of some of this obscurity seeping into the book.
Happily, all the examples in the final product are fine, even if the user has never seen the technique before. Using the block form of fetch for example:

    args = {a: 1, b: 2}
    args.fetch(:c) { 3 }

Even if you have never seen this pattern before, I can think of only two things it could be doing, some kind of processing on the value, or a default value. Inspecting the block makes it pretty obvious that it is the latter.


I like the informal tone used throughout, it helps to convey that this is one developer (Avdi Grimm) conveying his personal tips and tricks. I prefer this style to more prescriptive books as it is a helpful reminder that this is only one person's opinion and not the one true way of programming like many books like to preach.

So, should you buy the book? Yes. Most ruby developers will find something useful in here, especially intermediate developers. Although this book is not designed for beginners, it is probably still worth a read through, as the code is not difficult to understand.

[Confident Ruby is available now](http://devblog.avdi.org/2013/08/26/confident-ruby-is-finished/)
