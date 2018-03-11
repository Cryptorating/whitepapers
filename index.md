---
extensions:
   - .pdf
   - .txt
   - .md
---

<ul>
{% for file in site.static_files %}
{% if page.extensions == null or page.extensions contains file.extname %}
{% assign dirs = file.path | split: '/' %}
{% if page.directories == null or page.directories contains dirs[1] %}
   <li><a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.path }}</a></li>
{% endif %}
{% endif %}
{% endfor %}
</ul>

This site is done with [jeklist](https://github.com/fgallaire/jeklist) by [fgallaire](https://f.gallai.re)
