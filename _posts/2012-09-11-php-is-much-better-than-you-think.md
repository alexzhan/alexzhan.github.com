---
layout: post
title: "PHP比你想象的好的多"
description: ""
category: 
tags: [PHP, web, language, ecosystem, platform]
---
{% include JB/setup %}

有很多对于PHP的抱怨，甚至这些抱怨也出自很多聪明的人。当Jeff Atwood写下对于PHP的另一篇抱怨[文章](http://www.codinghorror.com/blog/2012/06/the-php-singularity.html)之后，我思考了下PHP的好的方面。

这些抱怨最大的问题是他们出自很多仍在使用旧版本PHP的人。他们或许是不愿意关心或许是不愿意承认PHP不管在语言层面还是在社区层面都在以很快的速度演变。实际上它比任何其他语言或者web平台都演变的快。尽管并不总是如此，但是过去的五年PHP经历了一个惊人的历程。

在说最近PHP社区取得的惊人成就之前，我们先来看看一些有趣的数字：PHP被77.9%的服务端编程语言已知的网站使用。Wordpress被全世界16.6%的网站使用。使用率最高的三个CMS建站系统是：第一的Wordpress份额为54.3%，第二的Joomla份额为9.2%，第三的Drupal份额为6.8%。这三个产品都是用PHP写的。

PHP一定做了一些正确的事，不是吗？

现在，我来告诉你吧，PHP的绝技在于：尽管经过了这么多年的变化，PHP对于非技术人员依然是最容易学习的语言，它让人可以比其他技术更快地建立动态网站，也让人没有麻烦地托管网站。PHP可能不是这个世界上设计最好的语言，但是它能让你完成事情(get things done)，这一点是毋庸置疑的。

###PHP语言

PHP5.0（2004年发布）带来了很实用的对象模型...等等，我在说8年前发布的东西。快进到现在的PHP5.4，即PHP最近的版本，带来了对于现代web语言你梦寐以求的东西：是的，PHP支持了命名空间(namespaces)；是的，PHP支持闭包(closure)；是的，PHP支持traits。

尽管需要花费一些时间，但是PHP5.4带来了一些语法糖使得整体体验比以往更好：是的，PHP支持用\[ ]定义数组；是的，PHP支持新创建的对象这样调用函数：(new Foo())->bar()；是的，PHP支持数组这样获取元素：$foo->bar()\[1]。

PHP甚至向它自己曾犯过的错误学习：register_globals 和 magic_quotes被彻底删除了。

PHP有了内置web服务器以方便本地测试，它能以微秒级的速度启动。

接下来的挑战:我们怎样更新在网络上的讲解PHP的教程？在PHP程序中最好的支持WebSocket的技术是什么？

###PHP生态系统

拥有一个好的语言是很好的，但是拥有一个好的生态系统更棒。在过去的几年PHP生态系统演变了很多。

####Git

对于Git我不想讨论太多，Git被到处使用，PHP很快拥抱了Git。几乎所有PHP类库、框架和产品都在使用Git，包括PHP本身。

####Composer

两年前，我想去掉我在symfony 1中hack的丑陋PEAR代码以支持插件。我想替换成能管理项目依赖的东西，而不是一个像PEAR一样的整体的安装，所以我试着寻找能管理软件依赖的最佳的算法。我几乎尝试了所有可能：从Perl到Ruby，从Debian到Redhat。结果没有让我满意的，只有我自己的解决方案恰巧能工作...当然这只是我的经验只谈。之后我偶然发现了[ZYpp](http://en.wikipedia.org/wiki/ZYpp)，就是它了。ZYpp使用[布尔可满足性问题](http://en.wikipedia.org/wiki/Boolean_satisfiability_problem)解来管理依赖。多亏了[Nils Adermann](http://www.naderman.de/)和[Jordi Boggiano](http://seld.be/)的辛苦工作，PHP现在有了做好的管理依赖的工具--[Composer](http://getcomposer.org/)。

是的，PHP比其他语言有了更好的依赖管理工具。

由于有了Git，Composer，和PHP内置web服务器，我们更容易下载/测试/安装一个PHP项目。

想测试Symfony（使用PHP5.4）？

    $ composer.phar create-project symfony/framework-standard-edition
    $ cd framework-standard-edition
    $ ./app/console server:run

想测试Silex？

    $ composer.phar create-project fabpot/silex-skeleton
    $ cd silex-skeleton
    $ php -S localhost:8888 -t web/

还不知道Composer？你应该了解下它了。

浏览下主要的Composer仓库[Packagist](http://packagist.org/packages/)，它已经拥有1900多个包，且它们在不到三个月的时间里被安装了上百万次。

接下来的挑战：在下一个PHP版本里内置Composer？

####合作

社区合作是本文说的重点，也是我最引以为豪的地方。我们开始看到PHP项目中更好的合作，甚至大项目也是如此，大到你可以忽略其他项目了。

phpBB，Drupal，ez Publish，Symfony，和很多其他项目（比如phpDocumentor, PHPUnit, Behat, Zikula, Propel, Doctrine, Midgard等等）都在共享代码。是的，他们彼此是竞争者，但是他们都理解彼此合作是很重要的。Composer能很好地促进这种合作。

接下来的挑战：说服更多的项目加入这个趋势中来。

###结论

让我再重申一次，PHP可能不是最好的编程语言，我也是第一个说出它的怪处的，但是PHP是迄今为止最好的web平台。


*说明：本文译自[PHP is much better than you think](http://fabien.potencier.org/article/64/php-is-much-better-than-you-think)*
*译者微博：[@alexzhan](http://weibo.com/alexzhan)*
