---
extensions:
   - .pdf
---
<ul>
{% for file in site.static_files %}
{% if page.extensions contains file.extname %}
   <li><a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.path }}</a></li>
{% endif %}
{% endfor %}
</ul>
