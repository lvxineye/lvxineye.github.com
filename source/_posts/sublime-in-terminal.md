title: Mac OSX 在Terminal中使用sublime Text
date: 2015-03-25 14:03:15
categories: Develop tools
tags: [Mac OSX,Terminal,Sublime Text]
---

在Terminal中使用*subl*来打开SublimeText

下载安装好Sublime Text后，已经有了一个在终端下使用的命令:

```
$ open /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl
```

为了能在终端的任何目录下直接使用subl来直接使用Sublime Text，只要把上面的快捷键链接到/usr/bin目录下：

```
$ sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/bin/subl
```