---
layout: post
title:  "Teaching MRI and Book"
author: peder
categories: [ education ]
image: assets/images/MRI_logo-retro.png
featured: true
---

For the last 15(!) years I’ve been teaching an introductory MRI course to graduate students, and I struggled to find a textbook that was both rigorous but also accessible to students with a wide variety of coming from backgrounds, including engineering and physics but also biology, chemistry, and neuroscience.  Within the past year I decided to finalize my own textbook, which I am now proud to share as an online and open source (including code for generating figures and plots shown) book:

[Principles of MRI](https://larsonlab.github.io/MRI-education-resources/Introduction.html)

I just finished my first year relying solely on this book, and am writing this to share my justification for creating a new book, my experience using it, and also to encourage feedback.  You can also read my previous post about teaching MRI which includes some similar discussion points [Learning MRI (with lectures too)](../Learning-Principles-of-MRI/).

## Finding a Book Suitable for Engineers, Physicists, Biologists, Chemists, Neuroscientists, and More

The target audience of my course are students in the [UCSF Masters of Science in Biomedical Imaging program](https://radiology.ucsf.edu/education/graduate-programs/msbi-program) that includes a broad range of backgrounds and aims to teach the fundamental principles of biomedical imaging modalities as well as how imaging is used in clinical applications.  The program does not require prerequisites in engineering.  The students come from varied backgrounds including engineering, physics, biology, chemistry, and neuroscience.  They take this coures in their first quarter of the program.

I first taught with [**Principles of MRI** by Dwight Nishimura](https://www.lulu.com/shop/dwight-nishimura/principles-of-magnetic-resonance-imaging/paperback/product-6355103.html?page=1&pageSize=4), the textbook written by my PhD advisor and what I learned MRI from.  It is a great text - concise, consistent, clear, and rigorous - but my non-engineering students struggled.  
In retrospect, I think I took for granted the engineering principles and also the signals and systems perspective that I already had when learning MRI, but many of my students did not have.  However, I leaned heavily on the material from this book when creating my book.

I also tried a few other books that are written for a learners without an engineering background, including [**MRI: From Picture to Proton** by McRobbie, Moore, Prince, and Graves](https://doi.org/10.1017/9781107706958) and [**MRI: The Basics** by Hashemi, Lisanti, and Bradley](https://shop.lww.com/MRI--The-Basics/p/9781496384355).  
These books used lots of intuitive and visual examples to explain MRI concepts, as well as included many example images, which I think resonated with many of my students.
However, I found they lacked the mathematical rigor, including consistency of notation and fundamental signal equations, that I wanted to use when teaching MRI.

## My Book

In [Principles of MRI](https://larsonlab.github.io/MRI-education-resources/Introduction.html), I sought to create a book that was both rigorous and accurate, but also accessible to all of my students.  The Learning Goals are stated in the Introduction, and generally aim towards a practical understanding of MRI such that students can be comfortable and competent running MRI scanners and working with MRI images.

It includes key equations that I found I wanted to use in lectures and homework assignments, but often I have skipped over derivations or in some cases used simplified forms of equations.

I created simulations to illustrate and provide visual examples of concepts.

There are several practical sections, including tables of values and a few example images. 

In the Fall of 2025, I taught solely based on this book, and made a "final" round of edits to fill in any gaps (or eliminate material that was too complex), and now am reasonably confident in this version of the book.


## Online and Open Source

When I first saw the use of the JupyterBook format, I was blow away.  This, to me, is the future of publishing, as it can leverage text, images, simulations, and even interactive content.  I experimented over the past 5 or so years with this format, which formed the basis of this book.  

The code is all there to use as is or modify.  In homeworks, I have asked students to build off of these examples and experiment or make modifications.

The format also allows for community contributions and feedback.  If you use the book, I sincerely hope you will consider using this feature.  
You can message me or leave a GitHub issue with comments, or even create a pull request for content changes you want to suggest. 

## Next Steps

I still have some self doubt about this book.  I wonder if it really was worth it, and whether I should have stuck with, for example, Dwight Nishimura's book, and provided any supplementary materials needed to support this.  I worry I have made errors that will propagate!  But I also really had a lot of fun creating this book, so maybe that in itself makes it worth it.

I am in the midst of the next evolution of the course to include significant demonstrations using the [Ilumr](https://resonint.com/ilumr) tabletop MRI system. You can read about my experience [Tabletop MRI for Education - Teaching Experience](../Tabletop_MRI_Education/), and I aspire to release descriptions of demos I do on this scanner in class that can accompany the book.