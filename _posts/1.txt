---
layout: post
description: 使用 Jekyll 发布 Github Pages
image: assets/images/githubp.png
comments: true
author: sal
---

> Jekyll + GitHub Pages 本以为很简单，但就是让我折腾了一天，还什么都没有学到，所以在这里来描述一些心里的感受。

之前已经搭建过WordPress博客系统，可惜的是没有自己的域名，所以现在就开始尝试着使用GitHub Pages+Jekyll。虽然已经做了好长时间的程序员，但看了官方文档后还是不太明白这两个东西是怎么结合到一起来的，所以还是找到一些教程这才慢慢的上路了。

首先安装 Jekyll 如下所示：

```bash
#安装 Ruby 和 Gem
brew install ruby
#安装 bundler jekyll
gem install bundler jekyll
```

其中 bundler 是一个 gem 包依赖管理工具，即在 Gemfile 中申明的包，使用 bundle install 即可。

好了，现在不急着新建 GitHub Pages 仓库，一般我选择安装好一个博客框架后，然后就是去安装各种主题，这次我也是一样，但是这个 Jekyll 主题安装让我很是头疼。刚刚接触这个，对这个主题结构还不是很熟悉，还没有什么一键安装配置的界面，所以我在这里踩了很多的坑，这里我就总结一下我最后安装主题的方法(很笨)。

去[JekyllTheme](http://jekyllthemes.org)找一个自己喜欢的主题，我比较喜欢简洁的，就是图片很少，居中文章标题的那种比如[Kiko](https://github.com/gfjaru/Kiko)，然后就是直接克隆到一个目录：

```bash
#克隆主题
git clone https://github.com/gfjaru/Kiko
cd Kiko
#安装依赖并启动
bundle install
jekyll serve
```

现在可以查看主题效果，之后就可以新建自己的GitHub Pages仓库了，假定用户名为 user，那么仓库的地址为https://github.com/user/user.github.io.好了现在可以开始了：

```bash
#移除之前克隆的 remote
git remote remove origin
#添加自己的 remote 
git remote add origin https://github.com/user/user.github.io
#更新
git pull origin master

