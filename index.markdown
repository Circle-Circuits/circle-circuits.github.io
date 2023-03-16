---
layout: home
---

<ul>
{%- for page in site.pages -%}
  {%- if page.title -%}
    <li><a href='{{ page.url }}'>{{ page.title }}</a></li>
  {%- endif -%}
{%- endfor -%}
{%- for post in site.posts -%}
  <li><a href='{{ post.url }}'>{{ post.title }}</a></li>
{%- endfor -%}
</ul>
