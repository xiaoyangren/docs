---
layout: base
title:  'Universal features'
generated: 'true'
permalink: u/feat/all.html
---

# Universal features

{% include u-feat-table.html %}

----------

{% for p in site.u-feat %}
{% if p.content contains "<!--details-->" %}    
{{ p.content | split:"<!--details-->" | first }}
<a href="{{ p.url | remove_first:'/' }}">See details</a>
{% else %}
{{ p.content }}
{% endif %}
<a href="{{ site.git_edit }}/_u-feat/{{ p.title }}.md" target="#">edit {{ p.title }}</a>

----------

{% endfor %}