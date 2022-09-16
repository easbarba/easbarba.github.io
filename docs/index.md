---
Title: Home Page
layout: default
---
Hi, I'm Alex Barbosa, a Java Developer & Linux power-user based on Brazil . 

Here I share tips, how-toes and I reckon even complaining articles of what I grow
fond of GNU/Linux cool stuff, specially Emacs, GUI, Debian and general
programming topics.

I hope you find them useful, and who knows get a like of them too. :)

## Writings

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
