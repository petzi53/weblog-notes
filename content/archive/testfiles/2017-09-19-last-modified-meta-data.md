---
author: Peter Baumgartner
categories: [test, help]
tags: [test]
date: 2017-09-19
description: How to apply last modified data to the footer?
slug: last-modified-meta-data
title: Last modified meta data
creatordisplayname: Peter Baumgartner
creatoremail: peter.baumgartner@icloud.com
lastmodifierdisplayname: Petzi Baumgartner
lastmodifieremail: peter.baumgartner@icloud.com
lastmod: 2017-09-23
draft: false
---

#### add to the YAML frontmatter

```
creatordisplayname: Jack Praker
creatoremail: jack.praker@icloud.com
lastmodifierdisplayname: Jack Praker
lastmodifieremail: jack.praker@icloud.com
lastmod: 2017-09-23
```
#### add a new partial with following code

```
<footer class=" footline" >
	{{with .Params.LastModifierDisplayName}}
	    Last modified:
	    <i class='fa fa-user'></i> <a href="mailto:{{ $.Params.LastModifierEmail }}">{{ . }}</a> {{with $.Lastmod}} <i class='fa fa-calendar'></i> {{ .Format "2006-01-02" }}{{end}}
	    </div>
	{{end}}
</footer>
```

#### include partial in template

Include the partial in an adequat place in your templates. (Either `single.html` oder `footer.html` etc.)



**But how to use the `creator` metadata?**
