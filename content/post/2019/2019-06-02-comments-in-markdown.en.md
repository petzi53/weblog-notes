---
title: Comments in Markdown
author: Peter Baumgartner
date: '2019-06-02'
categories:
  - tips
tags:
  - markdown
slug: comments-in-markdown
lastmod: 2019-06-05
description: How to write comments in markdown?
disable_comments: no
draft: no
---

In reworking this ` docdock-theme,` I wanted to document the reasons for my changes and how I have done it. But I didn't know how to write comments in markdown. 

Yes, one could use a normal HTML-comment, but you still can see the comment in the source code. 

```
<!-- 
This is a comment.

Multiline comments are allowed as well 
-->
```

Look at the source code, and you will see the text example below this line.

<!-- 
This is a comment.

Multiline comments are allowed as well 
-->


Searching in `Stack Overflow` I came finally up with the following  [solution](https://stackoverflow.com/questions/4823468/comments-in-markdown):


```
[comment]: # (This text is a comment!)

[comment]: # (This text is a comment! Multiline comments are allowed as far as long there is no line break. This text is a comment! Multiline comments are allowed as long as there is no line break. This text is a comment!  Multiline comments are allowed as long as there is no line break. )
```
[comment]: # (This text is a comment!)

[comment]: # (This text is a comment! Multiline comments are allowed as far as long there is no line break. This text is a comment! Multiline comments are allowed as long there is no line break. This text is a comment! Multiline comments are allowed as long there is no line break. )

You can't see the result of this last code example not even in the source code. The comment is hidden by definition :wink: But you can inspect my original text file on my `GitHub` repository. Just click on the `Edit page` link in the top right corner of this page.

There are also other possibilities, but the above solution with `comment:` written in square brackets and the `#` - sign followed by the comment written inside round brackets is the most portable version. 
