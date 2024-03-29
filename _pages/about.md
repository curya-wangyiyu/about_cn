---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>
{% include_relative includes/intro.md %}

<span class='anchor' id='-educations'></span>
{% include_relative includes/educations.md %}

<span class='anchor' id='-news'></span>
{% include_relative includes/news.md %}

<span class='anchor' id='-publications'></span>
<div id="publications">
  <!-- 这里将会插入另一个repo的publications.md内容 -->
</div>

<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<script>
fetch('https://raw.githubusercontent.com/curya-wangyiyu/curya-wangyiyu.github.io/main/_pages/includes/publications.md')
  .then(response => response.text())
  .then(text => {
    // 使用 marked.js 解析 Markdown
    const html = marked(text);
    // 将解析后的 HTML 插入到页面中
    document.getElementById('publications').innerHTML = html;
  });
</script>

<span class='anchor' id='-internships'></span>
{% include_relative includes/internships.md %}

<span class='anchor' id='-honors-and-awards'></span>
{% include_relative includes/honors.md %}

<span class='anchor' id='-others'></span>
{% include_relative includes/others.md %}