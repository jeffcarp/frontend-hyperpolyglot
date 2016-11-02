---
layout: default
title: Browsers
---

# [Browser Hyperpolyglot](http://jeffcarp.github.io/frontend-hyperpolyglot/)

<table class="wiki-content-table">
  {% for category in site.data.browsers %}
    {% if category.name %}
    <tr>
      <th colspan="{{ site.data.browserlabels | size | plus: 1 }}" id="{{ category.name | slugify }}"><a href="#{{ category.name | slugify }}-note">{{ category.name }}</a></th>
    </tr>
    {% endif %}
    <tr>
      <th></th>
      {% for label in site.data.browserlabels %}
        <th>{{ label }}</th>
      {% endfor %}
    </tr>
    {% for comparison in category.comparisons %}
      <tr>
        <td id="{{ comparison.label | slugify }}"><a href="#{{ comparison.label | slugify }}-note">{{ comparison.label }}</a></td>
        {% for browser in comparison.browsers %}
          {% if browser[1].link %}
            <td><a href="{{ browser[1].link }}">{{ browser[1].linktext }}</a></td>
          {% else %}
            <td>{{ browser[1] }}</td>
          {% endif %}
        {% endfor %}
      </tr>
    {% endfor %}
  {% endfor %}
</table>

<div id="remarks">
{% for category in site.data.browsers %}
  <h1 id="{{ category.name | slugify }}-note"><a href="#{{ category.name | slugify }}">{{ category.name }}</a></h1>
  {% for comparison in category.comparisons %}
  {% if comparison.remarks %}
  <h2 id="{{ comparison.label | slugify }}-note"><a href="#{{ comparison.label | slugify }}">{{ comparison.label }}</a></h2>
  {{ comparison.remarks | markdownify }}
  {% endif %}
  {% endfor %}
{% endfor %}
</div>
