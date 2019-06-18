---
title: About images (.md)
author: Peter Baumgartner
date: '2017-04-24'
slug: about-images-md
description: This post demonstrates different methods to display pictures.
disable_comments: yes
draft: yes
---

Images have a similar syntax to links but include a preceding exclamation point.

	![agence](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg)

![agence](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg)

## Resizing image

Add HTTP parameters `width` and/or `height` to the link image to resize the image. Values are CSS values (default is `auto`).


	![Hackathon](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg?height=180px)

![agence](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg?height=180px)


## Add CSS classes

Add a HTTP `classes` parameter to the link image to add CSS classes. `shadow` and `border` are available but you could define other ones.

	![s](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg?classes=border,shadow)

![agence](https://github.com/vjeantet/vjeantet.fr/raw/master/static/images/sgthon/C.jpg?classes=border,shadow)

***
## Image with relative URL

### The solution above doees not work (or does it?)


	![Foto Peter](/img/petzi.jpg?height=180px)

![Foto Peter](/img/petzi.jpg?height=180px)


### Other solution ist HTML for `.md` files


        <img src="/img/petzi.jpg" alt="Foto Peter" style="width: 100px; height: 100px"/>

<img src="/img/petzi.jpg" alt="Foto Peter" style="width: 100px; height: 100px"/>

### In `.Rmd` files work the following code:

        ![Foto Peter](/img/petzi.jpg){ width=10% }

 ( Not here, because this is an `.md` file.)
 
### In inline markdowmn

If you are using external markdown (for instance using sildes with `reveal.js`) then you can use:

        ![Foto Peter](/img/petzi.jpg)<!-- .element height="50%" width="50%" -->
 
