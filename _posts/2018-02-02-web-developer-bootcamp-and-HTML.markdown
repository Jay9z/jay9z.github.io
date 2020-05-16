---
layout: post
title: "p1: HTML"
date: "2018-02-02 14:09:48 +0800"
---

### front end and back end
*
*

### tools needed
* chrome
* bootstrap
* atom (with package named tags)

### how internet works
* http requests
* IP address
* servers
* pacages

### html
* shortcut
  *html+tab
  *ctr+/
* MDN
  *mdn+html+element
  *don't need remember all of them, some acquisition is enough
* basic tags
  DOCTYPE,head,body,title,h1~6,p,strong, em
* order list
  ```
  <ol>
  <li> </li>
  <li> </li>
  <li> </li>
  </ol>
  ```
* unorder list
```
  <ul>
  <li> </li>
  <li> </li>
  <li> </li>
  </ul>
```
* composition of ul and ol
when one is put inside the other, its level is simular with tag li.

```
<h2>HTML</h2>
<ul>
  <li>Stands for <strong>Hyper Text Markup Language</strong></li>
<li>Lots of tags</li>
<ul>
  <li>Boilerplate</li>
    <ol>
      <li>Doctype</li>
      <li>HTML</li>
      <li>Head</li>
        <ol>
          <li>Title</li>
        </ol>
      <li>Body</li>
    </ol>
  <li>Headings</li>
  <li>Paragraph</li>
  <li><em>em</em></li>
  <li><strong>strong</strong></li>
</ul>
</ul>

```
Browser Display:

<h2>HTML</h2>
<ul>
  <li>Stands for <strong>Hyper Text Markup Language</strong></li>
<li>Lots of tags</li>
<ul>
  <li>Boilerplate</li>
    <ol>
      <li>Doctype</li>
      <li>HTML</li>
      <li>Head</li>
        <ol>
          <li>Title</li>
        </ol>
      <li>Body</li>
    </ol>
  <li>Headings</li>
  <li>Paragraph</li>
  <li><em>em</em></li>
  <li><strong>strong</strong></li>
</ul>
</ul>

* div
 it works like a container to group components together
 box
* span
  container, inline
* a,img
* table
* form
 * get, post, send?
* input
  .type=color,radio,text,password
  .placeholder=""
  .pattern
  .title
* button  
* select
* textarea

### Html Attribute
* src
* href
* name : used as variable name
* value
* id: identification of element
* class

### what bootstrap is

### components
* containner
  .create a frame for components with round corner decoration
* button
  .btn/.btn-primary/.btn-success/.btn-danger
  .style can be changed by css
* jambostron
  .used to create a discription for whole website/page
* form >.form-group>.form-control
  .from-group :create margin between component group
* form.inline-form
  . make components lie in a single line.  
  . Add .form-inline to your form (which doesn't have to be a <form>) for left-aligned and inline-block controls. This only applies to forms within viewports that are at least 768px wide.
