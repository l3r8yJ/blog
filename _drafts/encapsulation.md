---
layout: post
title: "New Metric: the Distance of Coupling"
date: 2020-10-20
place: Moscow, Russia
tags: oop
description: |
  Encapsulation is a great idea, which doesn't work in practice;
  measuring the coupling distance between objects seems to be
  a better alternative.
keywords:
  - coupling
  - java coupling
  - coupling distance
  - distance between objects
  - java coupling distance
image: /images/2020/10/
jb_picture:
  caption: ...
---

[Encapsulation](https://en.wikipedia.org/wiki/Encapsulation_%28computer_programming%29),
as you know, is one of the
[four key principles](https://www.indeed.com/career-advice/career-development/what-is-object-oriented-programming)
in [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming).
Encapsulation, according to [Grady Booch et al.](https://amzn.to/3o7RnDZ),
is "the process of hiding all the secrets of an object
that do not contribute to its essential characteristics."
Practically speaking, it's about those `private`
attributes we use in Java and C++: they are not visible to the users of
our objects, that's why can't be modified or even read.
Booch et al. believe that the purpose of encapsulation is
"to provide explicit barriers among different abstractions,"
which leads to "a clear separation of concerns."
However, does it really work as planned? Do we really have
explicit barriers between objects? Let's see.

<!--more-->

{% jb_picture_body %}

First, I'm not the first and not the only one asking this question.
[David West](http://amzn.to/266oJr4) much earlier said that "in most ways,
encapsulation is a discipline more than a real barrier," and
that "seldom is the integrity of an object protected in any absolute sense".
In practice, "it is up to the user of an object to respect that object's encapsulation.''
Indeed, let's take a look at the class `Temperature` from my blog post
about [naked data]({% pst 2016/nov/2016-11-21-naked-data %}):

{% highlight java %}
class Temperature {
  private int t;
  public int getT() { return this.t; }
  public void setT(int t) { this.t = t; }
}
{% endhighlight %}

Can we say that the attribute `t` is truly _encapsulated_?
Technically, it is: it's impossible
to modify it directly via the dot notation.
Simply put, we can't do this:

{% highlight java %}
Temperature x = new Temperature();
x.t = 10;
{% endhighlight %}

And we can't even do this:

{% highlight java %}
int y = x.t;
{% endhighlight %}

However, we can do exactly the same via the
[getter]({% pst 2014/sep/2014-09-16-getters-and-setters-are-evil %}) `getT()`
and the setter `setT()`.
Thus, the designer of the class `Temperature` gives us an ability to access
its attribute, but indirectly, through
[getters and setters]({% pst 2014/sep/2014-09-16-getters-and-setters-are-evil %}).
I would say
that the principle of encapsulation is being violated here, and, I'm sure,
[Allen Holub](https://www.infoworld.com/article/2072302/more-on-getters-and-setters.html)
would agree with me. What is the solution? The [article]({% pst 2016/nov/2016-11-21-naked-data %})
about naked data
proposed to utilize the [TellDontAsk principle](http://media.pragprog.com/articles/jan_03_enbug.pdf)
and get rid of the getter:

{% highlight java %}
class Temperature {
  private int t;
  public String toString() {
    return String.format("%d F", this.t);
  }
}
{% endhighlight %}

Now the class `Temperature` doesn't allow us to read its attribute `t`.
Instead, we can only _tell_ it to prepare a string presentation of the temperature
and return back to us. Maybe not exacly a classic example of the "tell" paradigm,
since some data is coming back, but now it looks much better than before. The beauty
of this refactoring is less [coupling]({% pst 2018/sep/2018-09-18-fear-of-coupling %})
between the client and the object. With
the getter (or a direct access to the attribute via dot notation), the client
was able to retrieve the numeric value of the temperature and recalculate it
to Farenheit, assuming that it was in Celcius. With the `String` being
returned the client would not do this. It will only use the string as a final
product, not modifiable. Or maybe not?

What if the client would do this:

{% highlight java %}
Temperature x = new Temperature();
String txt = x.toString();
String[] parts = txt.split(" ");
int t = Integer.parseInt(parts[0]);
{% endhighlight %}

How does it look? Isn't it a violation of encapsulation?
The result of `toString()` is treated
not as it is supposed to be treated. Not as a solid string, but a data with
some internal structure, which is _known_ to the client. The _knowledge_ the
client posseses about the output is the key problem here. The client knows too
much and uses this knowledge for its own benefit: to deconstruct the
data and manipulate the result.

Can we really prohibit the client from doing this? There is no such feature
in any programming language, to my knowlege. When the output of the method
is delivered to the client, the client is allowed to do whatever is needed
with it. This is what is the lack of respect to encapsulation, if I correctly
understood Dr. West. And we are not even discussing
[Reflection API](https://docs.oracle.com/javase/tutorial/reflect/), which
would allow us to take the `t` out of `Temperature` without even calling any methods.

Thus, encapsulation is _not_ an explicit barrier. It exists for as long as we have
a desire to respect it. If we don't, nothing can stop us from abusing an
object in any way we want. And even `private` attribute modifiers won't help.
Moverover, they will only create an illustion of encapsulation, while in reality
everyone is able to do whatever they feel like suitable for their business case.

I have an proposal, though, which may help us make
encapsulation more explicit.

What if we would have an ability to control what's happening with the data
and objects _after_ we return them to clients? What if we would disallow the client
to `split()` the output of the `toString()` method? We can't do this at compile time, I guess,
by going through all the code and checking how _far_ are the moments of interation with our
objects from the places where they were returned. In the example above,
the _distance_ is two: 1) first, we do the `split`, 2) second, we do the `parseInt()`.
Larger applications will have bigger numbers, of course.

It seems that we can use this distance number as a metric of coupling between objects
in the entire app. The larger the number (or the mean of all numbers), the
worse is the design: in good design we are not supposed to take something
out of a method and then do some complex processing. We are supposed, according to
the TellDontAsk principle mentioned above, let our objects do the work and only
return a quick summary of it. The distance metric will tell us exactly that:
how many times and how much we violated the principle of loose coupling.

Would you be interested in creating such an analyzer for, say, Java code?
