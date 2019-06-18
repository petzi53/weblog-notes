---
title: Alternatives for Disqus?
author: Peter Baumgartner
date: '2017-09-14'
categories:
  - web-service
  - review
tags:
  - disqus
lastmod: '2019-06-05'
slug: alternatives-for-disqus
draft: no
description: Disqus is a top-rated service for hosting and managing comments. But
  it has as an external service several disadvantages which oppose the philosophy
  of static websites diametrically. I discuss some alternatives for integrating discussion
  fora with static websites.
---

[Disqus](https://disqus.com/) is a top-rated service for hosting and managing comments. But it has as an external service several disadvantages which opposed the philosophy of static websites diametrically. I discuss some alternatives for integrating discussion fora with static websites.

## Disqus has a long list of drawbacks

In [one of my tutorials]({{< ref "2017-09-10-how-to-install-disqus-on-hugo.md" >}}) I have explained how to integrate [Disqus](https://disqus.com/) into your static website. But in this article, I recommend looking for alternative comment services. Why this different standpoint? In the meanwhile, I read several articles questioning Disqus. Here is a list of critiques I found on the web (without ranking):

* Disqus is slow and has a bad (re-)loading behavior.
* Disqus is tracking many different things for different customers; some of them hidden and unknown.
* Disqus does not allow `Markdown`.
* Disqus does not allow anonymous content  (IP address, email, and name are recorded). 
* Disqus is hosted in the USA which is considered to have less strict privacy laws than Europe.
* Disqus is not open source.
* Disqus does not allow that user can use free licenses for their comments. It is not clear who has ownership of the comments.
* Disqus in one central authority collecting all comments of your website visitors and users on _their_ servers.

Especially the first and last bullet points defeat the advantages of a static website: Speed and _all_ content always at your disposal. On a static website, data are just plain text file, saved locally on your hard disk. Therefore you can static sites transfer easily: Compress all your data in one zip file and unzip it where ever you want it. --- But with Disqus, these advantages are not valid anymore, because your blog text and its comments are hosted separately on different servers.

## What are alternatives for Disqus?

Summarizing the disadvantages, I mentioned above I am looking for a system which is

* free
* open source
* and does not host the user-generated comments centrally

The [Hugo page on comments](https://gohugo.io/content-management/comments/#comments-alternatives) lists six of available alternatives for comment on static websites. On [AlternativeTo](https://alternativeto.net/software/master-comments-system/) you will find 16 systems. 


I looked cursory in some services:

**[Staticman](https://staticman.net/)**: Staticman is open source and transforms user-generated content into data files to merge in your [GitHub](https://github.com/) repository, along with the rest of your content. This approach seems for me promising, but until now, I couldn't manage to install it. I have [reported my problem](https://github.com/eduardoboucas/staticman/issues/134), and I am currently waiting for help. As soon as I know how to fix it, I will review the system here on these pages.

<!--
**[txtpen](https://txtpen.com/)**: txtpen is proprietary software and collects data on its server. e.g., it does not qualify as a better alternative to Disqus. But txtpen is interesting for another reason: It is a service for commenting inline annotation, but not a good one. There are others with better interfaces and more widespread like the proprietary platform [diigo](https://www.diigo.com/) and especially the open source project [hypothes.is](https://web.hypothes.is/). 

<div class="alert alert-warning" role="alert">
<b>Update 2019-05-31:</b> The txtpen link does not work anymore.
</div>
-->

**[hypothes.is](https://web.hypothes.is/)**: The vision is to provide 'a conversation layer over the entire web that works everywhere, without needing implementation by any underlying site'. For this approach, the data has to be stored centrally. So this software again is not an alternative to Disqus. This remark is not a critique of `hypothes.is` because it belongs to another category of software services. It has a new approach worth to review it later in more detail. 

**[IntenseDebate](http://intensedebate.com/)**: It is a feature-rich comment system for many blogging resp. CMS platforms. IntenseDebate is developed by the people who are behind many other well-known software services (e.g., WordPress.com, WooCommerce, Jetpack, Simplenote, VaultPress, Akismet, Gravatar, to name a few). It seems a bit odd that I could not find newer information than [January 2014](https://blog.intensedebate.com/). It is [free but not open source](https://intensedebate.com/tos), but it hosts the content centrally in the US. IntenseDebate is, therefore, no candidate for replacing Disqus.

**[Graphcomment](https://graphcomment.com/)** is a beautiful designed commenting service with a (limited) free plan. But it is disqualified under my criteria as the code is not open source and it hosts the comments centrally too.

**[MUUT](https://muut.com/)**: It [does not allow pre-moderation](http://learn.muut.com/faq), e.g. every comment is online immediately. But it is no alternative to Disqus: There is no free plan, and alls right of the user-generated belongs to MUUT!

**[ISSO](https://posativ.org/isso/)** is a lightweight commenting service, programmed in `Python`, which allows anonymous comments. It is free, open source, and installed locally. So it does qualify! But the installation procedure seems complex as there is no GUI and one has to use the terminal for the installation. Furthermore, it seems to me that not all operating systems are covered. But I  should give it a try anyway and review it.

**[Discourse](https://www.discourse.org/)** is a feature-rich open source environment, supports `Markdown` and allows anonymous posting. As a hosting service, it has no free plan and costs as a minimum US$ 100  / month (with 80% discount for educational resp. 50% for non-profit institutions.). But you can install Discourse yourself without cost on your server. Alternatively, you can pay a one-time fee of $99 for a cloud installation with a $10/month hosting fee. With the possibility to install it on your server, `Discourse` is another candidate to try out.

**[Using GitHub](http://donw.io/post/github-comments/)**: Another website is also recommending to use [GitHub](https://github.com/) for comments. I have no clear idea how these proposed code lines will work in practice, but if it works, then it will certainly qualify: Open source, free, supporting `Markdown` and hosted by the website owner.

## Summary

I reviewed superficially different commenting systems. I was looking for a free, open source system, allowing anonymous content, `Markdown` and hosted by the website owner. Four services seem to fulfill my criteria: `Staticman`, `ISSO`, `Discourse` and a code proposal by `Don Williamson`. `hypothes.is` is an exciting project, but not a commenting system. It belongs, therefore, to a different category of software (annotation systems). 

A competent review of these four systems requires a test installation, which I plan to do in the next few weeks. 

