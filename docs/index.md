---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
Title: Home Page
layout: default
---
Hi, I'm Alex Barbosa, a backend developer from Brazil. 

Here I share with you tips, how-tos and, I reckon, even complaining of what I grow fond of GNU/Linux cool stuff, specially Emacs, Guix, Debian and
Programming. 

I hope you find something useful and who knows, get a like of them too. :)

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
