---
layout: post
title: "p5:js array"
date: "2018-02-05 00:22:14 +0800"
---

### array definition
* var color =['red','yellow','orange']
* []
* new Array()
* can hold array kinds of different data in one array
* can be used like:color[4]='black', color[10]= 'purple'
* color.length

### array method
* arr.push & pop
  array works like stack from array end

* arr.unshift & shift
  operate at array front; unshift is push operation at the front postion of array

* arr.indexOf(item)
  find the index of an item

* arr.slice(n,m)
 copy [n,m) items from array

* arr.forEach(func)
 func should defined as following:
  * 1st type
  function func(element[,index[,arr]]){}
  arr.forEach(func)
  * 2nd type
  arr.forEach(function func(color){})

* arr.splice(index)

### add array method
* Array.prototype.methodname = function(func_callback){}
