---
Title: Home Page
layout: default
---
Hi, I'm Alex Barbosa, a Java Developer & Linux power-user based in Brazil. 

Here I share articles on all of what I have grow fond in the GNU/Linux land,
specially Emacs, Guix, Debian and general programming topics.

I hope you find them useful, and who knows, get a like of them too. :)

## Writings

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
