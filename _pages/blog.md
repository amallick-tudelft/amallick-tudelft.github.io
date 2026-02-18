---
layout: archive
title: "Blogs"
permalink: /blog/
author_profile: true
---

<style>
.page__content {
  position: relative;
}

.page__content::before {
  content: "";
  position: fixed;
  top: 0;
  right: 0;
  width: 45%;
  height: 100vh;
  background-image: url('/images/Netaji.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  opacity: 0.2;
  z-index: -1;
  pointer-events: none;
}

@media (prefers-color-scheme: dark) {
  .page__content::before {
    opacity: 0.15;
  }
}

@media (max-width: 968px) {
  .page__content::before {
    display: none;
  }
}
</style>

{% include base_path %}

{% assign posts_count = site.posts | size %}

{% if posts_count > 0 %}
  {% for post in site.posts %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  <p>No blog posts yet. Check back soon!</p>
{% endif %}
