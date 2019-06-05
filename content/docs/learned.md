---
title: Learned
author: Peter Baumgartner
date: '2019-06-04'
categories:
  - collection
  - how-to
  - lessonLearned
  - notes
  - update
tags:
  - addins
  - config
  - rstudio
  - YAML
slug: changes
lastmod: '2019-06-05'
toc: no
disable_comments: yes
draft: yes
---

+ If somethings goes wrong with lines in the  configuration files, YAML header or with a shortcut or other command, Hugo does not necessarily show the problem. But when I restart R and server I will get an error message. **Therefore:** Always check with CMD-SHIFT-10 (restart R) and CTRL-S (start server) if everything is ok!

+ Install RStudio Addins and provide shortcuts: https://rstudio.github.io/rstudio-extensions/rstudio_addins.html and https://www.youtube.com/watch?v=zAtf9NkSOUg

+ `fileListing: yes`: in YAML header is default value. Displays oneliner with title only.

+ `fileListing: no`: or no filelisting parameter in YAML displays title, short description but also categories and tags.

+ the shortcut `%children style="h4" description="true"%` displays title, short description but no categories and tags.

+ `children: yes`: displays just the children shortcut, otherwise you get also at the end of the page a fileListing. 

+ If there are no visible file or folders under a directory (folder), then there is a design problem with the menu.

### YAML front matter
* lastmod: my first Hugotemplate with logic (if then)
* hidden yes/no (for menus)
* draft yes/no with disable_comments yes/no
* children yes/no in combination with fileListing yes/no
* alwaysopen yes/no (for menus)

### RStudio
+ Looking for text in files (in RStudio)
+ Shortcuts for RStudio addins: 
    * Serve Site = CTRL S
    * New Post = CTRL P
    * Update Metadata = CTRL M
    * Insert Image = CTRL I
    
### Updates R, R packages, RStudio, and pandoc

Updates of my many R packages are very often, pratically on a dayly bases.
New versions are coming all 3 moths or so. Here I have written a script that will inform me if there is a new R version available.

    # check if there is a new R version available (for the macOS)
    
    if (rversions::r_release_macos()$version != paste0(R.version$major, ".", R.version$minor)){
    message("There is a new R version for macOS available. See my notes to updateR in '~/.Rprofile'.")}

Besides of regularily update of R and R packages I have also to update RStudio and pandoc. pandoc is already bundled with RStudio but it seems to me, that I am using a special (extra) installation.

Form time to time I have to update `pandoc` because it seems that this is not done automatically. For instance I have version 1.19.2.1 installed, but currently (201906-05) there is in [pandoc](https://pandoc.org/releases.html) already version 2.7.2.

Both programs have comfortable package installer.

I noticed that my versions were outdated because of an error message:

    Error in doc_parse_raw(x, encoding = encoding, base_url = base_url, as_html = as_html, : Space required after the Public Identifier [65]
    
After updating both software programs the error message disappeared!




    




