---
layout: page
permalink: /technology/
title: Technology
---

{% for post in site.categories['Poetry'] %}
  <article>
    {% include meta.html post=post preview=true %}
    {{ post.excerpt | truncatewords: 124}}
    <div class="more"><a href="{{ post.url | relative_url }}">read more</a></div>
  </article>
{% endfor %}
