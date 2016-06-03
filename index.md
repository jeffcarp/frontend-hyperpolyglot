---
layout: default
title: Front-end Hyperpolyglot
---

# [Front-end Hyperpolyglot](http://jeffcarp.github.io/frontend-hyperpolyglot/)

_Inspired by [hyperpolyglot.org](http://hyperpolyglot.org/), a comparison of similar features in popular JavaScript frameworks._

<p>Any contributors who are more familiar with these frameworks would be massively appreciated. The source is on <a href="https://github.com/jeffcarp/frontend-hyperpolyglot">GitHub</a>.</p>

<table class="wiki-content-table">
  {% for category in site.data.frameworks %}
    {% if category.name %}
    <tr>
      <th colspan="8" id="{{ category.name | slugify }}"><a href="#{{ category.name | slugify }}-note">{{ category.name }}</a></th>
    </tr>
    {% endif %}
    <tr>
      <th></th>
      <th>React</th>
      <th>Angular 2</th>
      <th>Angular 1</th>
      <th>Polymer</th>
      <th>Vue</th>
      <th>Ember</th>
      <th>Riot</th>
    </tr>
    {% for comparison in category.comparisons %}
      <tr>
        <td id="{{ comparison.label | slugify }}"><a href="#{{ comparison.label | slugify }}-note">{{ comparison.label }}</a></td>
        {% for framework in comparison.frameworks %}
          {% if framework[1].js %}
            <td>{% highlight js %}{{ framework[1].js }}{% endhighlight %}</td>
          {% elsif framework[1].comment %}
            <td class="faded">{{ framework[1].comment }}</td>
          {% else %}
            <td>{% highlight html %}{{ framework[1] }}{% endhighlight %}</td>
          {% endif %}
        {% endfor %}
      </tr>
    {% endfor %}
  {% endfor %}
</table>

<div id="remarks">

{% for category in site.data.frameworks %}
  <h1 id="{{ category.name | slugify }}-note"><a href="#{{ category.name | slugify }}">{{ category.name }}</a></h1>
  {% for comparison in category.comparisons %}
  {% if comparison.remarks %}
  <h2 id="{{ comparison.label | slugify }}-note"><a href="#{{ comparison.label | slugify }}">{{ comparison.label }}</a></h2>
  {{ comparison.remarks | markdownify }}
  {% endif %}
  {% endfor %}
{% endfor %}
</div>
