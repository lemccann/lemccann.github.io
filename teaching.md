---
title: "Teaching"
permalink: /teaching/
author_profile: true
---


<!-- Instructor of Record Section -->
<h2>Instructor of Record</h2>
<ul>
{% for post in site.teaching %}
  {% if post.role == "Instructor" %}
    <li>
      {{ post.title }}
      {% if post.type %} — {{ post.type }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

<!-- Teaching Assistant Section -->
<h2>Teaching Assistant</h2>
<ul>
{% for post in site.teaching %}
  {% if post.role == "TA" %}
    <li>
      {{ post.title }}
      {% if post.type %} — {{ post.type }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

