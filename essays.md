---
layout: page
permalink: /essays/
title: Essays
---

{% for post in site.categories['Essays'] %}
  <article>
    {% include meta.html post=post preview=true %}
    {{ post.excerpt }}
    <div class="more"><a href="{{ post.url | relative_url }}">read more</a></div>
  </article>
{% endfor %}
