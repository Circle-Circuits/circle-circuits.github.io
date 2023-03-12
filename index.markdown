---
layout: home
---

{%- assign manuals_pages = site.pages | where_exp: "item", "item.path contains 'manuals'" -%}
<section>
<h1>📚 Manuals</h1>
{%- for page in manuals_pages -%}
  <a href='{{ page.url }}'>{{ page.title }}</a>
{%- endfor -%}
</section>

{%- assign builds = site.posts | where_exp: "post", "post.categories contains 'builds'" -%}
{%- assign first_item = builds | first -%}
{%- if first_item.title -%}
  <section>
  <h1>🎸 Builds</h1>
  {%- for build in builds -%}
    <a href='{{ build.url }}'>{{ build.title }}</a>
    <br />
  {%- endfor -%}
  </section>
{%- endif -%}

{%- assign thoughts = site.posts | where_exp: "post", "post.categories contains 'thoughts'" -%}
{%- assign first_item = thoughts | first -%}
{%- if first_item.title -%}
  <section>
  <h1>💬 Thoughts</h1>
  {%- for thought in thoughts -%}
    <a href='{{ thought.url }}'>{{ thought.title }}</a>
    <br />
  {%- endfor -%}
  </section>
{%- endif -%}

{%- assign circuits_pages = site.pages | where_exp: "item", "item.path contains 'circuits'" -%}
{%- assign first_item = circuits_pages | first -%}
{%- if first_item.title -%}
  <section>
  <h1>👨🏻‍🏭 Circuits</h1>
  {%- for page in circuits_pages -%}
    <a href='{{ page.url }}'>{{ page.title }}</a>
    <br />
  {%- endfor -%}
  </section>
{%- endif -%}
