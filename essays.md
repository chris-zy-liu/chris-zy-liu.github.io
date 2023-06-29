---
layout: page
permalink: /technology/
title: Technology
---

{% for post in site.categories['Technology'] %}
  <article>
    {% include meta.html post=post preview=true %}
    {{ post.excerpt }}
    <div class="more"><a href="{{ post.url | relative_url }}">read more</a></div>
  </article>
{% endfor %}
