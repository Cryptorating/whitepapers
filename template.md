---
---

{% assign index = page.url.size | minus: 2 %}
{% assign directory = page.url | slice: 1, index | remove_first: "symbol/" %}
{% assign baseurl = site.github.baseurl %}

<div>
{% if site.style == 'list' %}
    <ul>
{% elsif site.style == 'nlist' %}
    <ol>
{% elsif site.style == 'dir' %}
    <dl>
    {% if site.spacification == null %}
        <dt>{{ directory }}</dt>
    {% else %}
        <dt>{{ directory | replace: site.spacification, ' ' }}</dt>
    {% endif %}
{% endif %}
{% for file in site.static_files %}
    {% if site.extensions == null or site.extensions contains file.extname %}
        {% assign dirs = file.path | split: '/' %}
        {% if dirs[1] == directory or dirs[2] == directory %}
            {% if site.style contains 'list' %}
                <li>
            {% elsif site.style == 'dir' %}
                <dd>
            {% endif %}
            {% if site.html_link contains file.extname %}
                {% assign index = file.path.size | minus: file.extname.size %}
                {% assign fpath = file.path | slice: 0, index %}
                {% if site.style == 'dir' %}
                    {% assign fname = file.basename %}
                {% else %}
                    {% assign fname = fpath | slice: 1, fpath.size %}
                {% endif %}
                {% if site.truncate == null %}
                    <a href="{{ baseurl }}{{ fpath }}">{{ fname }}</a> (<a href="{{ baseurl }}{{ file.path }}">{{ file.extname }}</a>)
                {% else %}
                    <a href="{{ baseurl }}{{ fpath }}">{{ fname | truncate: site.truncate }}</a> (<a href="{{ baseurl }}{{ file.path }}">{{ file.extname }}</a>)
                {% endif %}
            {% else %}
                {% if site.style == 'dir' %}
                    {% assign fname = file.name %}
                {% else %}
                    {% assign fname = file.path | slice: 1, file.path.size %}
                {% endif %}
                {% if site.truncate == null %}
                    <a href="{{ baseurl }}{{ file.path }}">{{ fname }}</a>
                {% else %}
                    <a href="{{ baseurl }}{{ file.path }}">{{ fname | truncate: site.truncate }}</a>
                {% endif %}
            {% endif %}
            {% if site.style contains 'list' %}
                </li>
            {% elsif site.style == 'dir' %}
                </dd>
            {% elsif site.style == null %}
                <br>
            {% endif %}
        {% endif %}
    {% endif %}
{% endfor %}
{% if site.style == 'list' %}
    </ul>
{% elsif site.style == 'nlist' %}
    </ol>
{% elsif site.style == 'dir' %}
    </dl>
{% endif %}
</div>

This site is done with [jeklist](https://github.com/fgallaire/jeklist)
