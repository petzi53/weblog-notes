---
title: Comments in Markdown
author: Peter Baumgartner
date: '2019-06-02'
categories:
  - blogdown
tags:
  - markdown
slug: comments-in-markdown
lastmod: 2019-06-04
description: How to set comments in markdown?
disable_comments: no
draft: no
---

In reworking this ` docdock-theme,` I wanted to document the reasons for my changes and how I have done it. But I didn't know how to write comments in markdown. Searching in `Stack Overflow` I came up with the following  [solution](https://stackoverflow.com/questions/4823468/comments-in-markdown):


```
[comment]: # (This is a comment, it will not be included.)
```
[comment]: # (This is a comment, it will not be included.)

There exist other versions as well, but the example above is the most portable solution. --- You can't see the result of this code, as it is hidden by definition :wink:. But look at the source code on my `GitHub` repository. Just click on the `Edit page` link in the top right corner of this page.

It is also possible to write lengthy comments or to comment out a whole paragraph. 

```
In reworking this ` docdock-theme,` I wanted to document the reasons for my changes and how I have done it. But I didn't know how to write comments in markdown. Searching in `Stack Overflow` I came up with the following [solution](https://stackoverflow.com/questions/4823468/comments-in-markdown):
```

[comment]: # (In reworking this ` docdock-theme,` I wanted to document the reasons for my changes and how I have done it. But I didn't know how to write comments in markdown. Searching in `Stack Overflow` I came up with the following [solution](https://stackoverflow.com/questions/4823468/comments-in-markdown):)

But line breaks are not allowed.
