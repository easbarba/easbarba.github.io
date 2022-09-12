---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
Title: Home Page
layout: default
---
- [Algorithmic Publishing Systems](#algorithmic-publishing-systems)
- [Posts](#posts)
- [Pages](#pages)
- [About Me](#about-me)
  - [My Companies](#my-companies)
  - [My Resumes](#my-resumes)
  - [My Coordinates](#my-coordinates)

Hi, i'm Alex Barbosa.

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
