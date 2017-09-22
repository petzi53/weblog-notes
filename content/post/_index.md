---
date: 2017-04-24T18:36:24+02:00
description: ""
title: My Notes (Posts)
weight: 5
pre: "<i class='fa fa-user'>&nbsp;&nbsp;&nbsp;</i> "
---

<footer class=" footline" >
	{{with .Params.LastModifierDisplayName}}
	    <i class='fa fa-user'></i> <a href="mailto:{{ $.Params.LastModifierEmail }}">{{ . }}</a> {{with $.Date}} <i class='fa fa-calendar'></i> {{ .Format "02/01/2006" }}{{end}}
	    </div>
	{{end}}
</footer>
