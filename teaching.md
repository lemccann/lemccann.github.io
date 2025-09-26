---
title: "Teaching"
permalink: /teaching/
author_profile: true
---
<div style="padding-bottom: 3em;"> <!-- adds space after entire section -->

  <h2>Instructor of Record</h2>
  {% for post in site.teaching %}
    {% if post.role == "Instructor" %}
      <div style="margin-bottom: 2.5em;"> <!-- increased spacing between posts -->
        <strong>{{ post.title }}</strong> — {{ post.type }}
        {% if post.badge %}
          <span style="background-color: #f0f0f0; border-radius: 4px; padding: 2px 6px; font-size: 0.85em; margin-left: 6px;">
            {{ post.badge }}
          </span>
        {% endif %}
        {% if post.semester %}
          <div><em>{{ post.semester }}</em></div>
        {% endif %}
        <div>{{ post.content }}</div>
      </div>
    {% endif %}
  {% endfor %}

  <h2>Teaching Assistant</h2>
  {% for post in site.teaching %}
    {% if post.role == "TA" %}
      <div style="margin-bottom: 2.5em;"> <!-- consistent spacing for TA posts -->
        <strong>{{ post.title }}</strong> — {{ post.type }}
        {% if post.badge
