---
layout: default
title: Front-end Hyperpolyglot
---

# frontend-hyperpolyglot

<table>
  {% for category in site.data.frameworks %}
    <tr>
      <th colspan="6">{{ category.name }}</th>
    </tr>
    <tr>
      <th></th>
      <th>React</th>
      <th>Angular</th>
      <th>Ember</th>
      <th>Polymer</th>
      <th>Vue</th>
    </tr>
    {% for comparison in category.comparisons %}
      <tr>
        <td>{{ comparison.label }}</td>
        {% for framework in comparison.frameworks %}
          <td>
            {{ framework[1] |  escape }}
          </td>
        {% endfor %}
      </tr>
    {% endfor %}
  {% endfor %}
</table>
