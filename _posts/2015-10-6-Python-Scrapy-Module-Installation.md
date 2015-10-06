---
layout:post
title:Python爬虫架构Scrapy的安装
categories:
- Python
- Scrapy
- Mac
tags:
- Python
- Scrapy
- 安装
- 爬虫
---

	

	最近在做一个Python爬虫的东西，在Scrapy这个工具的安装上，出现了一些问题。这里把解决办法记下来。

1. 第一个问题：Scrapy所依赖的lxml包无法安装。
   
   解决办法：
   
   ``` 
   sudo CPATH=/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.9.sdk/usr/include/libxml2 CFLAGS=-Qunused-arguments CPPFLAGS=-Qunused-arguments pip install lxml
   ```
   
   直接利用pip install lxml会遇到权限、路径等问题。
   
2. 第二个问题：在安装Twisted时，遇到下面这个问题：
   
   ``` 
   OSError: [Errno 1] Operation not permitted: ‘/tmp/pip-nIfswi-uninstall/System/Library/Frameworks/Python.framework/Versions/2.7/Extras/lib/python/six-1.4.1-py2.7.egg-info'
   ```

	这个错误，是在最新的OSX EI Captain上才有的错误，原因在于新系统的System Integrity Protection特性。我们需要关闭这个特效。

	解决办法：我们进入Recovery mac模式下，打开工具（utilities）里面的终端（terminal），利用命令csrutil disable来关闭之。最后再在Terminal中输入sudo -s pip install等相关命令进行安装。

