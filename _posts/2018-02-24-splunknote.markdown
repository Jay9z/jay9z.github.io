---
layout: post
title: "SPLUNK_note for <<implement splunk>>"
date: "2018-02-24 23:18:09 +0800"
---
事件用键值对表示字段与值

搜索的本质是统计字段


搜索词不区分大小写的；
多个搜索词同时出现，表示“and”关系；
字段名称区分大小写，但字段的取值不区分。譬如 host=“myhost”
索引名称是怎么建立的？

如何加快搜索
保存搜索
创建报警 1.

1. top命令
给出 count 和 percent，简化stats
| top host user 和 | top user by host是不同的
前者先按host字段的统计数量的按序拆分，再按user字段的统计数量继续按序拆分；
后者先按host字段的值按序拆分，再按user字段的统计数量按序拆分。

| top user by host
| top limit=20 host

| top useother=true otherstr="others" ip logger
userother参数用于累加limit之外的字段信息，otherstr参数用于设置显示关键字

2. stats命令
| stats functions by fileds
functions：
  count, avg(fieldname), max(fieldname)...
e.g.  | stats count first(ip) max(_time) as _time by user

3. table命令
与stats的区别？table直接取回字段，stats会进行统计

3. chart命令
| chart count over user by logger
| chart count over logger by user

4. timechart命令
| timechart limit=3 usenull=false count by user

5. eval命令
有哪些函数呢？

6. rex命令
| rex “ip=(?P<subnet>\d+\.\d+\.\d+)\.\d+”
| rex field=ip "(?P<subnet>\d+\.\d+\.\d+)\.\d+”

例子：
ip=(?P<subnet>192.168.1)\.\d+

7. bucket
span=1h, bins=10
建立索引 与 抽取字段
抽取字段默认是对 _raw字段进行操作的
抽取字段命令的使用：在搜索中使用fieldholder而不是提取器的名称

# post search
search(with a given id)通过命令table或stats过滤出多个指示板共用的field，从而去除重复搜索

# 子查询

# 扩展搜索，都类似与给搜索另起一个名字
1. 标签
| tag::tagname
2. 事件类型
为常用搜索字符串起了一个别名
| eventtype= eventname
3. （自动）查找操作
将定义文件中的字段也添加的搜索结果中。
| lookup fileName columnName
e.g.
sourcetype="impl_splunk_gen" | lookup users.csv user | stats count by user city state department
4. 宏

5. 工作流动作
在事件操作中添加而外的搜索功能

# 定制nav bar
面板的id对应与xml中的name，当我们通过右键修改splunk面板标题之后，其id保持不变，但显示在UI中的菜单项会随“标题”变化。另外通过复制面板产生新面板时，“面板”的默认id会根据其“标题”命名自动生成，需要特别注意。

# 配置合并优先级
  搜索之外的：
  system/default
  reversed_apps/default
  reversed_apps/local
  system/local

  搜素功能：
  system/default
  system/local
  sorted_other_apps/default
  sorted_other_apps/local
  current_app/default
  current_app/local

How to use python code in splunk
  1. required lib is not available, but depended its depended libs are installed
  download code from github, and build it as separated lib
  python setup.py build_ext --inplace --force

  2. lib and its depended libs are all not installed
    # method 1: use pip
    check pip, or install pip by "python setup.py install"/ "python get-pip.py"
    # method 2: build all source code

    # method 3: pip install and copy them from "site-package"
  3. copy package to bin directory(my method)
