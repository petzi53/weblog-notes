---
title: 'Physik Libre:  A bookdown project'
author: Peter Baumgartner
date: '2019-06-05'
categories:
  - case-study
tags:
  - bookdown
disable_comments: no
draft: no
description: 'The article is an interview with Michael Rundel. Michael is a teacher
  at a grammar school in Vienna/Austria and teaches physics, computer science, and
  His project is a practical implementation of cross-media publishing with `bookdown`,
  media design. He talks about his experiences with [bookdown](https://bookdown.org/yihui/bookdown/)
  in writing Physik Libre ( https://physikbuch.schule/), a new textbook on physics.
  which I had described in my [7-part German tutorial](https://peter.baumgartner.name/schlagwort/cmp/)
  on my other blog [Gedankensplitter](https://peter.baumgartner.name). '
slug: physik-libre-a-bookdown-project
toc: no
reading_time: yes
comment_count: yes
---

The article is an interview with Michael Rundel. Michael is a teacher at a grammar school in Vienna/Austria and teaches physics, computer science, and media design. He talks about his experiences with [bookdown](https://bookdown.org/yihui/bookdown/) in writing Physik Libre ( https://physikbuch.schule/), a new textbook on physics. His project is a practical implementation of cross-media publishing with `bookdown`, which I had described in my [7-part German tutorial](https://peter.baumgartner.name/schlagwort/cmp/) on my other blog [Gedankensplitter](https://peter.baumgartner.name). 

## Status of the following interview

This article is an interview with Michael Rundel. Michael is a teacher at a grammar school in Vienna/Austria and teaches physics, computer science, and media design. He talks about his experiences with blogdown in writing Physik Libre ( https://physikbuch.schule/), a new textbook on physics. His project is a practical implementation of cross-media publishing with `bookdown`, which I had described by in my  [7-part German tutorial](https://peter.baumgartner.name/schlagwort/cmp/) on my other blog [Gedankensplitter](https://peter.baumgartner.name). 


{{< figure src="/img/2019-06-04-physik-libre/michael-rundel-min.jpg?classes=border, shadow" class="floatleft"
    alt="Photo of Michael Rundel" title="Michael Rundel (CC-BY Michael Rundel)" >}}

The interview took place two years ago, but I didn't find until now the time to translate it into English and to publish the article in this weblog. I asked the questions in German via email and translated the text with the help of [Google Translate](https://translate.google.com/), [dict.cc], and [thesarus.com]. Where it was useful, I have links provided the first time the concept or software was mentioned. Subsequently, I have these same notions marked as red text. I edited the article with the premium version of [Grammarly](https://www.grammarly.com/). If you are a native English speaker, I would be happy to know about the mistakes in grammar or other language issues. Please use the `Edit Page` button on the top right corner to provide improvement via a pull request to my [GitHub](https://github.com/) repository.

I've gotten to know Michael during one of my talks about the free software environment for statistical computing and graphics R at Danube University Krems. In this talk titled "The many faces of R," I demonstrated to (mostly computer science) teachers the many different use cases of R, driven by special R packages like `bookdown`.  When people wanted to see a practical demonstration for school purposes, Michael came to the front and presented `Physik Libre`. I was delighted not only to have a school-based example but also to find a colleague near my hometown who is also working with `bookdown`.

## Why another physics book?


_**Question:** There are so many physics books why write one more?_

There is already a very long tradition of Open Education Resources (OER) in the US. A couple of years ago I found English free physics books for study and teaching (for example [Physics for K-12](https://cnx.org/contents/MymQBhVV@175.14:VbwW0hKB@13/Why-yet-another-course-in-physics) (Sunil Kumar Singh), [People's Physics Book](http://scipp.ucsc.edu/outreach/index2.html), [CK-12 Physics - Intermediate](https://www.ck12.org/book/CK-12-Physics-Intermediate/), ...). In German-speaking countries, there was something like that not yet. In the meantime, I have found with [Physikunterricht Online](https://physikunterricht-online.de/) an exciting project in the German-speaking area. But in my opinion it does not go far enough: There are more possibilities for interactive usage nowadays. And I want to build the most state-of-the-art physics book available for students. 

We can see many extremely positive developments in recent years: web technologies have matured, projects like [Gitbook](https://www.gitbook.com/) allow you to create documents with minimal effort, we now have a variety of free program tools and [Creative Commons](https://creativecommons.org/) licensed [more than 1.1 billion media available](https://www.oercommons.org/) on different [websites and repositories for educational purposes](https://www.smartcopying.edu.au/open-education/creative-commons/creative-commons-information-pack-for-teachers-and-students/quick-reference-guide-to-finding-creative-commons-material) available , and collaborative platforms like [GitHub](https://github.com/), [GitLab](https://about.gitlab.com/) or `Bitbucket` are no longer used exclusively by programmers.

## Physik Libre as "Proof of Concept"

With `Physik Libre` I want to show what is possible today with the latest technology using the example of a physics book for the secondary school.  It is a proof of concept – if you will. The last few years of Linux have shaped me, I'm afraid. The following points are important to me personally for the implementation of the project:

{{< figure src="/img/2019-06-04-physik-libre/physik-browser-smartphone-min-576x1024.jpg?classes=border, shadow" class="floatright" alt="Page of 'Physik Libre' on a smartphone" title="Page of 'Physik Libre' on a smartphone" >}}

+ Device-independent (Smart TV, PC, notebook, tablet, smartphone, e-book reader, print)
+ Operating system independent (web browser, ePub reader, PDF reader)
+ Free Standards (HTML, JS, CSS, ePub, PDF)
+ Free Licenses (CC-BY-SA 4.0, GPL 2)
+ Free Software supporting online publications like `bookdown`, [GitBook](https://www.gitbook.com/), [R](https://www.r-project.org/), [pandoc](https://pandoc.org/), [LaTeX](https://www.latex-project.org/), [LyX](https://www.lyx.org/),  [Inkscape](https://inkscape.org/), etc.,  sharing all their material on free accessible repositories ([GitHub](https://github.com/) / [Gitlab](https://about.gitlab.com/) / [Bitbucket](https://bitbucket.org/))
+ Free access and respect for privacy (no accounts, no registration, no tracking)
+ Contemporary (full-text search, sharing function, etc.)
multilingual approach.

_**Question:** What was the origin of your idea to write an online book?_

Since my students days in the 1990ties, I have tinkered with web technology. Although I was always impressed what is achievable by combining HTML+JavaScript I never dreamed of the possibility of building full applications like [Google maps]( https://www.google.at/maps) or [tinkercad]( https://www.tinkercad.com/) by using pure web technologies. 

In Austria, the current so-called _digital schoolbook_ of today is a PDF document put on the internet. There is much more possible with today's web technology. **Much** more!

_**Question:** Could you give me a short overview of the historical development and the different phases of your project?_ 

The idea was roughly born three years ago when I was experimenting with the [canvas element]( https://en.wikipedia.org/wiki/Canvas_element), which I was using in my physics applets. This technology helped me to abandon flash applets. Don't get me wrong! – Flash was a neat tool in its time, and I loved working with it. But it always felt like a workaround, and furthermore, it was proprietary software. At that time (2016), I thought there are all building blocks available to realize such a project with pure web technology.

{{< figure src="/img/2019-06-04-physik-libre/cover-physik-libre-min.jpg?classes=border, shadow" class="floatleft"
    alt="Cover of the online physics book 'Physik Libre'" title="Cover of the online physics book 'Physik Libre'" >}}

The following months I learned [SVG] (https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) and `Inkscape`, discovered [Markdown](https://daringfireball.net/projects/markdown/) and the document converter `pandoc`, the version control system [git](https://git-scm.com/) and the `GitBook` project. Summer 2017, I learned about the `R` package `bookdown`. The following school year, I have taught a class of 5th grades of Austrian secondary school (second year of the upper school) in physics. So I decided to start the work on the project.

**Question:** What were your most significant hurdles to overcome in finishing the `Physik Libre` project successfully?? 

The biggest challenge for me was time constraints. I managed to finish the project with sleeping sparsely.

**Question:** Were there some favorable circumstances for the project?



1. First of all: I would have never had a chance to do such a project if there were not such excellent tools like the Linux software and the combined efforts of the Wikimedia community.
2. On the technical side: I studied Mathematics and Physics, but I also have acquired some essential programming skills. This knowledge helped me to glue together some parts in the workflow of the book.
3. And finally on the personal side: First there is the love of my wife and my child. Also, my school principal is so generous as to give me a share of our schools web space for my project.

_**Question:** I noticed that you deliberately do not call your book a textbook. What's the difference between your physics book and a physics textbook?_

A certified textbook always has to be based on the current syllabus and exam regulations. It contains competency-related tasks and guides for teachers. Most of the books websites – at least in the German-speaking countries – are not yet approved by the Ministries of Education. But they play an essential role as a "second opinion." 

In this sense, I understand my physics book project as a "second opinion" for teaching physics to high school students. It tries to explain connections as well as possible – and therefore also with all technically feasible means – for the mathematical level of a high school student.

_**Question:** You have a full teaching commitment and family. How did you come up with the idea to approach such a mammoth project as an individual?_

At the beginning of the project, two considerations were crucial.

1. First, everything - except for the actual writing of the text and the occasional drawing of graphics (where I could not find suitable content on Wikimedia Commons) - should be automated via programs.
2. The second point is not to view the book as my proprietary, but to view it as a collaborative project. All source files of the project should be hosted on a platform like `GitHub` or `GitLab`, thus minimizing the hurdle for other people's participation in the book and encouraging them to participate –even if they find and correct just a spelling mistake.

But real life is quite different!

{{< figure src="/img/2019-06-04-physik-libre/physik-browser-desktop-min.jpg?classes=border, shadow"
    alt="Page of 'Physik Libre' on a desktop computer" title="Page of 'Physik Libre' on a desktop computer" >}}


Concerning the first point: Although there are already many excellent free tools such as `pandoc` and `bookdown` for the generation of documents and final formats, the devil is in the details. For example, many images from [Wikimedia Commons](https://commons.wikimedia.org/wiki/Main_Page), have wrong dots per inch ([DPI](https://en.wikipedia.org/wiki/Dots_per_inch) entries in the metadata. But this piece of information is essential for printing. If I use, for example, an animated gif picture in the web version, a particular frame must be captured and integrated for the print version.

For all such cases, I had to write programs that automate these tasks.

Reflecting on the second point, I mentioned I have to confess there is still a kind of Wild-West mood in the project: Until now I experiment a lot what is feasible. However, this also means that this additional functionality will change the program. Therefore it is challenging to find collaborators when even I do not know what the final features will be. For fruitful cooperation, one needs to establish a common goal with a framework that is the most salient aspects already consolidated.

I taught the fifth grade in physics last year and tried to write the content in the book in parallel with my lesson preparation so that my current students can benefit from my progress as well. So far, I have mostly succeeded, but it is very time-consuming, especially since I am – unfortunately – not a natural-born author.

## Plans with Physik Libre

_**Question:** It sounds that your book is still a work in progress. What are your plans for further developments?_

I have already implemented solutions for most of the technical issues I have encountered. But these program snippets are not very elegant, and there may be a more straightforward answer - after all, I am not a professional programmer.

One problem I am still struggling with is the [same-origin policy](https://en.wikipedia.org/wiki/Same-origin_policy) concept, which limits the embedding of content from other web sites. So far, I have not found a satisfactory solution to this problem.

Besides, much work needs to be done on the documentation before I want to release the project on `Github` or `GitLab.`

_Thank you, Michael, for this interview!_


<span class='Z3988' title='url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=blogPost&amp;rft.title=Physik%20Libre:%20%20A%20bookdown%20project%20::%20Open%20Science%20Education&amp;rft.source=Physik%20Libre:%20%20A%20bookdown%20project&amp;rft.rights=CC%20BY-SA%204.0&amp;rft.description=The%20article%20is%20an%20interview%20with%20Michael%20Rundel.%20Michael%20is%20a%20teacher%20at%20a%20grammar%20school%20in%20Vienna/Austria%20and%20teaches%20physics,%20computer%20science,%20and%20His%20project%20is%20a%20practical%20implementation%20of%20cross-media%20publishing%20with%20%60bookdown%60,%20media%20design.%20He%20talks%20about%20his%20experiences%20with%20[bookdown](https://bookdown.org/yihui/bookdown/)%20in%20writing%20Physik%20Libre%20(%20https://physikbuch.schule/),%20a%20new%20textbook%20on%20physics.%20which%20I%20had%20described%20in%20my%20[7-part%20German%20tutorial](https://peter.baumgartner.name/schlagwort/cmp/)%20on%20my%20other%20blog%20[Gedankensplitter](https://peter.baumgartner.name).%20&amp;rft.identifier=https%3A%2F%2Fnotes.peter-baumgartner.net%2F2019%2F06%2F05%2Fphysik-libre-a-bookdown-project&amp;rft.aufirst=Peter&amp;rft.aulast=Baumgartner&amp;rft.au=Peter%20Baumgartner&amp;rft.date=&amp;rft.language=en'></span>