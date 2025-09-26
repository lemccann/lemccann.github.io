<h1>{{ page.title }}</h1>

<ul>
{% for post in site.teaching %}
  <li>
    {{ post.title }}
    {% if post.type %}
      — {{ post.type }}
    {% endif %}
  </li>
{% endfor %}
</ul>
