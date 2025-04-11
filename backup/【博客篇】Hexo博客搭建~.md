# 前言

> 关于运用`Github Pages`搭建`Hexo`博客的一些想法~

* 这篇文章将讲述运用`Github Pages`功能搭建`Hexo`博客的基本方法

* 内容包括详细的`Git`和`node`的下载和运用和`Github`的仓库上传

* 不建议使用！第一次失误可能导致后续无法成功！成功后也或多或少有问题~但还是写出来大家可以试试~

  ---

# 开始搭建

> 请按照教程一步一步进行！否则可能报错。

##  准备工具

> 工具处保存路径其他均默认
>
> ---

**[下载nodejs](https://nodejs.org/en/)**

---

**[下载git](https://git-scm.com/downloads)**

---

## 测试下是否都下载成功

管理员运行cmd（在输入cmd后不确定，直接`Ctrl+Shift+Enter`即可），依次输入如下命令

```cmd
node -v
npm -v
git -v
```

## 下载hexo

> 依旧在`cmd`中进行

```cmd
npm install hexo-cli -g
```

## 搭建仓库

成功下载好工具之后，我们开始搭建GitHub存储静态页面的仓库

首先注册/登入[Github](https://github.com/)

点击`Create a new repository`进入新建仓库页面

仓库名输入：用户名.github.io

勾选 `Public`

勾选 `Add a README file`

拉到下面点击`create`创建

## 生成SSH Keys

进入任意文件夹，右键空白处然后点`Git bash here`,输入

```
ssh-keygen -t rsa -C "邮件地址"
```

然后敲4次Enter⌨️

然后进入C:\Users\用户名，在里面进入`.ssh`文件

用记事本打开里面的`id_rsa.pub`,全选复制里面的代码

## 设置Github

打开Github

进入用户设置，找到`SSH keys`

新建`SH keys`名称随意，在下面粘贴代码，

然后创建`SSH keys`

##  测试是否成功

在git bash中输入

> 注意！这里要关闭加速器在输入代码！不然无法连接！
>
> 只能回车一次不然将跳过`yes`导致无法连接!

```
ssh -T git@github.com
```

回车，然后再输入`yes`

## 本地生成博客内容

在喜欢位置新建文件Blog（可自定义文件名），然后进入文件夹

右键空白处然后点`Git bash here`，输入Hexo初始化命令

```
hexo init
```

> 如果‘command not find’，就在前面加上npx，如：`npx hexo init`

然后安装Hexo

```
hexo install
```

接下来使Hexo生成

```
hexo g
```

本地运行Hexo

```
hexo s
```

（如果不成功的话就重复直到成功，因为国内与github连接不稳定）

现在就可以复制生成的链接进入浏览器看到我们生成的本地服务器了

然后回到命令行，`ctrl+c`关闭服务

## 上传博客

进入之前的Blog文件夹，用记事本打开`_config.yml`

拉到最下面将deploy后面的全删掉，复制粘贴这段

```
  type: git
  repository: 
  branch: main
```

> 注意缩进格式：每行前面都有两个空格不要删，每个冒号后面都有个空格也不要删！首行缩进对齐！

去github之前生成的仓库页面，点code，复制https链接

将其粘贴到我们记事本中的`repository：`后面

然后保存退出

**回到博客文件夹，git bash**

## 安装自动部署发布工具

在Blog文件夹右键打开git bash，生成

```
hexo g
```

上传

```
hexo d
```

> 如果是第一次使用git的话会需要配置，不然会报错

```
git config --global user.email "你的邮箱"
```

```
git config --global user.name "你的名字"
```

配置完后再`hexo d`上传

在跳出来的窗口内进行登录（不要乱点，不然错过了很麻烦）

运行后我们就成功把本地内容上传到github了

上传成功以后，我们就算搭建好了！上自己的网址看看吧

网址是我们之前设的仓库名：用户名.github.io

# 网站基本设置

我们的博客标题还是默认的hexo，整个页面是初始默认的，接下来我们对其进行修改

用记事本打开我们blog文件夹中的`_config.yml`文件

将#Site下面按自己的需求填上

```
## Site
title: 标题
subtitle: 副标题
description: 描述
keywords: 关键词
author: 站主
language: 语言（可以填写zh-CN）
timezone: 时区（可以填写Asia/Shanghai）
```

记得保存

# 文章上传

我们在Blog文件夹中打开git bash,输入下方代码就可以生成新的文章md文件

```
hexo new 文章标题
```

文章是.md格式，在我们的Blog文件夹中的`source/_posts`中

推荐用Typora软件来编辑.md格式的文件

> Typora官网：https://www.typoraio.cn/（89元终身使用，推荐正版）
>
> 破解版奉上：[蓝奏云文件](https://kevinwu06.lanzout.com/iXkq30icv1ha)

然后我们用Typora软件打开该.md文件就可以开始写文章了

写好以后，我们还是一样打开git bash生成、上传

```
hexo g
hexo d
```

---

至此，我们就成功搭建好基本的博客了，剩下的就是对博客的一些优化和美化了。

# 博客主题

推荐主题：[Butterfly](https://butterfly.js.org/posts/21cfbf15/)，[anzhiyu](http://docs.anheyu.com/)

大家可以参阅主题文档进行安装配置

---







# 其他博主教程推荐

`Gmeek-html<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=1303633876&bvid=BV1Ju4m1c7WR&cid=1521925412&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>`

---