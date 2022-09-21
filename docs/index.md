---
Title: Home Page
layout: default
---

Short tips on all the great things of Linux distributions, its tools, and specially Emacs and Programming.

## Tips

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
