---
title: Disqus installation again
author: Peter Baumgartner
date: '2017-10-03'
categories:
  - web-service
tags:
  - disqus
  - hugo
slug: disqus-installation-again
description: 'A short personal note on my tutorial on Disqus installation: I have
  used for my screenshots, not this `docdock` but the hugo-academic theme. I have
  changed from `docdock` to `hugo-academic` and now (2017-05-31) I am back at `docdock`
  again. I will explain the reason for this twofold change in one of my next blog
  post. I am also planning to update text and screenshots to the new blogdown versions.'
draft: no
---

In my tutorial [How to install disqus on Hugo]({{< ref "2017-09-10-how-to-install-disqus-on-hugo.md" >}}) I have used the [hugo-academic theme](https://github.com/gcushen/hugo-academic) to demonstrate the installation process. The article was one of my first contact with static websites, and I experimented with it at https://portfolio.peter-baumgartner.net. 

After some experiences with the academic website, I looked for other themes which are using more prominent the blog function. I came up with this beautiful and very functional [hugo-theme-docdock](https://github.com/vjeantet/hugo-theme-docdock) website for documentation. But for the tutorial, I have used a different code for the integration of Disqus proposed by [Yihui Xie](https://support.rbind.io/2017/04/25/yihui-website/).

In the meanwhile, Yihui has suggested his approach as a [pull request](https://github.com/gohugoio/hugo/pull/3639) which was accepted by the Hugo team. So I assume that in a new release we will all get this more elaborated disqus integration code in the standard Hugo installation.
