---
title: "《出洋肄習錄》"
author: "<a href=\"https://jessekelighine.com\"><code>jessekelighine.com</code></a>"
layout: default
---

<nav id="TOC" role="doc-toc">
  <ul>
    <li><a href="#prologue">序</a></li>
    {% for post in site.posts reversed %}
    {% assign anchor = post.anchor | default: post.date | date: "%Y-%m-%d" %}
    {% if post.title and post.title != "Post" %}
    <li><a href="#{{ anchor }}">{{ post.title }}</a></li>
    {% else %}
    <li><a href="#{{ anchor }}">{{ post.date | date: "%Y-%m-%d" }}</a></li>
    {% endif %}
    {% endfor %}
    <li><a href="#comments">留言板</a></li>
  </ul>
</nav>

# 序 {#prologue}

> 奏為擬選聰穎子弟，前赴泰西各國，肄習技藝，以培人才，恭折仰祈聖鑒事。
>
> <p align="right">曾國藩〈擬選子弟出洋學藝折〉同治十年（1871）</p>

單純記錄一些在紐約的所見所聞還有心情，
所以以<ruby><rb>意識流</rb><rp>（</rp><rt>流水帳</rt><rp>）</rp></ruby>的體例寫作。

<!-- POSTS START HERE  -->

{% for post in site.posts reversed %}
{% assign anchor = post.anchor | default: post.date | date: "%Y-%m-%d" %}
{% if post.title and post.title != "Post" %}
<h1 id="{{ anchor }}">{{ post.title }}</h1>
{% else %}
<h1 id="{{ anchor }}">{{ post.date | date: "%Y-%m-%d" }}</h1>
{% endif %}
{{ post.content }}
{% endfor %}

# 留言板 {#comments}

<script src="https://giscus.app/client.js"
        data-repo="jessekelighine/educational-mission"
        data-repo-id="R_kgDOQ_yBnA"
        data-category="General"
        data-category-id="DIC_kwDOLmNjDc4CmBxS"
        data-mapping="number"
        data-term="1"
        data-reactions-enabled="0"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="light"
        data-lang="zh-TW"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
