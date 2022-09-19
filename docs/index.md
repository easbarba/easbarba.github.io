---
Title: Home Page
layout: default
---

Hi, I'm Alex Barbosa. I have as goal to introduce helpful articles on Linux, Emacs
and Programming.

## Articles

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
