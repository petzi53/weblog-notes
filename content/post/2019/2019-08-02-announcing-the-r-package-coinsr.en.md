---
title: Announcing the R package coinsR
author: Peter Baumgartner
date: '2019-08-02'
categories:
  - scientific writing
  - app
tags:
  - blogdown
  - citation
  - hugo
  - r
  - RStudio
description: 'This blog entry announces the R program `coinsR` to produce bibliographic metadata automatically for websites within the Hugo framework. The dominant use case at the moment is with the `blogdown` package.'
disable_comments: no
draft: no
slug: announcing-the-r-package-coinsr
---

This blog entry announces the R program `coinsR` to produce bibliographic metadata automatically for websites within the Hugo framework. The dominant use case at the moment is with the `blogdown` package.

In a [previous blog entry](/2019/06/19/bibliographic-metadata-for-your-web-page/) I wrote about the advantages to provide bibliographic metadata for your web pages producing COinS. COinS is the abbreviation of [Context Objects in Spans](https://en.wikipedia.org/wiki/COinS). It refers to a [microformat standard to embed bibliographic metadata as HTML](https://www.univie.ac.at/elib/index.php?title=COinS_Microfromat_Bibliographic_Metadata_for_Embedding_in_HTML). 

A [COinS string](https://www.questia.com/magazine/1G1-161981672/coins-what-it-stands-for-context-objects-in-spans) includes HTML code all the information necessary to cite a publication correctly. It works for every type of writing (books, papers, web pages). COinS embedded in your HTML pages help your blog readers or website visitors to cite your posts and pages correctly.


I wrote also a [detailed tuorial](/tutorial/how-to-produce-bibliographic-metadata-for-you-web-page/) how to produce COinS with the help of the free bibliographical research tool [Zotero](https://www.zotero.org/). But this is a quite complicated procedure with several steps. Besides, it works only for every page individually and not automatically for all blog entries of your website.

To produce COinS laboriously for every webpage was my motivation to write the R package `coinsR` for it.


## Use cases of `coinsR` and its limitations

The package requires:

1. [Hugo](https://gohugo.io) with the R package [blogdown](https://bookdown.org/yihui/blogdown/)
2. Config file in the TOML format (config.toml)
3. Blog entries with YAML frontmatter

I am planning for a future version to loosen the last two limitations and allow it for config.yaml and TOML frontmatter (but not for .json).

You can call `coinsR` via an RStudio Addin for every page individually. But you can also produce COinS automatically for all files under a specific directory.

## Where to find `coinsR` and how to install it?

You can download the package from Github with 

```
remotes::install_github('petzi53/coinsR', build_vignettes = TRUE)
```

I am trying to prepare `coinsR` as an R package distributed via the [CRAN repository](https://cran.r-project.org/). But as I am still not very experienced in R programming, I am not sure if I will succeed. 

There is a detailed description in the help file and the vignette description of how to invoke the two functions `coins_this()` and `coins_all()`. 


<span class='Z3988' title='url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=blogPost&amp;rft.title=Announcing%20the%20R%20package%20coinsR%20::%20Open%20Science%20Education&amp;rft.source=Announcing%20the%20R%20package%20coinsR&amp;rft.rights=CC%20BY-SA%204.0&amp;rft.description=This%20blog%20entry%20announces%20the%20R%20program%20%60coinsR%60%20to%20produce%20bibliographic%20metadata%20automatically%20for%20websites%20within%20the%20Hugo%20framework.%20The%20dominant%20use%20case%20at%20the%20moment%20is%20with%20the%20%60blogdown%60%20package.&amp;rft.identifier=https%3A%2F%2Fnotes.peter-baumgartner.net%2F2019%2F08%2F02%2Fannouncing-the-r-package-coinsr&amp;rft.aufirst=Peter&amp;rft.aulast=Baumgartner&amp;rft.au=Peter%20Baumgartner&amp;rft.date=&amp;rft.language=en'></span>
