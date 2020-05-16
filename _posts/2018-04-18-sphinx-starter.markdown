---
layout: post
title: "sphinx starter"
date: "2018-04-18 14:17:23 +0800"
---
1. install sphinx
>it can be installed with several different kinds of method, like:
  1. apt-get install ..
  1. pip install ..
  1. anaconda environment tool

1. create configuration frame work
  1. quick method with command 'sphinx-quickstart'

1. generate rst file manually
  1. sphinx-apidoc [options] -o <outputdir> <sourcedir> [excluded_sourcedir,]

1. theme update(optional)
>step 1. pip install sphinx_rtd_theme
>step 2. import sphinx_rtd_theme
>step 3. html_theme = "sphinx_rtd_theme"
   step 4. html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]

1. generate html document
  >change directory to outputdir, and run command
