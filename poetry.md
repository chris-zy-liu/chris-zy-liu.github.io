---
layout: page
permalink: /poetry/
title: Poetry
---

<div class="posts">
  {% for post in site.categories['Poetry'] %}
     <article>
    	{% include meta.html post=post preview=true %}
    	{{ post.excerpt }}
    	<div class="more"><a href="{{ post.url | relative_url }}">read more</a></div>
     </article>
  {% endfor %}
</div>
