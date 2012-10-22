---
layout: default
title: It is what it is!
tagline: a technical trip
---
<div class="blog-index">  
  {% assign post = site.posts.first %}
  {% assign content = post.content %}
  {% include post_detail.html %}
</div>
<hr>
{% include JB/comments %}
