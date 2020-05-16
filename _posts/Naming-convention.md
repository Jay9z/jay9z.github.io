---
title: Naming convention
date: 2019-07-24 23:20:21
tags:
---

summarize the ways i will follow in futher project.

### class

combination of upper capital nouns, such as "MyClass".


### method

combination of verb and nouns, and verb with lower initial, such as "buyCandy".


### property

start with m_, and combine with nouns, such as "m_towerHeight".


### variable

It is combined of nouns, and the first nouns has low initial, such as "oldValue".


### space

before closure, there are two empty lines. one empty line is used between function modules.
``` code
void buyCandy()
/*if there are candys in pocket, you don't need buy some more.
*/
{
	// number of canday in pocket
	int totalNum = countCandy();

	if(totalNum<=0)
	{
		return true;
	}
	else
	{
		return false;
	}
}


void sellCandy()
/*if there are candys in pocket, you can sell them.
*/
{
	if(totalNum<=0)
	{
		return false;
	}
	else
	{
		return true;
	}
}
```


### comment

There are three types of comments, such as Module, Class/Method, and Section. 


