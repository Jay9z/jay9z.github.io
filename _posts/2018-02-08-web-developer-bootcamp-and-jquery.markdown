---
layout: post
title: "web developer bootcamp and JQuery"
date: "2018-02-08 22:02:17 +0800"
---
### CDN
* download js lib there
* or link url to script.src

### element selection with JQuery
* $(...).method()
* always list output
* iteration operation
* get one of elements
  $(...).last().method
  $(...).first().method
### Style
* $().css(,)
* style name
  CSS: camel style attribute name
  html: c language style attribute name
* $(tag:first-of-type)

### Text (WR)
* .text() : read textContent
* .text(something) : write something as textContent, it is a more safe operation
* when write, it iterate and give a value to every tag

### Attribute & Value 5851011H@Njie
e.g.
$(img).css({width:"200px"})
$(img).attr("src"):get attribute
$(img).attr("src",'...jpg'): set attribute
$(img).attr("type","checkbox"): set attribute
$(input).val(): get value
$(input).val("input text") : set value

### Class Objects
.addClass()
.toggleClass()
.
