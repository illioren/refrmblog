---
title: The first prototype
layout: post
author: Tim
date: '2020-10-12 07:00:00'
category:
- refframe
- journey
- first prototype
summary: What was Refframe's first prototype.
thumbnail: "/assets/img/posts/2020-10-12-the-first-prototype/thumbnail.png"
hero: "/assets/img/posts/2020-10-12-the-first-prototype/post_hero.png"
---

# "The first prototype: implementation"


In a [previous post](https://illioren.github.io/refrmblog/refframe/journey/first%20prototype/2020/10/05/your-first-prototype/), I talked about the definition of a First Prototype and the divergence of understanding that can arise from it. By one of those definitions, I had my prototype ready in some 3.5 months.

The first version of Refframe was a monolithic application written in Python. In fact, it was not even "an" application, but rather a collection of scripts calling one another: 
  - A script to generate single references from .bib and .bst files and tag the individual parts as being "authors", "title", and "journal" to generate training samples.
  - A script to generate and train an artificial neural network to recognise the different part of a given reference using the training samples generated above
  - A script to open and extract information from a PDF.

    This script was where the "heavy" lifting was happening. It was effectively opening all the `.pdf` files contained within a folder❶ and:
        1. Scanned the first few pages of the file to find the title.
        2. Found out how many columns were present within the document.
        3. Scanned the document backward from the end to find the start reference section.
        4. Extracted the references and attempted to rebuild them if they were spanning over multiple lines before storing them in `.json` files.

  - A script to parse and tag the references using the trained artificial neural network.
  - A script to plot a co-citation graph from the JSON files produces.

 > ❶ If the PDF did not contain any text, an OCR engine ([Tesseract](https://github.com/tesseract-ocr/tesseract)) was kicking in to further attempt a data extraction.

 All this code was essentially acting as a single monolithic program (single process, single thread - except for the reference parsing that was calling on a C based neural network library); the performance of which was then very low, both in term of extraction success rate and was, and as you can guess, of speed. It would often need more than a minute to finalise the data extraction process of a single document. 

Nevertheless, it was "working" and proving my point. With that said, even without considering the numerous stability issues, it was pretty much unusable due to the lack of controls on one hand (all steps were hard codded operations) and the lack of interactivity on the other hand: the result visualisation was stored in a barely readable PDF document and had little value.

Later, I took the time to address this point an added a graphical interface. But this is a topic for a later post.