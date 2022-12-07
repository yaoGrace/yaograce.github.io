---
title: tkinter python图形界面开发
author: 王扣
top: false
cover: false
toc: true
mathjax: false
date: 2022-12-07 00:47:49
img:
coverImg:
password: #a7404cc35e7955968e8ca89099f98d06d30663b8626597a9d9403f13665819f7 # shandian110
summary: "概要"
tags: tkinter
categories:  Tkinter界面应用开发
---

# tkinter模块简介

>Tkinter模块("Tk 接口")是Python的标准Tk GUI工具包的接口.Tk和Tkinter可以在大多数的Unix平台下使用,同样可以应用在Windows和Macintosh系统里.Tk8.0的后续版本可以实现本地窗口风格,并良好地运行在绝大多数平台中。

# 目录结构

1、简单实例
2、Label控件
3、Button控件
4、Entry控件
5、点击按钮输出输入框中的内容
6、Text控件
7、带滚动条的Text
8、Checkbutton多选框控件
9、Radiobutton单选框
10、Listbox控件一
11、Listbox控件二
12、Listbox控件三
13、Listbox四
14、Scale控件
15、Spinbox控件
16、Menu顶层菜单
17、Menu鼠标右键菜单
18、Combobox下拉控件
19、Frame控件
20、表格数据
21、树状数据
22、绝对布局
23、相对布局
24、表格布局
25、鼠标点击事件
26、鼠标移动事件
27、鼠标释放事件
28、进入和离开事件
29、响应所有按键的事件
30、响应特殊按键事件
31、指定按键事件
32、组合按键事件

# 1、简单实例

　下面的代码是创建出一个窗口，其他的操作就在这个平台上进行。执行之后会在桌面弹出一个窗口，窗口的标题就是代码中设置的win.title。这里说一下，我使用的版本是python3.6。后面的内容尽量按顺序看，后面的控件也许用到前面写到的东西。

```python
#!/usr/bin/env python
# -*- coding:utf-8 -*-

import tkinter


# 创建主窗口
win = tkinter.Tk()
# 设置标题
win.title("yudanqu")
# 设置大小和位置
win.geometry("400x400+200+50")

# 进入消息循环，可以写控件

win.mainloop()

```

# 2、Label控件

```python
#!/usr/bin/env python
# -*- coding:utf-8 -*-

import tkinter

win = tkinter.Tk()
win.title("yudanqu")
win.geometry("400x400+200+50")

'''
Label:标签控件,可以显示文本
'''
# win：父窗体
# text：显示的文本内容
# bg：背景色
# fg：字体颜色
# font：字体
# wraplength：指定text文本中多宽之后换行
# justify：设置换行后的对齐方式
# anchor：位置 n北，e东，w西，s南，center居中；还可以写在一起：ne东北方向
label = tkinter.Label(win,
                      text="this is a word",
                      bg="pink", fg="red",
                      font=("黑体", 20),
                      width=20,
                      height=10,
                      wraplength=100,
                      justify="left",
                      anchor="ne")

# 显示出来
label.pack()


win.mainloop()
```

# 3、Button控件
```python
#!/usr/bin/env python
# -*- coding:utf-8 -*-

import tkinter 

def func():
    print("aaaaaaaaaaaaaaaaaaaaaaa") 

win = tkinter.Tk()
win.title("yudanqu")
win.geometry("400x400+200+50") 

# 创建按钮
button1 = tkinter.Button(win, text="按钮", command=func, width=10, height=10)
button1.pack()

button2 = tkinter.Button(win, text="按钮", command=lambda: print("bbbbbbbbbbbb"))
button2.pack()

button3 = tkinter.Button(win, text="退出", command=win.quit)
button3.pack()

win.mainloop()
```

# 4、Entry控件
```python
#!/usr/bin/env python
# -*- coding:utf-8 -*-

import tkinter

win = tkinter.Tk()
win.title("yudanqu")
win.geometry("400x400+200+50")

'''
Entry：输入控件，用于显示简单的文本内容
'''

# 密文显示
entry1 = tkinter.Entry(win, show="*") # show="*" 可以表示输入密码
entry1.pack()

# 绑定变量
e = tkinter.Variable()

entry2 = tkinter.Entry(win, textvariable=e)
entry2.pack()

# e就代表输入框这个对象
# 设置值
e.set("wewewewewewe")
# 取值
print(e.get())
print(entry2.get())

win.mainloop()
```

# 5、点击按钮输出输入框中的内容
```python
#!/usr/bin/env python
# -*- coding:utf-8 -*-
import tkinter

win = tkinter.Tk()
win.title("yudanqu")
win.geometry("400x400+200+50")

def showinfo():
    # 获取输入的内容
    print(entry.get())

entry = tkinter.Entry(win)
entry.pack()

button = tkinter.Button(win, text="按钮", command=showinfo)
button.pack()

win.mainloop()
```

# 