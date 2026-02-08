---
layout: archive
title: "Blogs"
permalink: /blog/
author_profile: true
---

{% include base_path %}

{% assign posts_count = site.posts | size %}

{% if posts_count > 0 %}
  {% for post in site.posts %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  <p>No blog posts yet. Check back soon!</p>
{% endif %}
