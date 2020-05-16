---
title: 学习设计模式
date: 2019-07-13 21:22:30
tags:
---


### 面向对象三特性：封装、继承、多态
> 封装：分离业务逻辑与界面逻辑的 譬如：计算器的GUI和数学运算函数，GUI的内容和布置会根据用户类别进行设计，而计算函数却可以保证不变。
> 继承：通过继承提供业务逻辑扩展的安全行与便利性。譬如在不修改四则运算函数代码的情况下，添加根方运算函数。
> 多态: ？？

### UML类图

接口，继承关系
聚合关系（数组），组合关系（属性）
依赖关系（形参），关联关系（引用）

### 工厂模式
``` code
class CalFactory():
	def __init__(self):
		pass

	def createCal(self,index):
		oper = None
		switch(index):
		{
			case 1:
				oper = Add()
				break
			case 2:
				oper = Sub()
				break
		}
		return oper

class Calculation():
	def __init__(self):
		self.numberA = None
		self.numberB = None

	def GetResult(self):
		pass

class Add(Calculation):
	def __init__(self):
		super(Add,self).__init__(self)

	def GetResult(self):
		return self.numberA+self.numberB

class Sub(Calculation):
	def __init__(self):
		super(Sub,self).__init__(self)

	def GetResult(self):
		return self.numberA-self.numberB
```

### 策略模式



### 装饰模式