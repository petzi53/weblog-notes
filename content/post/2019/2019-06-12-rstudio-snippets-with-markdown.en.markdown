---
title: RStudio Snippets for Markdown
author: Peter Baumgartner
date: '2019-06-12'
slug: rstudio-snippets-for-markdown
categories: [how-to]
tags: [snippet, RStudio]
lastmod: '2019-06-16'
description: 'Code snippets are text macros which you can insert into your programs. They are used for repetitive tasks and can boost your productivity tremendously. After providing some link to tutorials about RStudio snippets, I am going to summarize eight reminders for practical usage.'
disable_comments: no
draft: no
---

## Tutorial for RStudio code snippets

Code snippets are text macros which you can insert into your programs. They are used for repetitive tasks and can boost your productivity tremendously. Here I am not going to explain how to use it. There are already several good tutorials around:

+ The official [RStudio tutorial](https://support.rstudio.com/hc/en-us/articles/204463668-Code-Snippets) on code snippets
+ A [Blog entry by Jake Daniels](https://datacritics.com/2019/01/28/rstudio-snippets/): How RStudio Snippets Improve My Productivity
+ A [Blog entry by Jozef Hajnala](https://jozef.io/r906-rstudio-snippets/): 4 ways to be more efficient using RStudio's Code Snippets, with 11 ready to use examples
+ A [Video by Sharon Machlis](https://www.youtube.com/watch?v=h_i__VTSurU&list=PL7D2RMSmRO9JOvPC1gbA8Mc3azvSfm8Vv&index=28&t=141s): R tip: Save time with RStudio code snippets (part of her video channel [Do more with R](https://www.youtube.com/playlist?list=PL7D2RMSmRO9JOvPC1gbA8Mc3azvSfm8Vv))

## Eight useful reminders

In this post, I want to summarize some important details, which I learned laboriously after time-consuming trials:

1. The Markdown section in the snippet editor works only with `.Rmd` and `.Rmarkdown` files. -- So if you are going to write just text (e.g., a blog entry) _and_ you want use RStudio snippets to insert shortcodes than you have to write into `.Rmd` / `.Rmarkdown` files.
2. The snippets in the R section of the snippet editor are for code chunks whereas the snippets in the Markdown section work only in markdown text of `.Rmd` / `.Rmarkdown` files.
3. To insert snippets in the Markdown part of `.Rmd` / `.Rmarkdown` files, you have to use SHIFT-TAB (and not just TAB as for R snippets in the code chunks).
4. To write your snippets, you have to use the TAB key for indenting. 4 Spaces do not work!
5. It is legitimate to write huge snippets for large code junks. For instance, you can write complex `ggplot2` snippets as a kind of a template you are going to use frequently.
6. For large code chunks, it may be preferable to write the snippets with the RStudio code pane. You can load the snippet files under `~/.R/r.snippets` respectively ~`.R/markdown.snippets` into RStudio.
7. You can share you snippets sending these files to your colleagues and collaborators.
8. Do not use names, which are difficult to type to call your snippets. For instance, to insert the markdown syntax for an image do not name it "![" but "ii" for example.


<span class='Z3988' title='url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=blogPost&amp;rft.title=RStudio%20Snippets%20for%20Markdown%20%3A%3A%20Open%20Science%20Education&amp;rft.source=RStudio%20Snippets%20for%20Markdown&amp;rft.rights=CC%20BY-SA%204.0&amp;rft.description=Code%20snippets%20are%20text%20macros%20which%20you%20can%20insert%20into%20your%20programs.%20They%20are%20used%20for%20repetitive%20tasks%20and%20can%20boost%20your%20productivity%20tremendously.%20After%20providing%20some%20link%20to%20tutorials%20about%20RStudio%20snippets%2C%20I%20am%20going%20to%20summarize%20eight%20reminders%20for%20practical%20usage.&amp;rft.identifier=https%3A%2F%2Fnotes.peter-baumgartner.net%2F2019%2F06%2F12%2Frstudio-snippets-for-markdown%2F&amp;rft.aufirst=Peter&amp;rft.aulast=Baumgartner&amp;rft.au=Peter%20Baumgartner&amp;rft.date=2019-06-07&amp;rft.language=EN'></span>

