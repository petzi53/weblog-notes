---
title: 'What happened with my English weblog?'
author: Peter Baumgartner
date: '2018-06-27'
slug: what-happened-with-my-english-weblog
tags: ["blogdown","hugo", "weblog"]
categories: ["reflection","how-to"]
description: "Spring 2017, I started to experiment with the static website generator `Hugo` in alliance with the R package `blogdown` to publish weblogs post written in English. I planned to write, but after one year I have to say that it didn't turn out the way I have projected it."
draft: no
---
The <a href="https://bookdown.org/yihui/blogdown/">R package blogdown</a> was developed by Yihui Xie to make writing for the web as easy as possible. At least this is the intention and the theory. 

But `blogdown` is also a very sophisticated tool. It is not only built upon many other technologies but also has built-in a lot of facilities which themselves are using advanced technologies. As long as you keep using just the default options, many of these complexities are hidden. But if you want to use some of the provided nice features -- and I am sure that there will come the time where you want like me to adjust something to your growing needs -- then some difficulties could emerge. At least this happened to me.

<div class="alert alert-info" role="alert">
I have written recently a post <a href="/2019/05/31/blog-writing-barriers-to-overcome/" class="alert-link">"Blog writing barriers to overcome"</a> which addresses these complexities with the negative result that I haven't blogged regularily with this new technical infrastructure.
</div>

## Some observations

+ **Draft:** Starting a new article it is set by default to `draft: true`. This means that to deploy the website with <a href="https://www.netlify.com/">Netlify</a> does not show this article! So I can safely make my commits to <a href="https://github.com/">GitHub</a> until the article is ready for publication. Then I have to set `draft: true` and commit the article to GitHub. I can also withdraw articles by setting `draft: true` again.

<div class="alert alert-danger" role="alert">
**Update 2019-05-31:** The following four paragraphs about _.Rmd files_ and _compiling_ are not correct. It turned out that I didn't understand quite well the interplay blogdown -> Github and Netlify. There is a new post coming on this subject.
</div>
+ **Rmd-File:** I am not sure if there aren't some incompatibilities with my sophisticated theme, especially concerning the creation of new types of pages. But there should be no problem as I can always change the file extension later on. 
        - At the moment, I am not writing about R topics where I would need _.Rmd files_. But this could change very shortly, e.g., when I am writing posts about statistic subjects or using R packages in these posts. 
        - The intermediate HTML files can be cleaned up with the button "Clean All" under the "More" menu using the command `rmarkdown::cleansite()`.

+ **Compiling:** There is a slight difference between using the RStudio addin "Serve Site" using `blogdown:::serve_site()` or the "Build Website" button using `rmarkdown::render_site(encoding = 'UTF-8')`. Whereas `serve_site()` always displays the homepage, remains `render_site()` on the page I am working on.

## Checklist for new blogdown project

1. Immediately after the project is started, create two git branches: `config` and `posts` to prevent that everything is directly committed into the `master` branch.
2. Change to branch config and do the necessary changes in the config.toml

## config.toml

<div class="alert alert-danger" role="alert">
**Update 2019-05-31:** Again there is some confusion until the end of the article. I decided not to delete the wrong parts as these text passages will document my learning experiences. In the upcoming new blog post I will reference these wrong explanations.
</div>
+ Add `title = "<name of website>"`
+ Add `themes = "<name of theme used>"`
+ Add `themesdir= "<path-to-theme>"`
+ Add `ignoreFiles = ["\\.Rmd$", "\\.Rmarkdown$", "_files$", "_cache$"]`
+ Backup your site and run `blogdown::hugo_convert(to = "YAML", unsafe = TRUE)`
+ Set `relativeURLs = true` (default is false) to view your website with the `build_site()` command. If you want to see it in your browser than set "Preview in Window" under the configuration menue in the code pane. You can always view it with the `serve_site()` command (shortcut: CTRL-S) in the viewer pane or on the browser with a click in "Show in a new window" icon, right from the broom icon in the viewer pane.
