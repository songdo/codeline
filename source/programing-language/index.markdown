---
layout: default
title: "programing-language"
date: 2017-03-06 15:24
comments: true
sharing: true
footer: true
#下面为添加的内容
description: "宋源的个人博客之编程语言部分"
keywords: 编程语言，programing-language
---

<!--首页展示博客-->
<div class="blog-index">
  {% assign index = true %}
  {% for post in site.posts %}
  {% if post.categories contains 'programing-language' %}
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
