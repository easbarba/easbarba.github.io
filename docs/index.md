---
Title: Home Page
layout: default
---
Hi, I'm Alex Barbosa, a Linux advocate and Programmer based in Brazil. 

I have as goal to introduce useful articles on Debian, Emacs, Guix, and miscellaneous programming topics.

## Articles

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
