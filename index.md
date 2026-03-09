---
layout: default
title: Home
---

{% assign profile = site.data.profile %}

<section class="row g-4 align-items-start mb-4 mb-md-5">
  <div class="col-12 col-md-4 col-lg-3">
    <img
      src="{{ profile.image | relative_url }}"
      alt="{{ profile.image_alt }}"
      class="img-fluid portrait border border-dark-subtle"
      loading="lazy"
    >
  </div>
  <div class="col-12 col-md-8 col-lg-9">
    <h1 class="display-name mb-2">{{ profile.main_name | default: profile.name }}</h1>
    <p class="mb-3">{{ profile.institution }}</p>
    {% for paragraph in profile.about %}
      <p class="mb-3">{{ paragraph }}</p>
    {% endfor %}
  </div>
</section>

<section id="contact" class="section-block">
  <h2>Contact</h2>
  <p class="mb-1">{{ profile.contact_name | default: profile.name }}</p>
  <p class="mb-1">{{ profile.institution }}</p>
  <p class="mb-1">Email: <a href="mailto:{{ profile.email }}">{{ profile.email }}</a></p>
</section>
