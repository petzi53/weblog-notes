---
title: 'Up-to-dateness: Books vs. Blogs'
author: Peter Baumgartner
date: '2017-10-05'
slug: up-to-dateness-books-vs-blogs
categories: [publishing]
tags: [blogdown, bookdown]
description: 'Inspired from a blog post by Yihui Xie I present thoughts about the differences between book and blog authors and draw some consequences for the possible future developments of bookdown and blogdown packages.'
draft: yes
---

In his newest blog entry [Different Degrees of Freedom for Bloggers and Book Authors](https://yihui.name/en/2017/10/bloggers-vs-book-authors/) Yihui Xie mentioned my 4-part tutorial on blogdown favorably. I am happy that I didn't make some mistakes where he had to correct me :sweat_smile: , especially as I was stealing his precious time with --  as I see it now --  pretty dumb questions on [Stack Overflow](https://stackoverflow.com/search?q=user:7322615+[blogdown]).

In the blog post Yihui Xie is pondering about different constraints for bloggers and book authors. Cause for his reflection was my decision to demonstrate the installation process of blogdown as easy as possible even if I referred to tools and procedures which may not survive the next few months or e.g. the next version of RStudio. Bloggers have the possibility to exploit actuality by revising and updating the blog entries frequently whereas book authors have to limit themselves to more conservative choices. ^[Actually I believe that there are two different subjects to address: One is the problem of actuality respectively the fact that software/web pages can change/disappear overnight and the different problem of how to explain/teach complicated things to people lacking the necessary background. It is fascinating for me to see how Yihui addresses in his blog both problems alternately: For instance [Different Degrees of Freedom for Bloggers and Book Authors](https://yihui.name/en/2017/10/bloggers-vs-book-authors/) refers to up-to-dateness, [The Minimal Reproducible Example Paradox](https://yihui.name/en/2017/09/the-minimal-reprex-paradox/) refers to the teaching problem. Here in this article I will focus on actuality/up-to-dateness.]

### Different perspectives -- same problems

But this conflict (actuality versus time for a new publication cycle) is exactly the same problem that I am experiencing all the time in writing books on eLearning, educational technologies etc. Yihui -- as a software engineer -- wants that people use his cutting edge products without hassle. I -- as an educationalist -- want people to apply educational technology in an appropriate and innovative teaching setting.  We both have the problem that our practical (hands-on) documentation is outdated very fast. I concede that for me as university professor it is a bit easier: I could hide behind 'theoretical groundbreaking' publications :alien: but with the unintended and negative consequences that abstract thoughts do not have much impact for the target group of practitioners (teachers in my case) :thumbsdown:. 

The solution I came up with was to provide two different types of publications: a book/print version and an accompanying website. But the production process of these two different outputs is complicated and not much supported neither by tools nor by publishers. ^[Maybe there are some exceptions like [O'Reilly](https://www.oreilly.com/) or [CRC Press](https://www.crcpress.com/) who allow an additional free web version in some cases. I have no experiences with this publishers but it would be interesting to learn more about their business model.] This was the era before [bookdown](https://bookdown.org/yihui/bookdown/) and [blogdown](https://bookdown.org/yihui/blogdown/) and this is exactly the reason why I became so interested in these new tools.

### Nasty experiences with the publishing process

To explain my expectation with the future development of bookdown and blogdown I have to report about my personal experiences in publishing books. I will focus on my last two books that I have already written in Latex using the open source editor [LyX](https://www.lyx.org/). Both books [Schaufenster des Lernens](https://www.waxmann.com/waxmann-buecher/?tx_p2waxmann_pi2%5bbuchnr%5d=2643&tx_p2waxmann_pi2%5baction%5d=show) and [Taxonomie von Unterrichtsmethoden](https://www.waxmann.com/waxmann-buecher/?tx_p2waxmann_pi2%5Bbuch%5D=BUC124005&tx_p2waxmann_pi2%5Baction%5D=show&tx_p2waxmann_pi2%5Bcontroller%5D=Buch&cHash=6c279fbf89fb47881e02893c29044337) have a complicated and outstanding layout. The book on ePortfolio patterns (written together with Reinhard Bauer) has a very specialized format of presenting the different use cases drawn from the [pattern community](http://hillside.net/patterns/). Whereas the taxonomy book has a complex interrelated structure with 55 charts, 47 tables and two indices, all linked together.

Except selecting a cover image, proofreading and printing I did _everything_ of the production process myself (from the bastard title to the layout and linked bibliography and index).  But this didn't help to facilitate the publishing process for me. For instance I got all pages with typos marked with pencil from the proof reader as a print output sent via snail mail. And the eBook version is much worse as my own generated PDF. Only the chapter headers are linked in the publisher version. This is for the work with the taxonomy book useless as the references between different categories, concepts, tables and graphs are essential. Not even the literature and indices are linked -- in the meanwhile a standard procedure for eBooks publication. The problem is that the background and experiences of the publisher was focussed on Humanities and they didn't have such 'advanced' requirements before. Okay, this was 5-6 years ago, but I doubt whether the situation has changed essentially.

To counter changing and/or disappearing website links I used a twofold strategey for the previously mentioned books: 

* In the taxonomy book I provided addresses managed by [snipURL](http://snipurl.com/) a link shortener, so that I could change the URLs without affecting the published link addresses. Checking the link address of snipURL today I noticed that the service is not available due to maintenance reason (migrating to a new server), destroying completely my intended strategy :rage:.

* In the ePortfolio book we used [Webcite](http://www.webcitation.org/) to archive the actual referenced webpage. Luckily this strategy still holds but there was a time a couple of years ago, were the future of the Webcite service was insecure and dependent of donations.

### What are my expectations with bookdown and blogdown?

I understand that a smoother book publishing process has essentially to do with the innovativeness of the publisher. ^[This is the reason why we have applied for financial support to design educational courses to change workflows of the Austrian publishers of school books. We are already in the short list and we will have the final hearing on Monday, 9th of October.]

The following list is to understand as my personal dream as a layman in software engineering:

1. I want to have full control of the complete publication process. This includes the book publication and the deployment of the accompanying website. It seems to me that bookdown and blogdown strive for this important goal.

2. I want to have help in the management and distribution of chapters/articles for both outlets. I would like to have just one interface for book and weblog as many parts are referencing each other or they are including even some identical paragraphs. This means that bookdown and blogdown should be work together, maybe with a conditional command which controls the three possibilities of the publication process (publishing for the book, publishing for the blog, publishing for both outlets).

3. In want to have more help in the requirements for the print publication (bookdown). In the new blogdown book there is much information about necessary environment and infrastructure conditions. Similar to chapter 3, 5 and the information in the whole appendix of blogdown I would like to have similar recommendation for bookdown. Questions I am interested in are for example: Which tools to use for designing a cover? What process are important in order to self-publish the book?

### Summary and outlook

Yes, there are different degrees of freedom between blog and book authors (e.g. in the concern of typos), but I believe that this is not the essential distinction in writing tutorials. It has more to do with different perspectives on the published product. There are different but equally demanding obligation for both groups: 

* Books authors _have_ to focus more on abstract concepts which are valid for a longer period whereas bloggers _have_ to provide concrete up-to-date information.
* Book authors _have_ to think about additional methods to provide more accurate information (e.g. accompanying websites) whereas bloggers _have_ the duties to provide new versions of their entries whenever something important has changed. 

In a way this responsibilities of bloggers are more difficult to meet: It means that the blog entry is not a onetime action (like publishing a book) but an ongoing maintenance task. One could say that the task of a blogger is similar to updating software products. Software always requires a responsible maintenance person, who (re)acts when the environment changes (e.g. a new version of the operating system). The person responsible for software maintenance could be different from the original developer. 

I am not sure if this comparison also hold for book authoring and maintaining an accompanying website. I believe that both outlets are only two sides of the same product. Nowadays the book author should also be able to publish and maintain the associated website. I believe that bookdown and blogdown addresses exactly this issue. And I hope that in the future their interplay will provide the necessary functionality to help people like me with the publishing process of book _and_ website in a holistic manner with a unified interface.
