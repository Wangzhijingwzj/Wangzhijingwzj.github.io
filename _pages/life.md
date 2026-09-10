---
layout: archive
title: "Life"
permalink: /life/
author_profile: true

photos:
  - photo-01.jpg
  - photo-02.jpg
---

A collection of photographs from everyday life.

<style>
.life-photo-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
  align-items: start;
}

.life-photo-grid a {
  display: block;
  min-width: 0;
}

.life-photo-grid img {
  display: block;
  width: 100%;
  height: auto;
  margin: 0;
}
</style>

<div class="life-photo-grid">
{% for photo in page.photos %}
  <a href="{{ site.baseurl }}/images/life/{{ photo }}">
    <img
      src="{{ site.baseurl }}/images/life/{{ photo }}"
      alt="Photograph {{ forloop.index }}"
      loading="lazy">
  </a>
{% endfor %}
</div>
