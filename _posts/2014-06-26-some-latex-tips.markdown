---
layout: post
title:  "Some LaTeX tips"
date:   2014-06-26
comments: true
categories: latex
---

Here are some Latex tips from my previous unsuccessful blog attempt.

## Line spacing in lists

Line spacing in lists can be customized by changing related variable of latex in
list block. For example, for itemize environment, you can change spacing between
items as follows:

{% gist sefakilic/7fc0ea1d4bc04bf6920f list-spacing.tex %}

Change `itemsep` value as you wish. You can do same thing for list and enumerate
environments as well.

## Piecewise function

In LaTex, a piecewise function can be displayed as follows:

{% gist sefakilic/7fc0ea1d4bc04bf6920f piecewise-function.tex %}

The output is

![testing]({{ site.url }}/images/blog/piecewise.png)

## Font sizes

There are 10 different font sizes provided. From smallest to largest one, they
are:

- \tiny
- \scriptsize
- \footnotesize
- \normalsize
- \large
- \Large
- \LARGE
- \huge
- \Huge

Usage: `{\Large This is an example sentence with large font size.}`



