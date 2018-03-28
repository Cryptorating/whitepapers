<ul>
{% for file in site.static_files %}
    {% if page.extensions == null or page.extensions contains file.extname %}
        {% assign dirs = file.path | split: '/' %}
        {% if page.directories == null or page.directories contains dirs[1] %}
            {% if page.html_link contains file.extname %}
                {% assign index = file.path.size | minus: file.extname.size %}
                {% assign fpath = file.path | slice: 0, index %}
                {% if page.truncate == null %}
                    <li><a href="{{ site.github.baseurl }}{{ fpath }}">{{ fpath | slice: 1, fpath.size }}</a> (<a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.extname }}</a>)</li>
                {% else %}
                    <li><a href="{{ site.github.baseurl }}{{ fpath }}">{{ fpath | slice: 1, fpath.size | truncate: page.truncate }}</a> (<a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.extname }}</a>)</li>
                {% endif %}
            {% else %}
                {% if page.truncate == null %}
                    <li><a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.path | slice: 1, file.path.size }}</a></li>
                {% else %}
                    <li><a href="{{ site.github.baseurl }}{{ file.path }}">{{ file.path | slice: 1, file.path.size | truncate: page.truncate }}</a></li>
                {% endif %}
            {% endif %}
        {% endif %}
    {% endif %}
{% endfor %}
</ul>

This site is done with [jeklist](https://github.com/fgallaire/jeklist) by [fgallaire](https://f.gallai.re)
