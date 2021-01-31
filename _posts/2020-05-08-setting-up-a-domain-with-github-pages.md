---
layout: post
title: GitHub Pages 绑定来自阿里云的域名
categories: [howto]
tags: how to, github pages
---

## 简介

我在阿里云上注册了一个新域名：[kunwang.info](https://kunwang.info)，我已经在GitHub Pages上建立了自己的博客：[kun-wang.github.io](http://kun-wang.github.io)。现在我希望将`kunwang.info`映射到`kun-wang.github.io`。主要参考资料：

1. [Setting up a custom domain with GitHub Pages][1]
2. [创建GitHub技术博客全攻略][2] - 第九部分：CNAME绑定域名
3. [Hexo在github上构建免费的Web应用][5] - 第4.3节：设置域名

## 第一步：创建CNAME文件夹

在你的个人博客仓库的根目录中新建文件`CNAME`（注意没有后缀），在该文件增加一行文字，告诉Github Pages服务器你想指定的域名。该域名不能包含前缀信息，即不能添加`http:\\`前缀。

> !重要补充！CNAME文件名一定要大写，否则Github Pages服务器无法识别和解析。我就出现了这样的问题。我的CNAME绑定域名是正确的，通过`ping kunwang.info`和`ping kun-wang.github.io`两条指令，我发现了他们都指向同一个IP地址（即我的博客IP地址），可是我在使用浏览器访问的时候，会出现`Site not Found`提示，这个时候我就只能合理的怀疑Github Pages服务器根本就没有把`kunwang.info`和`kun-wang.github.io`绑定起来，即我的CNAME文件设置错误。Google之后发现CNAME文件名的大小写会产生影响（[My custom domain isn't working][4]），万恶的Windows系统不区分文件名大小写，所以即使你在本地更改了CNAME大小写然后push到github，还是没有用。。。我就只好到github上去修改成大写了。。。坑。。。

每个CNAME文件能且只能指定一个域名。更多关于增加CNAME文件的信息可见[Adding a CNAME file to your repository][3]。

第一步的目的是，Github读取你的CNAME之后，Github服务器会设置`kunwang.info`为你的主域名，然后将`kun-wang.github.io`重定向到`kunwang.info`。

## 第二步：CNAME绑定域名

登录[阿里云单域名控制台](http://dc.aliyun.com/login/loginx)，在`域名解析`中添加如图所示的解析

![域名解析]({{ site.url }}/images/posts/post-setting-up-a-domain-with-github-pages-1.png)

默认使用阿里云提供的万网DNS服务器。当然你也可以使用[DNSPOD](https://www.dnspod.cn/)提供的DNS服务器，这样可以使你的域名在国外更快速的传播。当你使用DNSPOD提供的DNS服务器时，除了DNS服务器不一样以外，其他的设置（比如A记录和CNAME记录）均相同。以下我们简要分析我们所添加的A记录和CNAME记录的含义。

在域名解析中，A记录就是直接指定一个IP，CNAME就是重命名，指向另一个域名。

1. 在阿里云控制台，设置主机记录`www`，记录类型为A，记录值是IP`192.30.252.153`。其中`192.30.252.153`是Github Pages服务器指定的IP地址，访问该IP地址即表示访问Github Pages。
2. 在阿里云控制台，设置主机记录`www`，记录类型为A，记录值是IP`192.30.252.154`。同上。
3. 在阿里云控制台，设置主机记录`@`，记录类型为CNAME，记录值是`kun-wang.github.io.`。表示将`http://kunwang.info`这个主域名映射`kun-wang.github.io`。在这里千万不要忘记记录值中`.io`后面还有一个点`.`！
+ 但是很多时候，我们只想将子域名绑定到博客地址。比如如果你想将`blog.maindomain.com`（即博客子域名地址，主域名地址是`www.maindomain.com`）映射到`kun-wang.github.io`，那么在主机记录中就应该填写`blog`，记录类型为CNAME，记录值是`kun-wang.github.io`。因为你的主域名已经默认为`maindomain.com`，所以主域名和主机记录合起来就是`blog.maindomain.com`。而且这个时候，你github项目的CNAME文件内容也应该相应的改为`blog.maindomain.com`，因为你是想将`kun-wang.github.io`和`blog.maindomain.com`绑定起来，而不是和`www.maindomain.com`绑定。
+ 如果你想将`www.maindomain.com`（即主域名地址）映射到`kun-wang.github.io`，那么主机记录就是`www`,记录类型是A，记录值是具体的IP地址（在我们这个例子中是`192.30.252.153`、`192.30.252.154`）。因为你的主域名已经默认为`maindomain.com`，所以主域名和主机记录合起来就是`www.maindomain.com`。

你可以将多个域名都映射到`xxxxx.github.io`之类的你自己的站点上，但是需要新建不同内容的CNAME文件。

注意，`.me`已经是顶级域名（和`.com`、`.org`等域名是同一级的），所以需要使用A记录进行域名解析。

第二步的目的是，告诉所有DNS服务器，对于`kunwang.info`的访问都会被重定向到`kun-wang.github.io`。

## 第三步：漫长的等待

要全球解析生效，得等上一会了，也可以先ping一下自己的设置对不对。阿里云域名服务的工作原理是，在你更新了域名解析之后，首先是阿里的万网云解析，然后传播到各大运营商的DNS服务器，刷新DNS缓存，至此你的域名可以被访问。

[1]: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/
[2]: http://blog.csdn.net/renfufei/article/details/37725057
[3]: https://help.github.com/articles/adding-a-cname-file-to-your-repository/
[4]: https://help.github.com/articles/my-custom-domain-isn-t-working/
[5]: http://blog.fens.me/hexo-blog-github/