---
layout: page
title: Under Construction!
tagline: Supporting tagline
---
{% include JB/setup %}

## Testing Page List
<ul>
  {% assign pages_list = site.pages %}
  {% assign group = 'project' %}
  {% include JB/pages_list %}
</ul>

<ul class="posts">
  {% for post in site.posts %}
	{% if post.group == 'project'%}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }} | ({{ post.type }})</a></li>
    {% endif %}
  {% endfor %}
</ul>



