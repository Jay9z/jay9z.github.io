---
layout: post
title: "web developer bootcamp and DOM"
date: "2018-02-06 16:23:26 +0800"
---

### selection methods
* Document property
 document.url
 document.title
 document.head
 document.body
* Element selector
 document.getElementById
 .getElementsByClassName ==>  HTMLCollection
 .getElementsByTagName ==> HTMLCollection
* CSS-style selector
 .querySelector('#id/.class/tag')
  get first element
 .querySelectorAll(...)
  get all elements list

### manipulate style
1. query a tag
2. define a class of style:
```
.cssClass
  {
  color:green
  font-size:20px
  border:1px dash green
  background:white
  margintop:200px
  }
```

3. execute
* tag.classList.toggle("cssClass")
* tag.classList.add()
* tag.classList.remove()

### manipulate content
* tag.innerHTML = "<h1> good bye </h1>"
* tag.textContent = ''

### manipulate attribute
* tag.getAttribute('href')
* tag.setAttribute('src','..')

### addEventListener
  * Event from M
  * action: click,change,input
