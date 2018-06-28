---
title: "R Demo for Edudays"
author: "Peter Baumgartner"
date: '2018-04-02'
description: Nur eine kleine Demo
draft: yes
slug: r-demo-for-edudays
tags: test
categories: test
---

## Demo for Edudays

Heute halte ich ein Referat für die [Edudays](http://www.edudays.at).

Gehen auch die Umlaute? ÄÖÜßäöü

## Von R/RStudio über Git und GitHub zu Netlify und Hugo

Es ist ein recht komplexer Prozess, der im Hintergrund abläuft.

1. Zuerst die neue/geändert Datei speichern
2. Das erzeugt eine Änderung im Reiter "Git" (rechtes obereres Fenster)
3. Wähle "Commit", dh. im Versionierungssystem abspreichern
4. Änderung mit einer Meldung versehen und absenden "Commit"
5. Danach diese Änderung in das [ferne (remote) Repositorium](https://github.com/petzi53/weblog2-new) senden: Push
6. Das erzeugt jetzt auf [Netlify.com](https://netlify.com) die entsprechende Webseite. (Meine Netlify-Seite ist auf https://app.netlify.com/sites/pb/overview). Netlify "wacht" über Änderungen auf meiner GitHub-Seite.
7. Der Website wird nun mit Hilfe von [Hugo](https://gohugo.io/), einem statischen Website-Generator, kompiliert.

