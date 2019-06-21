---
title: ".md File Test"
author: Peter Baumgartner
date: '2019-06-10'
slug: md-file-test
categories: []
tags: []
lastmod: ~
description: ''
toc: no
disable_comments: yes
draft: yes
---

+ Notice `draft` is set to true.
+ Here also works the <code>code</code> command.
+ But snippet do not work


You can use alert, notice and panel shortcode with quotes. But better not, as they do not work in .Rmd files.

New lines, formating like bold or italics do not work inside these shortcodes. Use HTML instead.

{{% alert theme="info"%}}**this** is an info{{% /alert %}}
{{% alert theme="success" %}}**Yeahhh !** is an success{{% /alert %}}
{{% alert theme="warning" %}}**Be carefull** is a warning{{% /alert %}}
{{% alert theme="danger" %}}**Beware !** is a danger{{% /alert %}}


