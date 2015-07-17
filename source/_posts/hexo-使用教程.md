title: "hexo 使用教程"
date: 2015-07-01 10:28:37
categories:
tags: [hexo]
---

Hexo 使用教程

## 命令

#### 常用命令

```
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #将.deploy目录部署到GitHub
```

#### 常用复合命令

```
hexo deploy -g
hexo server -g
```

#### 简写

```
hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy
```

## 主题安装

> hexo的主题列表[Hexo Themes](http://github.com/tommy351/hexo/wiki/Themes).

安装主题的方法就是一句git命令：

```
git clone https://github.com/heroicyang/hexo-theme-modernist.git themes/modernist
```

安装完成后，打开hexo\_config.yml，修改主题为modernist

```
theme: modernist
```
