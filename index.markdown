---
layout: home
---

<div style="text-align: center; margin-top:20%;">
        <img src="assets/img/logo.png" width="80%" />
</div>
<br />
<p>{{ site.description }}</p>

<p>Find me on <a href="https://instagram.com/{{ site.instagram_username| cgi_escape | escape }}">Instragram</a>.</p>

<br /><br />
<h3>Manuals 📚</h3>
{%- assign manuals_pages = site.pages | where_exp: "item", "item.path contains 'manuals'" -%}
{%- for page in manuals_pages -%}
  <a href='{{ page.url }}'>{{ page.title }}</a>
{%- endfor -%}
