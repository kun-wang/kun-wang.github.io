---
layout: default
permalink: /news/
title: News
category: news
---

<section class="inner">

<ul  class="news list-unstyled" style="list-style-type:none;">
{% for item in site.news %}
    {% include news-page.html item=item %}
{% endfor %}
</ul>

</section>