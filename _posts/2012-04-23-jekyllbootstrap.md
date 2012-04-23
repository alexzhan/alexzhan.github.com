---
layout: post
title: "Jekyllbootstrap搭建手记"
description: ""
category: docs 
tags: [jekyll, jekyllbootstrap, ruby, github]
---
{% include JB/setup %}

###Github Pages

github好是好，只是在天朝速度太慢，而且，我现在是教育网+CMCC混用，没用网通，大部分时间都是用教育网，所以速度慢的可想而知。在github上创建alexzhan.github.com这个Repo之后，我并不想在本地直接clone，而是选择了绕道bitbucket，因为bitbucket的速度要快的多。

具体是这样做的：在bitbucket上也建立一个Repo，在本地的Repo指向这个bitbucket上的Repo，我在运行[18周](http://18zhou.openpk.org)的主机上再建立一个Repo也指向bitbucket的Repo，但是主机上的Repo的push地址指向github上的Repo，这样虽然很麻烦，但是每一步速度都是很快的(主机连github速度很快)。当然，当本地连github的速度提升之后就不用这么麻烦了。

###Jekyll Bootstrap

由于github支持Jekyll，所以访问用Jekyllbootstrap搭建的github pages是没有问题的。只是如果以前没有搞过rails的开发的话，在本地要运行起jekyll --server就会有些麻烦。

我的系统是Ubuntu 11.10.首先，需要Ruby 1.9.2:sudo rvm install 1.9.2，我在这一步遇到SSLv2的错误，因为我安装的是Ruby 1.9.2-p180，这个是较早期的版本了，如果是Ruby 1.9.2-p290则不会遇到这个问题。解决办法是：删去这个文件/var/cache/ruby-rvm/src/ruby-1.9.2-p180/ext/openssl/ossl_ssl.c的下面这三行：

    ---
    OSSL_SSL_METHOD_ENTRY(SSLv2),
    OSSL_SSL_METHOD_ENTRY(SSLv2_server),
    OSSL_SSL_METHOD_ENTRY(SSLv2_client),
    ---

重新设置gem的source：用@huacnlee 搭的镜像http://ruby.taobao.org/。之后即可gem install jekyll安装jekyll，运行jekyll --server在4000端口。
