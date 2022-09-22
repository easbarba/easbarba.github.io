---
Title: Home Page
layout: default
---

Miscellaneous tips on all of the awesome things of Linux and related techies.

## Tips

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
