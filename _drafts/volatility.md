---
layout: post
title: "Volatility, as a Code Base Metric"
date: 2016-01-25
place: Palo Alto, CA
tags: metrics
description:
  ...
keywords:
  - source code volatility
  - source code metrics
  - stability of code base
  - code base metrics
  - metrics of source code
---

Here is yet another software metric: Volatility. I made it
up a few years go. Let me explain how it's calculated and
what it does. Maybe you find it useful. The goal is to be able
to measure how **volatile** is the source code repository, which
means its . If just a small portion
of files are changed, the repository is more dead than alive.

<!--more-->

This is how I defined it three years ago:
"Volatility is an experimental metric that
shows how big is the difference between actively and rarely changed (dead)
code; it is to prove that a big percentage of dead code is
an indicator of knowledge transfer problems in a project."
Still looks correct. Let's see the math.

First, we collect metrics from Git (or any other SCM), just
by using `git log` and a minimum post-processing of the data. We
need to know how many times every single file was changed. In case
of Git we ay also know how many lines where changed. Say, this is what we get:

{% highlight text %}
file         frequency
----------------------
index.html          87
summary.html       107
logo.png             3
style.css           29
robots.txt           1
{% endhighlight %}

Obviously, we may not have zeros here, since at least once each file was
touched, in order to get into the repo.

Next, we sort the list and replace file names with numbers:

{% highlight text %}
file   frequency
----------------
   0         107  // it was "summary.html"
   1          87
   2          29
   3           3  // and this is "logo.png"
   4           1
{% endhighlight %}

Next, we normalize both file numbers and frequencies:

{% highlight text %}
file   frequency
----------------
0.00       1.000
0.25       0.821
0.50       0.274
0.75       0.028
1.00       0.000
{% endhighlight %}

Make sense so far? Visually, we have something like this:

{% figure /gnuplot/2014/11/hoc-vs-loc.svg 700 %}

On the x-axis we have file positions, normalized to 0..1 scale. On the
y-axis we have frequences of their changes. Most frequently changed
file (`summary.html`) stays on the left and its normalized frequency equals to 1.

That's basically it. All we need to do now is calculate
[mean](https://en.wikipedia.org/wiki/Expected_value) and
[variance](https://en.wikipedia.org/wiki/Variance#Discrete_random_variable) of this
distribution.

\begin{eqnarray}
\mu = \frac{\displaystyle\sum {x \times p(x)}}{\displaystyle\sum p(x)}
\end{eqnarray}

Variance is calculated as:

\begin{eqnarray}
Var(x) = \frac{\displaystyle\sum {|x - \mu|^2 \times p(x)}}{\displaystyle\sum p(x)}
\end{eqnarray}

In our example, &mu; equals to 0.17.

Variance is 0.0346.

The higher the variance, the higher the volatility.
