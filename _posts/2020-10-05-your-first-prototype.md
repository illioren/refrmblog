---
title: Your first prototype
layout: post
author: Tim
date: '2020-10-05 07:00:00'
category:
- refframe
- journey
- first prototype
summary: Concretely, what is a first prototype?
thumbnail: "/assets/img/posts/your-first-prototype/thumbnail.png"
hero: "/assets/img/posts/your-first-prototype/post_hero.png"
---

# Your first prototype



Today, I would like to talk about the notion of "First Prototype" and why I struggled with it.

When taking on this project, I set up to show what I was doing was, firstly, possible, and, secondly, a good idea. Not only to myself but also to my PhD supervisor and, at the time, partner.

This was also the time when I finally thought "it might be a good idea to learn how starting a business is done". Never too late to start asking the obvious, right? I was often been told that "all you need is a prototype", that "it should be fast, just slam it together" and that "it does not really need to work".

At the time of this writing, I have been working on this project for almost 6 years and, thankfully, I did not take me this long to produce a "prototype". The very first version was completed in less than 3 months of (very) part-time ML prototyping followed by 2 weeks of solid coding over the 2015 Christmas break.

## "Just put it online!"

So why did I not use this prototype? Well, I did not know how to be perfectly honest. Showing it to people is one thing, but I -rightfully so- doubted my ability to deliver something usable within the next 6 months to leverage their interest (following the advice that "you need to move fast, fast, fast..." - but this is another topic). 

When asking around, I was mostly told: "You have a prototype? You just need to put it online". While this is legitimate advice -I, indeed need to find an audience and make it known that I am doing something- there is more to this action than most people seem to believe. If you ask me, this advice is partly driven by a lack of insight around two key aspects:

  - <ins>Technical ignorance</ins>: of course, not all people are tech-savvy, and there is a multitude of ways to put something online. For a forum-like application written in PHP -for instance- a lot of "ready-to-fire" solutions exist out there that would enable you to do that in less than 5mn. For a custom software that tries to walk outside the mainstream path, this can become involved very quickly. In my case, "Just put it online", would have been a costly months-long endeavour which result would probably need to eventually be entirety re-worked.
  - <ins>Diverging definitions</ins>: by far the most important, here. In this context, what exactly qualifies as a "prototype"?:
    1. A series of command lines that you have to type to eventually display something and whose sole use if to make a point?
    2. A limping code that sort of works up to a certain point and then requires human intervention for any visualisation to occur? 
    3. A functional package that looks ugly but does the job? 

    Only one of those can indeed be put online without further development time. Well in my case I had something akin to the second definition: a code pipeline that -on my computer- could generate the data needed and embodied the essence of the idea and innovation. The software was not stable at all and sometimes needed multiple restarts to complete a single data transformation epoch. Plus, to produce something visual, it needed human intervention and partial curation of the output. Something like this still constitutes a "prototype" as it shows that the idea and technical approach are sound, but it cannot yet live a life of its own online.

    In retrospect, I think that what most people mean by "prototype" is "a facade that would attract attention". Something, even if static, shows your point and that you can present to investors, or leverage to show interest and market potential. As far as 5-years-younger-me was concerned, this was not even a possibility.

So, was I wrong to not use this barebone creation? Probably. I invested efforts in it and nothing came out. Was it my fault? Totally.

## About Refframe, more particularly:

Regardless of what happened, what I was left at the end of my few months of tickling looked something like this:

- ***First, A forced based co-citation graph showing articles (in red), references (in blue - often radiating in a star-like pattern from the red articles), and academic references (in green - ULR links, book references, etc...).***

  This representation was generated through a graph library (I cannot remember which one, it was a long time ago. Apologies) and saved directly to PDF.

  ![reference_net_subset_scaled](/refrmblog/assets/img/posts/your-first-prototype/reference_net_subset_scaled.png)

- ***Next, a connectogram representation of the same information***
  
  based on a different dataset:
  
  ![reference_net_subset_scaled](/refrmblog/assets/img/posts/your-first-prototype/graph_circle_scaled.png)

- ***Finally, a web UI used akin to the first image of the list here used to display a part of the bibliography of my PhD Thesis:***

  The web UI was lightly interactive, in the sense that you could drag nodes and hover them to display the title of the document.

  ![reference_net_subset_scaled](/refrmblog/assets/img/posts/your-first-prototype/AKMH_graph.png)
  

These graphs already displayed valuable information but were very hard to read, to use, and even harder (and slow) to generate. To be honest, the prototype itself was not too difficult to produce. The involved part(s) were to come later...We are still a long way away from what I timidly showcased in [My previous post](https://illioren.github.io/refrmblog/refframe/journey/2020/09/28/what-is-refframe/)

 
In a later post, I will dig more into what it did and how it worked back then.
