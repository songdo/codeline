---
layout: default
title: "data-structure"
date: 2017-03-06 15:23
comments: true
sharing: true
footer: true
#下面为添加的内容
description: "宋源的个人博客之数据结构部分"
keywords: 数据结构，data-structure
---

<!--首页展示博客-->
<div class="blog-index">
  {% assign index = true %}
  {% for post in site.posts %}
  {% if post.categories contains 'data-structure' %}
  {% assign content = post.content %}
    <article>
      {% include article.html %}
    </article>
  {% endif %}
  {% endfor %}
  <!--分页-->
  <div class="pagination">
    {% if paginator.next_page %}
      <a class="prev" href="{{paginator.next_page_path}}">&larr; Older</a>
    {% endif %}
    <a href="/blog/archives">Blog Archives</a>
    {% if paginator.previous_page %}
    <a class="next" href="{{paginator.previous_page_path}}">Newer &rarr;</a>
    {% endif %}
  </div>
</div>

<aside class="sidebar">

</aside>
