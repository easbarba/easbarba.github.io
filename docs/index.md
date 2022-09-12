---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
Title: Home Page
layout: default
---
Hi, i'm Alex Barbosa.

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
