---
title: "Teaching"
permalink: /teaching/
author_profile: true
---
<div>

  <h2>Instructor of Record</h2>
  {% for post in site.teaching %}
    {% if post.role == "Instructor" %}
      <div style="margin-bottom: 1.5em;">
        <strong>{{ post.title }}</strong> — {{ post.type }}
        {% if post.badge %}
          <span style="background-color: #f0f0f0; border-radius: 4px; padding: 2px 6px; font-size: 0.85em; margin-left: 6px;">
            {{ post.badge }}
          </span>
        {% endif %}
        {% if post.semester %}
          <div><em>{{ post.semester }}</em></div>
        {% endif %}
        <!-- Only space between the last field and content -->
        <div style="margin-top: 1em;">{{ post.content }}</div>
      </div>
    {% endif %}
  {% endfor %}

  <h2>Teaching Assistant</h2>
  {% for post in site.teaching %}
    {% if post.role == "TA" %}
      <div style="margin-bottom: 1.5em;">
        <strong>{{ post.title }}</strong> — {{ post.type }}
        {% if post.badge %}
          <span style="background-color: #f0f0f0; border-radius: 4px; padding: 2px 6px; font-size: 0.85em; margin-left: 6px;">
            {{ post.badge }}
          </span>
        {% endif %}
        {% if post.semester %}
          <div><em>{{ post.semester }}</em></div>
        {% endif %}
        {% if post.instructor %}
          <div style="color: #777; font-size: 0.85em; margin-top: 2px;">
            <em>Instructor: {{ post.instructor }}</em>
          </div>
        {% endif %}
        <!-- Only space between the last field and content -->
        <div style="margin-top: 1em;">{{ post.content }}</div>
      </div>
    {% endif %}
  {% endfor %}

</div>
