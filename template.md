---
---

{% if site.style == 'dir' %}
{% assign index = page.url.size | minus: 2 %}
{% assign directory = page.url | slice: 1, index %}

<div>
<dl>
{% if site.spacification == null %}
    <dt>{{ directory }}</dt>
{% else %}
    <dt>{{ directory | replace: site.spacification, ' ' }}</dt>
{% endif %}
{% for file in site.static_files %}
    {% if site.extensions == null or site.extensions contains file.extname %}
        {% assign dirs = file.path | split: '/' %}
        {% if dirs[1] == directory %}
            <dd>
            {% if site.html_link contains file.extname %}
                {% assign index = file.path.size | minus: file.extname.size %}
                {% assign fpath = file.path | slice: 0, index %}
                {% assign fname = file.basename %}
                {% if site.truncate == null %}
                    <a href="{{ site.github.baseurl }}{{ fpath }}">{{ fname }}</a> (<a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.extname }}</a>)
                {% else %}
                    <a href="{{ site.github.baseurl }}{{ fpath }}">{{ fname | truncate: site.truncate }}</a> (<a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.extname }}</a>)
                {% endif %}
            {% else %}
                {% assign fname = file.name %}
                {% if site.truncate == null %}
                    <a href="{{ site.github.baseurl }}{{ file.path }}">{{ fname }}</a>
                {% else %}
                    <a href="{{ site.github.baseurl }}{{ file.path }}">{{ fname | truncate: site.truncate }}</a>
                {% endif %}
            {% endif %}
            </dd>
        {% endif %}
    {% endif %}
{% endfor %}
</dl>
</div>
{% endif %}
