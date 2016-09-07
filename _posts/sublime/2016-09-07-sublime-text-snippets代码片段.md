---
title: "sublime text snippets代码片段"
excerpt: "当你发现你经常重复写一些相同的或者类似的代码时，你应该考虑使用下sublime text编辑器的snippets功能。该功能能显著提高我们的开发效率。snippet就是为一段代码片段设置一个名称，然后在文件中输入该名称再按Tab键就会生成设定的代码片段，且支持占位符的功能。"
category: sublime
tags: [sublime]
layout: post
---

当你发现你经常重复写一些相同的或者类似的代码时，你应该考虑使用下sublime text编辑器的snippets功能。该功能能显著提高我们的开发效率。snippet就是为一段代码片段设置一个名称，然后在文件中输入该名称再按Tab键就会生成设定的代码片段，且支持占位符的功能。

#### 如何创建snippets

依次点击菜单栏中的 `Tools` - `Developer` - `New Snippet` ,会在新页面中打开一个xml格式的文件。

类似下面的：

```xml
<snippet>
     <content><![CDATA[
Hello, ${1:this} is a ${2:snippet}.
]]></content>
     <!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
     <!-- <tabTrigger>hello</tabTrigger> -->
     <!-- Optional: Set a scope to limit where the snippet will trigger -->
     <!-- <scope>source.python</scope> -->
</snippet>
```

下面对xml文件的各个标签进行说明：

##### content 

`<content>`标签里面的内容是要生成的代码片段, 这里是要生成`Hello, this is a snippet.`这样一串字符，其中`${1:this}`表示当片段生成后光标会定位到`this`的后面，且`this`为选中状态，当再次按下`Tab`键时光标会定位到`snippet`单词的后面，且为选中状态。

##### tabTrigger

`<tabTrigger>`标签为设置触发字符，使用时可以将其注释去掉。例如这里设置的触发字符是`hello`，那么当我们输入字符`hello`后按`Tab`键的话就会生成代码片段`Hello, this is a snippet.`，我们也可以将其改为其他字符，以容易记忆为原则。

##### scope

`<scope>`标签是设置该`snippet`的作用范围，就是在什么类型的文件中可以使用这个`snippet`。

文件类型及其对应的scope如下：

```
ActionScript: source.actionscript.2
AppleScript: source.applescript
ASP: source.asp
Batch FIle: source.dosbatch
C#: source.cs
C++: source.c++
Clojure: source.clojure
CoffeeScript: source.coffee
CSS: source.css
D: source.d
Diff: source.diff
Erlang: source.erlang
Go: source.go
GraphViz: source.dot
Groovy: source.groovy
Haskell: source.haskell
HTML: text.html(.basic)
JSP: text.html.jsp
Java: source.java
Java Properties: source.java-props
Java Doc: text.html.javadoc
JSON: source.json
Javascript: source.js
BibTex: source.bibtex
Latex Log: text.log.latex
Latex Memoir: text.tex.latex.memoir
Latex: text.tex.latex
LESS: source.css.less
TeX: text.tex
Lisp: source.lisp
Lua: source.lua
MakeFile: source.makefile
Markdown: text.html.markdown
Multi Markdown: text.html.markdown.multimarkdown
Matlab: source.matlab
Objective-C: source.objc
Objective-C++: source.objc++
OCaml campl4: source.camlp4.ocaml
OCaml: source.ocaml
OCamllex: source.ocamllex
Perl: source.perl
PHP: source.php
Regular Expression(python): source.regexp.python
Python: source.python
R Console: source.r-console
R: source.r
Ruby on Rails: source.ruby.rails
Ruby HAML: text.haml
SQL(Ruby): source.sql.ruby
Regular Expression: source.regexp
RestructuredText: text.restructuredtext
Ruby: source.ruby
SASS: source.sass
Scala: source.scala
Shell Script: source.shell
SQL: source.sql
Stylus: source.stylus
TCL: source.tcl
HTML(TCL): text.html.tcl
Plain text: text.plain
Textile: text.html.textile
XML: text.xml
XSL: text.xml.xsl
YAML: source.yaml
```

##### description

还有一个标签在上面的示例中没有显示出来，那就是`<description>`标签，这个是对`snippet`的描述，显示的位置如下：

![snippet](/images/articles/sublime/snippet.png)

如果没有设置`<description>`标签，则该位置会显示该`snippet`保存时的文件名。

#### 如何保存snippet

编辑好该`snippet`文件后，保存文件，选择保存路径为你的`Packages > User > snippet`目录下，扩展名为`.sublime-snippet`。

#### 如何使用snippet

* 直接输入`<tabTrigger>`标签中的值后按`Tab`键。

* 点击菜单`Tools > Snippets`弹出snippet列表，点击相应的snippet即可。

如果按`Tab`键没有效果，或弹出的snippet列表中没有设置的snippet，请检查该snippet是否设置了scope。
