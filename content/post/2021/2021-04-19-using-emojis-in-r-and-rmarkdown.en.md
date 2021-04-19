---
title: "Using Emojis in R and RMarkdown"
author: "Peter Baumgartner"
date: '2021-04-19'
slug: using-emojis-in-r-and-rmarkdown
categories:
- Rmarkdown
- package
tags:
- emo
- emoji
- unicode
lastmod: null
description: 'Recently I worked on some pull requests for [interactive tutorials](https://github.com/OpenIntroStat/ims-tutorials) for the  OpenIntro textbook Introduction to Modern Statistics. There I came across the [package `emo`](https://github.com/hadley/emo). Its purpose is: "Easily insert emoji into R and RMarkdown". This post describes some learnings on how to use this package.'
disable_comments: no
draft: no
---

Recently I worked on some pull requests for [interactive tutorials](https://github.com/OpenIntroStat/ims-tutorials) for the OpenIntro textbook Introduction to Modern Statistics. There I came across the [package `emo`](https://github.com/hadley/emo). Its purpose is: “Easily insert emoji into <svg aria-hidden="true" role="img" viewBox="0 0 581 512" style="height:1em;width:1.13em;vertical-align:-0.125em;margin-right:0.2em;font-size:inherit;fill:steelblue;overflow:visible;position:relative;"><path d="M581 226.6C581 119.1 450.9 32 290.5 32S0 119.1 0 226.6C0 322.4 103.3 402 239.4 418.1V480h99.1v-61.5c24.3-2.7 47.6-7.4 69.4-13.9L448 480h112l-67.4-113.7c54.5-35.4 88.4-84.9 88.4-139.7zm-466.8 14.5c0-73.5 98.9-133 220.8-133s211.9 40.7 211.9 133c0 50.1-26.5 85-70.3 106.4-2.4-1.6-4.7-2.9-6.4-3.7-10.2-5.2-27.8-10.5-27.8-10.5s86.6-6.4 86.6-92.7-90.6-87.9-90.6-87.9h-199V361c-74.1-21.5-125.2-67.1-125.2-119.9zm225.1 38.3v-55.6c57.8 0 87.8-6.8 87.8 27.3 0 36.5-38.2 28.3-87.8 28.3zm-.9 72.5H365c10.8 0 18.9 11.7 24 19.2-16.1 1.9-33 2.8-50.6 2.9v-22.1z"/></svg> and RMarkdown.”

I was surprised that there is a special package. I didn’t think that including emojis wouldn’t be a problem — at least on the macOS. I only have to open the window for emojis and symbols (CMD-SHIFT-SPACE) and double click on the icon to insert it into the markdown document. No big deal, so what’s the matter?

![Screenshot of macOS window showing a selection of emojis](/post/2021/2021-04-19-using-emojis-in-r-and-rmarkdown.en_files/macOs-emojis-min.png)

After I searched online, I saw that there many questions (and [solutions](https://stackoverflow.com/questions/52378661/how-to-display-emojis-in-ggplot2-using-emo-package-in-r)) about this problem. There is on CRAN a special [package `emojifont`](https://cran.r-project.org/web/packages/emojifont/index.html) for using emojis and [Font Awesome](https://fontawesome.com/) in base R and `ggplot2` graphics and with [`emoGG`](https://github.com/dill/emoGG) another one on GitHub.

For me, it is still not clear what exactly the problem is. Perhaps it has to do with different operating systems? Does the Unicode not translate to all systems?

Anyway, I looked into `emo,` and it turned out that it offers some useful functions when working with strings containing emojis. You can also add emojis to summarize p-values. Additionally, I learned several things:

1.  With `emojis_df <- emo::jis`, you get a data frame with 3570 emoticons categorized by 21 variables.

2.  In `emojis_df`, you will find the keywords for each emoji. But this is problematic as they are not unique. In the [ReadMe of `emo` in GitHub](https://github.com/hadley/emo#keywords), you will see a massive list of multiple references for each keyword.

3.  If you are using keywords, the command `emo::ji(<keyword>)` will randomly pick one.

``` r
emo::ji("face")
emo::ji("face")
emo::ji("face")
```

    ## 😷 
    ## 😃 
    ## 😙

To identify, you have to use the short name of the [Common Local Data Repository](http://cldr.unicode.org/) (CDLR) included in the `emojis_df`.
If you want to use emojis with a particular skin tone, you have to use the alias name as the CDLR name produces an error.
Instead of looking up an emoji within the above-created data frame `emojis_df`, I found it more practicable to search in the official [Unicode Emoji List](https://www.unicode.org/emoji/charts/emoji-list.html). It has not so many different columns but focuses on icon display and CLDR short name.
