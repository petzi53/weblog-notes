---
title: alert
author: Peter Baumgartner
date: '2019-06-05'
categories:
  - shortcode
  - demo
  - how-to
weight: 10
description: The alert shortcode allows you to highlight information in your page.
disable_comments: yes
draft: yes
---

The `alert` shortcode allow you to highlight information in your page. They create a colored box surrounding your text, like this:

{{%alert%}}**This is** an alert !{{%/alert%}}

## Usage 

| Parameter | Default | Description |
|:--|:--|:--|
| theme | `info` | `success`, `info`,`warning`,`danger` |

{{%alert info%}}
**Tips :** setting only the theme as argument works too : 
`{{%/*alert warning*/%}}`  instead of `{{%/*alert theme="warning"*/%}}`
{{%/alert%}}

{{%alert danger%}}
<b>Danger:</b>
<ol>
</li>Writing with quotes generates an Error in .Rmd files.
Instead of `{{%/*alert theme="warning"*/%}}` USE ALWAYS `{{%/*alert warning*/%}}`</li>
</li>Markdown formating like extra lines or bold with ** do not work neither, use HTML insted!</li>
</ol>

{{%/alert%}}

## Basic examples

	{{%/* alert theme="info" */%}}**this** is a text{{%/* /alert */%}}
	{{%/* alert theme="success" */%}}**Yeahhh !** is a text{{%/* /alert */%}}
	{{%/* alert theme="warning" */%}}**Be carefull** is a text{{%/* /alert */%}}
	{{%/* alert theme="danger" */%}}**Beware !** is a text{{%/* /alert */%}}

{{% alert theme="info"%}}**this** is an info{{% /alert %}}
{{% alert theme="success" %}}**Yeahhh !** is an success{{% /alert %}}
{{% alert theme="warning" %}}**Be carefull** is a warning{{% /alert %}}
{{% alert theme="danger" %}}**Beware !** is a danger{{% /alert %}}
