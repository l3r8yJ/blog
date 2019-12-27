---
layout: post
title: "Talented Programmers, Who Are They?"
date: 2019-12-30
place: Moscow, Russia
tags: management
description: |
  Talent is a rare thing in every profession:
  we don't tolerate the lack of it in music,
  but we keep losing it in programming, unfortunately.
keywords:
  - talent for programming
  - talented programmers
  - programming talent
  - how talented are you
  - talent
image: /images/2019/12/
jb_picture:
  caption: ...
---

Talented programmers---who are they? I'm not talking about those who are
famous, well-paid, or the authors of big and popular products.
They are not necessarily talented, even though their _results_ are outstanding.
Talent is something some of us have as God's gift.
Very few of us... otherwise it would not be called a talent.
We all know how talent looks in music, sport,
poetry, or the art of acting. We can tell right off the bat who's got it and
who is faking it, no matter how hard they try.
Can we do the same after a short interview of a programmer? I believe, we can.

<!--more-->

{% jb_picture_body %}

I decided to read what others are saying about the art of interviewing and
how they suggest detecting the talent amoung all other regular
software writers.
[Jeff Attwood](https://blog.codinghorror.com/on-interviewing-programmers/)
suggests paying attention to person's passion, communication skills,
personal attitude, and the ability to work in the team.
[Joel Spolsky](https://www.joelonsoftware.com/2006/10/25/the-guerrilla-guide-to-interviewing-version-30/)
suggests hiring those who are smart and can get things done.
[Haoyi](http://www.lihaoyi.com/post/HowtoconductagoodProgrammingInterview.html)
gives very detailed instructions for the interviewer with the focus
on the candidate's ability to write code, discuss problems, reason
about constraints, and be a person we would enjoy working with.

All of these make sense, but it's not about talent.
It's about finding a person who can effectively write and maintain
spaghetti code and be _happy_ about it (maybe with just a little
dose of anti-depressants).

Imagine yourself recruting a yet another singer to the choir, which consists
of people who have no ear for music. Would you need a talent? I doubt a talent
would be able to sing. Well, maybe for a while, if you pay well enough. Just like any
other team in any other industry, most software groups
consist of _average_ code writers, not talents. Modern programming, especially in big
projects, is not about talented individuals, it's about team work of mediocre
coders. That's why all interview gurus teach us how to find a yet
another coder: a properly educated, trained, skilled, and ready
to write yet another pack of Spring controllers. And, of course, enjoy it.

Not sing. No.

So, what exactly is talent?

It's an innate need to _structure_ things.

Just like a musician, a talented programmer _physically_ can't tolerate
what _sounds_ wrong: ambiguity, inconsistency, chaos, irrationality, and
lack of logic. A talented programmer _feels_ these things, while a mediocre
one says "Whatever works!" and get on with it.

Let me explain by example. Over the last five years I've been using the same
[simple piece of Java code](https://github.com/yegor256/quiz/blob/master/Parser.java)
to interview everybody who is interested in working with me.
I ask them to review it and find what's wrong. Try it now. You have five minutes.

How many issues did you find? Here are the
[answers](https://github.com/yegor256/quiz/wiki/java-answers). There is
a prioritized list of defects I expect candidates to find. The most important
are at the top---they are about _structural_ problems in the code. Mediocre
developers are used to work with bad code and can easily put up with it.
The class name is `Parser`, but it has `get` and `save` methods? Who cares,
as long as it works! The pair of methods is not `get` and `set`, but `get` and ...
all of a sudden `save`? Who cares, it works anyway! And so on. Mediocre
programmers don't feel _annoyed_ when they meet inconsistencies. Just like
people with no ear for music, they _don't hear_ anything wrong!

When I interview programmers, I don't pay attention to how much they know
about Java, how well they understand OOP, or how many projects they've
managed to complete up to date. And, of course, I don't care
how potentially likeable they are. Instead, I pay attention to how much they _hate_
to see what doesn't look right. I check how _intolerant to chaos_ they are.
This is what my Java test is for.

To be honest, very few of them expose these qualities.

Because very few projects (and project managers) need these qualities.
Most processes and source code bases are poorly structured.
Any honest attempts to intollerate them and introduce some discipline
only annoy mediocre programmers, who are always in the majority.
A talented programmer constantly demanding discipline and
consistency looks like a crazy
[OCD patient](https://en.wikipedia.org/wiki/Obsessive%E2%80%93compulsive_disorder).
Nobody understands what's wrong and ignore him/her, at best.
Moreover, bad coding practices are coming from popular frameworks
and poor management principles are encouraged by Agile and its coaches.
They trains us to have no ear for high quality in programming.

Market's demand now is mediocrity, not talent.

Thus, don't worry if you feel that you've got not so much of
a talent---in most projects you will be much better off without it.