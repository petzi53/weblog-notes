---
title: revealjs
author: Peter Baumgartner
date: '2019-06-05'
categories:
  
  - shortcode
  - demo
tags:
  - reveal.js
description: Present content as a slide, using reveal.js
slug: revealjs
disable_comments: yes
draft: yes
---

This shortcode will format the enclosed markdown to render it with [reveal.js](http://lab.hakim.se/reveal-js/) at runtime (client-side)

Read more on [revealjs github repo](https://github.com/hakimel/reveal.js/#markdown).

## Usage

`revealjs` can use the following named parameters :

* theme
* transition
* controls
* progress
* history
* center


{{%warning title="Important" %}}Even if the enclosed content is a markdown, use `<` shortcode notation instead of the `%` notation {{%/warning %}}

### Content formating and slide delimiters

[read more on this here]({{% relref "page-slide.md"%}})

## Demo

{{<revealjs theme="moon" progress="true" controls="true">}}

# In the morning

___


## Getting up

- Turn off alarm
- Get out of bed

___

## Breakfast

- Eat eggs
- Drink coffee

---

# In the evening

___

## Dinner

- Eat spaghetti
- Drink wine

___

## Going to sleep

- Get in bed
- Count sheep

{{</revealjs>}}

## Source :

* [{{%icon "sunglasses" %}} click here to view raw content](https://raw.githubusercontent.com/vjeantet/hugo-theme-docdock/master/exampleSite/content/shortcodes/revealjs.md)
editURL

