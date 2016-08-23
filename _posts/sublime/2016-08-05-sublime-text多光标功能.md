---
title: "sublime text 多光标 Multiple Selections"
excerpt: "前段时间投入到subliem text的阵营了，因为发现sublime text有许多非常好的特性，今天我们来了解下sublime text的多光标特性。"
categorys: sublime
tags: [sublime]
layout: post
---

## sublime text 多光标 Multiple Selections

前段时间投入到subliem text的阵营了，因为发现sublime text有许多非常好的特性，今天我们来了解下sublime text的多光标特性。

本人环境：

* windows 10
* sublime text 3

---

sublime text 的多光标功能是我以前在其他编辑器中未曾见过的，所谓的多光标就是在同一编辑文件中可以有多个闪动的光标，即我们可以同时编辑多处位置。

### 如何添加光标

---

* `Ctrl` + 鼠标左键

按住`Ctrl`键的同时，在你想添加光标的位置点击鼠标左键即可添加一个光标。

* `Ctrl` + `Alt` + 上下方向键

按住`Ctrl` + `Alt`的同时按上方向键或下方向键，就会在上一行或下一行添加光标。

* `Ctrl` + `D`

按`Ctrl` + `D`键之前要先选中一段字符，然后按`Ctrl` + `D`，就会从当前光标向后查找与你选中的字符相同的字符，找到后就选中该字符并添加一个光标。

* `Ctrl` + `Shift` + `L`

使用`Ctrl` + `Shift` + `L`之前要先使用`Ctrl` + `L`组合键选中想要编辑的行（`Ctrl` + `L`是选中当前行快捷键，按一下会向下再选中一行），然后按`Ctrl` + `Shift` + `L`组合键就会在每行的末尾添加光标

### 如何删除光标

---

* 删除全部光标

删除多光标只要鼠标左键点击任何位置多光标就会消失,或按`Esc`键。

* 删除多光标中的某一个光标

如果想删除多光标中的某一个光标只要按住`Alt` + `Shift` + 鼠标**右**键点击想删除的光标即可。

### 使用技巧

---

#### 将多行合并为一行

`Ctrl` + `J` 快捷键可以将光标所在行和其下一行合并为一行，但如果想将多行合并为一行就需要多次按`Ctrl` + `J`快捷键。下面说下一个更简便的方法，首先根据上面说到的设置多光标的方法将需要合并为一行的行添加光标(不包括最后一行)，然后再按`Ctrl` + `J`快捷键。