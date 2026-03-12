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
    <p class="mb-2">{{ profile.about | first }}</p>
    {% if profile.about.size > 1 %}
      <details class="about-more">
        <summary aria-label="Show more about me">
          <span class="about-toggle-label">More</span>
          <span class="about-toggle-icon" aria-hidden="true">&gt;</span>
        </summary>
        {% for paragraph in profile.about offset:1 %}
          <p class="about-extra mb-0">{{ paragraph }}</p>
        {% endfor %}
      </details>
    {% endif %}
  </div>
</section>

<section id="research" class="section-block">
  <h2>Research</h2>
  {% for paragraph in profile.research %}
    <p class="mb-3">{{ paragraph }}</p>
  {% endfor %}
</section>

<section id="contact" class="section-block">
  <h2>Contact</h2>
  <p class="mb-0">{{ profile.contact_name | default: profile.name }}</p>
  <p class="mb-3">{{ profile.role }}</p>
  <p class="mb-0">{{ profile.institution }}</p>
  <p class="mb-0">{{ profile.department }}</p>
  <p class="mb-0">{{ profile.address_line1 }}</p>
  <p class="mb-0">{{ profile.address_line2 }}</p>
  <p class="mb-0"><i class="bi bi-envelope email-icon" aria-hidden="true"></i><span class="visually-hidden">Email:</span> {{ profile.email }}</p>
</section>
