---
title: Theme variants
author: Peter Baumgartner
date: '2017-04-29'
categories:
  
tags:
  - theme-docdock
description: change theme style/colors
disable_comments: yes
draft: yes
---

In site configuration file, you can set a variant name of this theme to load a specific css, with different color specifications.

add a param `themeVariant = "VARIANT_NAME"` in the `[params]` part of config.toml file.

{{%info%}}Available variants change only colors at this moment{{%/info%}}


## Variant "gray"
```
[params]
themeVariant = "gray"
```

![green docdock](/variant-gray.png)

## Variant "gold"
```
[params]
themeVariant = "gold"
```

![gold docdock](/variant-gold.png)

## Variant "green"
```
[params]
themeVariant = "green"`
```

![green docdock](/variant-green.png)
