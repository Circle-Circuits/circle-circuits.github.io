---
layout: home
---

<div style="text-align: center; margin-top:20%;">
        <img src="assets/img/logo.png" width="80%" />
</div>
<br />
<p>{{ site.description }}</p>

{% for manual in site.manuals %}
<p>
    <a href="{{ manual.asset }}.pdf">
      {{ manual.title }}
    </a>
</p>
{% endfor %}

{%- include social.html -%}