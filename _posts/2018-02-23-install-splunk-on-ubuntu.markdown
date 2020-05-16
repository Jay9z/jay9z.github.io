---
layout: post
title: "install splunk on Ubuntu"
date: "2018-02-23 01:32:59 +0800"
---
Download splunk package file .deb
then, run following command to install splunk:
>sudo dpkg -i Downloads/splunk-6.6.3-e21ee54bc796-linux-2.6-amd64.deb

After installing, start splunk server by this command:
>sudo /opt/splunk/bin/splunk start
