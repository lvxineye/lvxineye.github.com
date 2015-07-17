title: android studio启动时跳过fetching Android sdk component information方法
date: 2015-03-25 15:54:27
categories: Develop tools
tags: [Mac OSX,Android Studio]
---
Android Studio启动时经常会停留在Fetching Android sdk component infromation。

```
- 进入刚安装的Android Studio目录下的bin目录。找到idea.properties文件，用文本编辑器打开。
- 在idea.properties文件末尾添加一行： disable.android.first.run=true ，然后保存文件。
- 关闭Android Studio后重新启动，便可进入界面。
```
