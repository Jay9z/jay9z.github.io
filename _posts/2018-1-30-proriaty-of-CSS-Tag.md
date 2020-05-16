---
layout: post
title: class of html tags
---

同一个标签可以定义为多个类，但是要注意，head中的顺序决定了class优先级，靠后定义的优先级较高。

## 源代码如下：

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title></title>
<style>
.intro
{
	color:blue;
}
.important
{
	color:red;
}
</style>
</head>
<body>
<h1 class="important intro">标题 1</h1>
<p class="important">注意：这是一个很重要的段落。 :)</p>
</body>
</html>
```
文字显示色：全为红色

<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程</title>
<style>
.intro
{
	color:blue;
}
.important
{
	color:red;
}
</style>
</head>
<body>
<h1 class="important">标题 1</h1>
<p class="important">注意：这是一个很重要的段落。 :)</p>
</body>
</html>


## 源代码2如下：

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title></title>
<style>
.important
{
	color:red;
}
.intro
{
	color:blue;
}
</style>
</head>
<body>
<h1 class="important intro">标题 1</h1>
<p class="important">注意：这是一个很重要的段落。 :)</p>
</body>
</html>
```

文字显示色：一蓝一红

<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程</title>
<style>
.important
{
	color:red;
}
.intro
{
	color:blue;
}
</style>
</head>
<body>
<h1 class="intro">标题 1</h1>
<p class="important">注意：这是一个很重要的段落。 :)</p>
</body>
</html>
