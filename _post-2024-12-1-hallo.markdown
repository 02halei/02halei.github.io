---
layout:     post
title:      "Hello 2024"
subtitle:   " \"Hello World, Hello Blog\""
date:       2024-12-1
author:     "02halei"
header-img: "img/home.png"
catalog: true
tags:
    - Meta
---

> “Yeah It's on. ”


02halei 的 Blog 就这么开通了。

[跳过废话，直接看技术实现 ](#build) 

2024 年，02halei 总算有个地方可以好好写点东西了。


作为一个喜欢倒腾各种pc的up主

各种b站的教学视频激起了我开博客的冲动。可惜那种开源免费的一直没弄成，自己白嫖来的域名也是没用上，现在终于终于有一个地方能做一些我自己的分享了！


<p id = "build"></p>

## 正文

接下来说说搭建这个博客的技术细节。  

正好之前就有关注过 [GitHub Pages](https://pages.github.com/) + [Jekyll](http://jekyllrb.com/) 快速 Building Blog 的技术方案，非常轻松时尚。

其优点非常明显：

* **Markdown** 带来的优雅写作体验
* 非常熟悉的 Git workflow ，**Git Commit 即 Blog Post**
* 利用 GitHub Pages 的域名和免费无限空间，不用自己折腾主机
	* 如果需要自定义域名，也只需要简单改改 DNS 加个 CNAME 就好了 (当然我那个us.kg的域名好像不能DNS，所以没弄成……)
* Jekyll 的自定制非常容易，基本就是个模版引擎


本来觉得最大的缺点可能是 GitHub 在国内访问起来太慢，没想到github.io的国内访问还算流畅。




---

配置的过程中也没遇到什么坑，基本就是 Git 的流程，相当顺手

大的 Jekyll 主题上直接 fork 了 Clean Blog（这个主题也相当有名，就不多赘述了。唯一的缺点大概就是没有标签支持，于是我给它补上了。）

本地调试环境需要 `gem install jekyll`，结果 rubygem 的源居然被墙了……后来手动改成了我大淘宝的镜像源才成功

Theme 的 CSS 是基于p


## 后记

这个博客也是用的github上的来源模版来搭建的，主要是没那个时间倒腾太多东西(加上可能没有那么专业实力#^_^#)今后的分享都会在b站和博客同步，如果有什么不正确的地方或我的疑问🤔希望大家积极帮忙解决。🙏)

在经历 v1.0 - v1.5 的蜕变后，这个博客主题愈发完整，不但增加了诸多 UI 层的优化（opinionated）；在代码层面，更加丰富的配置项也使得这个主题拥有了更好的灵活性与可拓展性。而作为一个开源项目，我也积极的为其完善文档与解决 issue。

如果你恰好逛到了这里，希望你也能喜欢这个博客主题。

—— Hux 后记于 2015.10
