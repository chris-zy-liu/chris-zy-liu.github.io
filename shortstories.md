---
layout: page
permalink: /shortstories/
title: Short Stories
---

{% for post in site.categories['Short Stories'] %}
  <article>
    {% include meta.html post=post preview=true %}
    {{ post.excerpt }}
    <div class="more"><a href="{{ post.url | relative_url }}">read more</a></div>
  </article>
{% endfor %}
