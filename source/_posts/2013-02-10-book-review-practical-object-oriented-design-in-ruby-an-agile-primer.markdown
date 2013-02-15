---
layout: post
title: "Book Review: Practical Object-Oriented Design in Ruby: An Agile Primer"
date: 2013-02-10 21:08
comments: true
categories:
---
Although I am fairly well acquainted with the principles of Object-Oriented Design(OOD), I still yearn for a book on the subject that is great for beginner and intermediate developers, a book that is considered the final word in Object-Oriented Design. <!-- more --> Such a book should be:

* Definitive - The book should cover a wide variety of topics.
* Deep - As well as covering a wide variety of subjects, a shallow treatment is just not good enough.
* Prescriptive - The book should have practical rules to follow.
* Easy to read - Some books introduce revolutionary ideas, but are hard to get through. I would classify {{ "0321125215" |amazon_link }} as not easy to read, conversely {{ "0321146530" |amazon_link }} is a great read.
* Reasoned - It should provide insight into the author's reasoning, {{"0735619670" | amazon_link }} is a great example of this.
* Have examples - There are many design books out there that don't have any code. These books can be helpful, but applying the advice within can be difficult.

{{ "0321721330" | amazon_link }}(POODR) by Sandi Metz is not that book. It does however, come closer than most other books on the subject.

A quick look at the table of contents confirms it covers the important bits:

1. Object-Oriented Design
2. Designing Classes with a Single Responsibility
3. Managing Dependencies
4. Creating Flexible Interfaces
5. Reducing Costs with Duck Typing
6. Acquiring Behavior Through Inheritance
7. Sharing Role Behavior with Modules
8. Combining Objects with Composition
9. Designing Cost-Effective Tests

Do these bits live up to the ideals I outlined above?

The first chapter gives a general overview of OOD, but as pointed out by Metz in the "How to Read This Book", people with experience can skip this chapter. I advise you to take her advice, as it is the weakest of the set. In general though, each chapter in the book is better than the last. The chapter on Managing Dependencies has similar problems to other books covering the subject in that it advises people to inject dependencies, but does not adequately discuss the effects on the injecting classes. If a class has all it's dependencies injected, then it is the calling classes responsibility to know about those dependencies. This is not always optimal and POODR does not properly discuss this issue and the solutions to it.

The next few chapters do their subjects justice and, thanks to Metz's casual and engaging writing style, have the best argument against prolific inheritance I have ever read. This is why I consider POODR to be an excellent generic OOD book, it takes all the books, blogs and arguments that have been published and summarises them perfectly. While the treatement is not deep, I don't think much more needs to be said about inheritance than is mentioned in POODR.

Each chapter is well reasoned, there were a few points when reading the book that the code was not particularly well designed, only to read a paragraph later that this is deliberate in order to demonstrate a point. By using tricks like this, Metz gives good insights into her design process and the reasoning behind her designs.

A special mention must be made of chapter 9. Again, the summary of the Chicago verses London schools of testing (for those not familiar with the terms, these are the mockist verses non-mockist styles of Test Driven Development) is concisely summarised. The main disadvantage of mockist testing is that the classes being mocked can be changed without the tests failing. Metz introduces a simple solution that blew my mind. This solution may not be new, but it was certainly new to me. This is exactly why I have been looking for the definitive OOD book, because there is a vast amount of knowlege out there and despite my best efforts I haven't been able to read it all. POODR is almost a one stop book for OOD, especially for Ruby.

Back to my ideal OOD book, POODR is an entertaining and easy read, it fully lives up to tha requirement. It is not definitive, despite covering a good variety of subjects, there are gaps in the material. Metz's examples are perhaps too repeditive for me, but I won't hold that against the book. It is prescriptive, giving specific tips and rules. Despite wanting depth in my perfect OOD book, I didn't find myself needing more explanation in this book, as the concepts were explained so concisely.

So, should you buy the book? Yes is the easy answer for me. At the moment, it represents the best general OOD book on the market, let alone for Ruby and almost all developers will get something out of the book. If you are disheartened by the first few chapters don't worry, you will not be dissapointed by the end.
