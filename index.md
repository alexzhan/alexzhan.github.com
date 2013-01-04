---
layout: page
title: alexzhan
tagline: 
---
{% include JB/setup %}

这是我在互联网上的一块自留地，用[Jekyllbootstrap](http://jekyllbootstrap.com/)搭建，托管在[Github Pages](http://pages.github.com/)上，将记录我对术的理解、生活的感悟和展示自己的一些作品。

**alexzhan** 是我在互联网上的通用ID，我在 [Twitter](http://twitter.com/alexzhan)、[Github](http://github.com/alexzhan)、[微博](http://weibo.com/alexzhan)、[V2EX](http://www.v2ex.com/member/alexzhan)、[知乎](http://zhihu.com/people/alexzhan) 都使用这个ID，我个人更喜欢twitter，因为工作的原因用微博也比较多，所以找到我的最佳方式就是我的twitter或者微博。

大四的时候用Tornado做了一个开源的大学生社区，18周，代码在[http://github.com/alexzhan/dormforge](http://github.com/alexzhan/dormforge)，上班之后暂停了这个项目的开发和网站的托管，以后有时间和机会或许还会重启这个项目。

现在工作在新浪微博主站研发部，做一些我认为很有意义的研发工作。
### Recent Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
