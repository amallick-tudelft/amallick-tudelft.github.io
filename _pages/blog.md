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
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 60%;
  height: 70%;
  background-image: url('/images/Netaji.png');
  background-size: contain;
  background-position: center center;
  background-repeat: no-repeat;
  opacity: 0.12;  /* ADJUST THIS: 0.05 (very faint) to 0.3 (more visible) */
  z-index: -1;
  pointer-events: none;
}

@media (prefers-color-scheme: dark) {
  .page__content::before {
    opacity: 0.05;  /* ADJUST THIS for dark mode */
  }
}

@media (max-width: 968px) {
  .page__content::before {
    width: 80%;
    height: 50%;
    opacity: 0.05;
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
