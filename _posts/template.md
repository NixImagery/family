---
layout: post
title:  Title here
date:   2020-01-06 16:00
published: no               # comment this line out to publish
categories: 
# - Education
# - AI and Technology
# - Photography
tags:
    - example
---
{% newthought "Introductory words" %}{% marginnote "notename" "Margin note" %} to the first paragraph.
<!--more-->

* Table of contents
{:toc}

## Side notes
Some words and [a link](//cullaloe.net) more words{% sidenote "notetwo" "side note"%}.

## Images
{% fullwidth "assets/img/rhino.png" "Tufte's pet rhino (via <a href=\"//www.edwardtufte.com/tufte/\">Edward Tufte</a>)" %}

{% maincolumn 'assets/img/rhino.png' 'From Edward Tufte, *Visual Display of Quantitative Information*, page 92' %}

### Margin Figures
{% marginfigure 'mf-id-1' 'assets/img/rhino.png' 'F.J. Cole, “The History of Albrecht Dürer’s Rhinoceros in Zoological Literature,” *Science, Medicine, and History: Essays on the Evolution of Scientific Thought and Medical Practice* (London, 1953), ed. E. Ashworth Underwood, 337-356. From page 71 of Edward Tufte’s *Visual Explanations*.'  %}Images and graphics play an integral role in Tufte’s work.

## Formulas and LaTeX
*When {% m %}a \ne 0{% em %}, there are two solutions to {% m %}ax^2 + bx + c = 0{% em %}*

