---
title: Md vs. Rmd vs. Rmarkdown
author: Peter Baumgartner
date: '2019-06-21'
slug: md-rmd-rmarkdown
disable_comments: yes
draft: yes
---

<span class="upper">read pandoc!</span>

options	     | md  | Rmarkdown | Rmd   | work around
------------ | ----| --------- | ----- | -----------
rendered by  | Blackfriday | Blackfriday | rmarkdown + blogdown + pandoc
compile with save^[when server is down] | yes | no | no | Rmarkdown + Rmd needs "Touch File" when server is running
output       | markdown | markdown | html
intermediary files | no | yes | yes‚
numbered table, figures |
crossreferences

bibliography | no  | no        | yes   | See [help](https://notes.peter-baumgartner.net/)-file
run r code	 | no  | yes       | yes   | md: r code with fenced code chunk, but not executed 
task list	 | yes | yes       | no
mathjax	     | no  | no        | yes   | md: inline math expressions in a pair of backticks (CHECK!), Xaringan + JavaScript
html widgets | no  | no	       | yes   |
hugo toc     | yes | yes       | no    |
snippets     | no  | yes       | yes   |
shortcodes   | yes | yes       | no    |
rel, relref  | yes | yes       | no    |
emoj




There is a nice table, which I should include and add my own stuff to it.
https://github.com/rstudio/blogdown/issues/358#issuecomment-465821489

But see also 

+ [Tests in md file]({{< ref "2019-06-10-md-file-test" >}})
+ Tests in Rmd file
+ Tests in Rmarkdown file

***

Whenever I change a Rmd or Rmarkdown file and cannot see the changes, try the following procedure:

1. Call the menu "Clean All"
2. Restart R
3. Restart the server
4. AND touch the file (or type something in it) to change the date of the last modification!
