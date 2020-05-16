---
layout: post
title: "Jupyter Notebook remote connection setting"
date: "2018-04-10 11:16:05 +0800"
---

1. generate sha1 password
>* $from notebook.auth import passwd
* $passwd()

2. update config file
>* $jupyter notebook --generate-config
* $vim ~/.jupyter/jupyter_notebook_config.py
* add following lines:
  * c.NotebookApp.ip='*'
  * c.NotebookApp.password = u'sha:ce...刚才复制的那个密文'
  * c.NotebookApp.open_browser = False
  * c.NotebookApp.port =8888 #随便指定一个端口

3. launch notebook at a selected folder
>* $ cd selected_path_offolder
* $jupyter notebook
