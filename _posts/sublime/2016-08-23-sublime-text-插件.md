---
title: "sublime text插件管理器Package Control"
excerpt: "插件是sublime text的一个很好的特性，跟大多数编辑器一样，可以对编辑器进行很好的扩展。"
categorys: sublime
tags: [sublime]
layout: post
---


今天说下sublime text编辑器的插件。
插件是sublime text的一个很好的特性，跟大多数编辑器一样，可以对编辑器进行很好的扩展。
下面说下如何安装插件：

首先要想安装插件，就必须先安装package control包管理器。

复制以下代码：

```
import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

上面是sublime text3的，sublime text2的可以访问这个链接获取[https://packagecontrol.io/installation#st2](https://packagecontrol.io/installation#st2)

复制好后在sublime text的菜单栏点击 `View > Show Console` ,将内容粘贴到下面的输入框中然后回车，安装好后会在菜单`Preferences`下看到`Package Control`的选项。如果没有请重启下编辑器。

现在`Package Control`已经安装好了，下面说下如何使用`Package Control`安装插件:

* 点击菜单 `Preferences > Package Control` 选择`Install Packages`然后回车，等待几秒后会列出一个插件的列表，你可以选择一个或者输入插件名称然后回车安装
* 或者按`Ctrl` + `Shift` + `P` 打开命令面板，输入`Package Control:Install Packages`回车，输入插件名称回车。