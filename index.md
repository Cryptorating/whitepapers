---
---

<div>
{% if site.style == 'list' %}
    <ul>
{% elsif site.style == 'nlist' %}
    <ol>
{% endif %}
{% assign directory = '' %}
{% assign baseurl = site.github.baseurl %}
{% for file in site.static_files %}
    {% if site.extensions == null or site.extensions contains file.extname %}
        {% assign dirs = file.path | split: '/' %}
        {% if dirs[1] != directory and  site.style == 'dir' %}
            {% if directory != '' %}
                </dl>
            {% endif %}
            {% assign directory = dirs[1] %}
            <dl>
            {% if site.spacification == null %}
                <dt><a href="{{ baseurl }}/{{ directory }}">{{ directory }}</a></dt>
            {% else %}
                <dt><a href="{{ baseurl }}/{{ directory }}">{{ directory | replace: site.spacification, ' ' }}</a></dt>
            {% endif %}
        {% endif %}
        {% if site.directories == null or site.directories contains dirs[1] %}
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

This site is done with [jeklist](https://github.com/fgallaire/jeklist) by [fgallaire](https://f.gallai.re)
