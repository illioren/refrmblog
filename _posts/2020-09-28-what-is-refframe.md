---
title: What is Refframe, concretely?
layout: post
author: Tim
date: '2020-09-28 08:00:00'
category:
- refframe
- journey
summary: An overview of what I am building, in pictures and words.
thumbnail: "/assets/img/posts/what-is-refframe/thumbnail.png"
hero: "/assets/img/posts/what-is-refframe/hero.png"
---

### I am building a search engine

As I have explained in my [First post](./2020-09-21-refframe-and-blogging.md) Refframe is a platform dedicated to the search of academic documents. However, I was eager to offer a different set of tools compared to other search engines **❶**. Not because traditional tools do not work, but because they are not ill adapted: keyword-based search - coupled with page ranking - is sufficient for most common topics, but when it comes to research, some concepts can be specialised enough to require a full sentence (or more) to accurately characterise.

Fortunately, we already invented the symbols that encode those thoughts: *peer-reviewed publications*.

Peer-reviewed publications come with both the description and the relationships relative to a given topic. So why not use this to formulate a search term?

> **❶** *Most search engines that enable screening of scientific content use a 'keyword + filter' approach (taken after web-search engines)*

### I am building a graph interface

The idea of using scientific documents as search terms is at the root of the project. It, however, is only a single facet of an efficient document discovery system. More than formulating the search query, visualising the results should be done efficiently.

This aspect is often left aside and defaults to displaying a paginated list that the user is free to scroll up and down and walk back and forth. But let's be honest here, whoever passes the first page of results? All but the first five entries are likely simply ignored.

But to better grasp the results provided, I wanted to stay away from a tradition list display (although, a list display will also exist, for familiarity's sake).
Graph visualisation enables to seize at a glance the relationship between multiple articles; being similarities, topics and sub subtopics, and other interesting resources.

![imgs](/assets/img/posts/what-is-refframe/unfiltered_graph.png)

### I am building an exploration engine

I find the term "search engine" to be misleading: it hints that it will help you look for something, but in fact, most of them just give you a list of results, without any sense of *why* this result has been given. For hard facts lookup, it does not matter: if you are looking for the date of inauguration of a monument or the year humanity first made it to the moon, the factual results need not suffer any "why"s.

In the context of looking for "relevant" documents, though, it is another story altogether - especially when the document is 30 pages of involved content that will take you anywhere between a few hours to a few days to ingest and understand. I would also argue that, while doing research, we rarely look for "relevant" documents, but more for "***interesting material***" in a given field. And since *interest* is a very subjective metric, just providing hard answers simply doesn't cut it.

I have in mind that while the supposed results should be clearly presented on a dedicated page, they also should be interactive and enable a certain level of interaction - and exploration.

![imgs](/assets/img/posts/what-is-refframe/filtered_graph.png)
