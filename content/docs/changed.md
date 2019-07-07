---
title: Changed
author: Peter Baumgartner
date: '2019-06-04'
slug: changed
toc: no
disable_comments: yes
draft: yes
no_coins: yes
---

### Link attribute _target="_blank"

```
    [blackfriday]
        hrefTargetBlank = true  # true opens external links in a new tab.
```

changed to:

```
    [blackfriday]
        hrefTargetBlank = false
```
<hr/>

### layouts/partials/last-modified.html

+ always display "Page created" (but not the author because I am the only author!)
+ if `lastmod` is set to a date: display "Last modified"

```
<footer class=" footline" >
    {{with .Params.Date}}
    	   Page created:
    	   {{with $.Date}} <i class='fa fa-calendar'></i> {{ .Format "2006-01-02" }}{{end}}
    {{end}}

    {{ if ne .Lastmod .Date }}
    	{{with .Params.lastmod}}
        	    | Last modified:
        	    {{with $.Lastmod}} <i class='fa fa-calendar'></i> {{ .Format "2006-01-02" }}{{end}}
    	{{end}}
    {{end}}

    </div>

</footer>
```

### archetype with title for special characters

If I am using special characters in the title (for instance a colon) than the text cannot successfully compiled. I added a `'` symbol in the archetype, similar as in the description line.

```
---
title: '"{{ replace .TranslationBaseName "-" " " | title }}"'
date: {{ .Date }}
lastmod:
description: ""
toc: false
disable_comments: true
draft: true
---

Lorem Ipsum....
Notice `draft` is set to true.
```

Now I can write the following title without any problems:

```
---
title: 'This is a Test: with Sonderzeichen'
author: Peter Baumgartner
date: '2019-06-05'
slug: this-is-a-test-with-for-sonderzeichen
categories: []
tags: []
lastmod: ~
description: ''
toc: no
disable_comments: yes
draft: yes
---

Lorem Ipsum....
Notice `draft` is set to true.
```
