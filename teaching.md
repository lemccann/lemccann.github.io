---
title: "Teaching"
permalink: /teaching/
author_profile: true
---

<!-- Instructor of Record Section -->
<h2>Instructor of Record</h2>
<div class="teaching-section">
{% for post in site.teaching %}
  {% if post.role == "Instructor" %}
    <div class="course-entry">
      <p><strong>{{ post.title }}</strong>{% if post.type %} — {{ post.type }}{% endif %}</p>
      <div class="course-desc">
        {{ post.content | markdownify }}
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>

<!-- Teaching Assistant Section -->
<h2>Teaching Assistant</h2>
<div class="teaching-section">
{% for post in site.teaching %}
  {% if post.role == "TA" %}
    <div class="course-entry">
      <p><strong>{{ post.title }}</strong>{% if post.type %} — {{ post.type }}{% endif %}</p>
      <div class="course-desc">
        {{ post.content | markdownify }}
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>
