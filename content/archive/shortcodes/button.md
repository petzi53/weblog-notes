---
title: button
author: Peter Baumgartner
date: '2019-06-05'
categories:
  - shortcode
  - demo
  
  - how-to
description: Display an actionable button in your page.
disable_comments: yes
draft: yes
---

Display an actionable button in your page.

{{<button align="center" href="#" theme="warning" >}} This is a warning button {{< /button >}}

## Usage 

| Parameter | Default | Description |
|:--|:--|:--|
| href | "" | The location href to link to |
| align | "center" | horizontal align button on page |
| theme | `primary` | `default`, `primary` , `success`,`info`,`warning`,`danger` |

The inner text you place in short code will be displayed as the _button text_

## Demo

	{{</* button href="https://google.com" */>}} go to google {{</* /button */>}}
	{{</* button href="https://google.com" theme="success" */>}} Success {{</* /button */>}}
	{{</* button href="https://google.com" theme="info" */>}} Info {{</* /button */>}}
	{{</* button href="https://google.com" theme="warning" */>}} Warning {{</* /button */>}}
	{{</* button href="https://google.com" theme="danger" */>}} Danger ! {{</* /button */>}}
	{{</* button href="https://google.com" theme="default" */>}} Danger ! {{</* /button */>}}
    
{{<button href="https://google.com" >}} go to google {{< /button >}}
{{<button href="https://google.com" theme="success">}} Success {{< /button >}}
{{<button href="https://google.com" theme="info">}} Info {{< /button >}}
{{<button href="https://google.com" theme="warning">}} Warning {{< /button >}}
{{<button href="https://google.com" theme="danger">}} Danger ! {{< /button >}}
{{<button href="https://google.com" theme="default">}} Danger ! {{< /button >}}



