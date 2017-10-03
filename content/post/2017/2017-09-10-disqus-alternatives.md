---
title: Alternatives for Disqus?
author: Peter Baumgartner
date: '2017-09-14'
slug: alternatives-for-disqus
categories: [static sites, blog engines]
tags: [disqus]
draft: no
description: Disqus is a very popular service for hosting and managing comments. But it has as an external service several disadvantages which oppose diametrically the philosophy of static websites. I discuss some alternatives for integrating discussion fora with static websites.
---
[Disqus](https://disqus.com/) is a very popular service for hosting and managing comments. But it has as an external service several disadvantages which opposed diametrically the philosophy of static websites. I discuss some alternatives for integrating discussion fora with static websites.

## Disqus has a long list of drawbacks

In [one of my tutorials]({{< ref "2017-09-10-how-to-install-disqus-on-hugo.md" >}}) I have explained how to integrate [Disqus](https://disqus.com/) into your static website. But in this article I recommend to look for alternative comment services. Why this opposite standpoint? In the meanwhile I read several articles questioning Disqus. Here is a list of critiques I found on the web (without ranking):

* Disqus is slow and has a bad (re-)loading behavior.
* Disqus is tracking many different things for different customers; some of them hidden and unknown.
* Disqus does not allow Markdown.
* Disqus does not allow anonymous content  (IP address, email and name is recorded). 
* Disqus is hosted in the USA which is considered to have less stricter privacy laws than Europe.
* Disqus is not open source.
* Disqus does not allow that user can use free licenses for their comments. It is not clear who has the ownership about the comments.
* Disqus in one central authority collecting all comments of your website visitors and users on _their_ servers.

Especially the first and last bullet points defeats the advantages of a static website: Speed and _all_ content always at your disposal. On a static website, data are just plain text file, saved locally on your hard disk. Therefore you can static websites transfer easily: Compress all your data in one zip file and unzip it where ever your want it. --- But with Disqus these advantages are not valid anymore, because your blog text and its comments are hosted separately on different servers.

## What are alternatives for Disqus?

Summarizing the disadvantages I mentioned above I am looking for a system which is

* free
* open source
* and does not host the user-generated comments centrally

The [Hugo page on comments](https://gohugo.io/content-management/comments/#comments-alternatives) lists six of available alternatives for comment on static websites. On [AlternativeTo](https://alternativeto.net/software/master-comments-system/) you will find 16 systems. 


I looked cursory in some services:

**[Staticman](https://staticman.net/)**: Staticman is open source and transforms user-generated into data files that will be merged in your [GitHub](https://github.com/) repository, along with the rest of your content. This seems for me a very promising system, but until now I couldn't manage to install it. I have [reported my problem](https://github.com/eduardoboucas/staticman/issues/134) and I am currently waiting for help. As soon as I know how to install it, I will review the system here on these pages.

**[txtpen](https://txtpen.com/)**: txtpen is proprietary software and collects data on its own server. e.g. it does not qualify as a better alternative to Disqus. But textpen is interesting for another reason: It is a service for commenting inline annotation, but not a good one. There are others with better interfaces and more widespread like the proprietary platform [diigo](https://www.diigo.com/) and especially the open source project [hypothes.is](https://web.hypothes.is/). 

**[hypothes.is](https://web.hypothes.is/)**: The vision is to provide 'a conversation layer over the entire web that works everywhere, without needing implementation by any underlying site'. For this approach the data has to be stored centrally. So this software again is not an alternative to Disqus. This is not a critique on `hyothes.is` because it belongs to another category of software services. It has a very interesting approach worth to review it later in more detail. 

**[IntenseDebate](http://intensedebate.com/)**: It is a feature-rich comment system for many blogging resp. CMS platforms. IntenseDebate is developed by the people who are behind many other well known software services (e.g. WordPress.com, WooCommerce, Jetpack, Simplenote, VaultPress, Akismet, Gravatar to name a few). It seems a bit odd that I could not find newer information than [January 2014](https://blog.intensedebate.com/). It is [free but not open source](https://intensedebate.com/tos) and the content is centrally hosted in US. IntenseDebate is therefore no candidate for replacing Disqus.

**[Graphcomment](https://graphcomment.com/)** is a beautiful designed commenting service with a (limited) free plan. But it is disqualified under my criteria as the code is not open source and the comments are hosted centrally.

**[MUUT](https://muut.com/)**: It [does not allow pre-moderation](http://learn.muut.com/faq), e.g. every comment is online immediately. But it is no alternative to Disqus: There is no free plan and _every possible_ right of user-generated content, which is hosted centrally, is transferred to MUUT!

**ISSO** is a lightweight commenting service, programmed in Python, which allows anonymous comments. It is free, open source and installed locally. So it does qualify! But the installation procedure seems complex as there is no GUI and one has to use the terminal for the installation. Furthermore is seems to me that not all systems are covered. But I  should give it a try anyway and review it.

**[Discourse](https://www.discourse.org/)** is a feature-rich open source environment, supports Markdown and allows anonymous posting. As a hosting service it has no free plan and costs as minimum US$ 100  / month (with 80% discount for educatioanl resp. 50% for non-profit institutions.). But you can install Discourse yourself without cost on your own server. Alternatively you can pay a one time-fee of $99 for a cloud installation with a $10/month hosting fee. With the possibility to install it on your server, `Discourse` is another candidate to try out.

**[Using GitHub](http://donw.io/post/github-comments/)**: Another website is also recommending to use [GitHub](https://github.com/) for comments. I have no clear idea how these proposed code lines will work in practice, but if it works, than it will certainly qualify: Open source, free, supporting Markdown and hosted by the website owner.

## Summary

I reviewed superficially different commenting systems. I was looking for free, open source system, allowing anonymous content, Markdown and hosted by the website owner. Four systems seem to fulfill my criteria: `Staticman`, `ISSO`, `Discourse` and a code proposal by `Don Williamson`. `hypothes.is` is a very interesting project, but not a commenting system. It belongs therefore to a different category of software (annotation systems). 

A competent review of these 4 systems requires a test installation, which I plan to do in the next few weeks. 


