---
title: Jekyll更换主题后无法启动jekyll serve服务的问题
tags: TeXt
article_header:
  type: cover
---

在使用jekyll搭建博客时，首先使用命令创建一个blog文件夹

    jekyll new blogname

出现以下输出后创建成功。
![](https://raw.githubusercontent.com/Uranuslight/MarkdownPic/master/jekyll%20serve/20200624154632.png)
然后下载[TeXt](https://github.com/kitian616/jekyll-TeXt-theme)主题，解压所有文件并替换进自己的文件夹
此时使用命令开启jekyll服务。

    jekyll serve

大概率会无法成功，报错 Could not find gem 'rake (~> 10.0) x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)，如图所示

![](https://raw.githubusercontent.com/Uranuslight/MarkdownPic/master/jekyll%20serve/20200624122105.jpg)

在查阅[资料](https://jekyllrb.com/docs/themes/)后找到解决方案，在替换文件后应该执行命令

    bundle update

更新完成之后再启动服务即可成功。

![](https://raw.githubusercontent.com/Uranuslight/MarkdownPic/master/jekyll%20serve/20200624155309.png)

![](https://raw.githubusercontent.com/Uranuslight/MarkdownPic/master/jekyll%20serve/20200624155358.png)

<!--more-->
