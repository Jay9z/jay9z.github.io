---
layout: post
title: WIT web installation for developer
---
这篇文章用于介绍WITweb这套软件系统的安装与配置方法，也讲述了所依赖的开发包。所需源代码可以通过[https://github.com/TestProcessOffice/WireIntegrationTest](https://github.com/TestProcessOffice/WireIntegrationTest)获取，或者联系SAMC，process test office获取。

### Download tools
Downloading following software installer, and install them sequence independently.
* pycharm
* github desktop
* neo4j
* python2.7 or python3.6

### Configuration
This step will prepare denpendent modules and runtime variable to support flask programs.
1. Setup Windows OS enviornment for python,and pip
 >Put following directory name under OS variable $path,like python directory(eg. c:\Python27) ,and its subdirectory,".\Scripts"(eg.c:\Python27\Scripts).

2. Install virtualenv
 >no matter how many version python have been installed in your OS, only a   single virtualenv is enough.
 * $ pip install virtualenv (python2)
 * $ pip3 install virtualenv (python3)

3. Create Python env
 >Some modules must be installed,such as flask,py2neo,pandas,xlrd,openpyxl.
 we can create a isolated folder for python with dependent modules in following order:
 >1. $ virtualevn flask_py -p "path_to_python.exe"
 >2. $ cd flask_py/Scripts
 >3. $ activate
 >4. $ pip install (module_name), or pip install -r requirements.txt


### Lanuch program
Do following action step by step:
1. lanuch neo4j
2. open Project with pycharm
3. run manage.py
