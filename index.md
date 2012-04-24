---
layout: page
title: alexzhan
tagline: 
---
{% include JB/setup %}

这是我在互联网上的一块自留地，用[Jekyllbootstrap](http://jekyllbootstrap.com/)搭建，部署在[Github Pages](http://pages.github.com/)上，将记录我对术的理解、生活的感悟和展示自己的一些作品。

**alexzhan** 是我在互联网上的通用ID，我在 [Twitter](http://twitter.com/alexzhan)、[Github](http://github.com/alexzhan)、[微博](http://weibo.com/alexzhan)、[V2EX](http://www.v2ex.com/member/alexzhan)、[知乎](http://zhihu.com/people/alexzhan) 都使用这个ID。

用Tornado做了一个开源的大学生社区，[18周](http://18zhou.openpk.org)，代码在[http://github.com/alexzhan/dormforge](http://github.com/alexzhan/dormforge)。

正在做毕业设计，课题是移动设备程序与服务器端程序的通信，我希望能最终做出一个面向Android设备的通用通信组件，类似[Parse](http://parse.com)。
### Recent Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
