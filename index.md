---
layout: default
title: Front-end Hyperpolyglot
---

# frontend-hyperpolyglot

<table>
  <tr>
    <th colspan="6">
      Components
    </th>
  </tr>
  <tr>
    <th></th>
    <th>React</th>
    <th>Angular</th>
    <th>Ember</th>
    <th>Polymer</th>
    <th>Vue</th>
  </tr>

  <tr>
    <td>Define component</td>
    <td>
      // ES5<br />
      var Component = React.createClass({})<br />
      // ES6<br />
      class Component extends React.Component
    </td>
    <td>
      module.component('component-name', {})
    </td>
    <td>
      `<script type="text/x-handlebars" id="components/blog-post">`
        `<h1>Blog Post</h1>`
        `<p>Lorem ipsum dolor sit amet.</p>`
      `</script>`
    </td>
    <td>
      Polymer({})
    </td>
    <td>
      var Component = Vue.extend({})
    </td>
  </tr>

  <tr>
    <th colspan="6">
      Component communication
    </th>
  </tr>
  <tr>
    <th></th>
    <th>React</th>
    <th>Angular</th>
    <th>Ember</th>
    <th>Polymer</th>
    <th>Vue</th>
  </tr>

  <tr>
    <td>One-way data binding</td>
    <td>
      &lt;Child foo={bar} /&gt;
    </td>
    <td>
    </td>
    <td>
      &#123;{child foo=bar}&#125;
    </td>
    <td>
      &lt;Child foo='{"serialized": "object"}' /&gt;
    </td>
    <td>
      &lt;Child :foo="bar" /&gt;
    </td>
  </tr>

  <tr>
    <th colspan="6">
      Template logic
    </th>
  </tr>
  <tr>
    <th></th>
    <th>React</th>
    <th>Angular</th>
    <th>Ember</th>
    <th>Polymer</th>
    <th>Vue</th>
  </tr>

  <tr>
    <td>CSS show/hide</td>
    <td>
      &lt;div style=&#123;{display: shouldShow}&#125;>hi</div&gt;
    </td>
    <td>
      &lt;div ng-show="shouldShow" /&gt;
    </td>
    <td>
      &#123;{child foo=bar}&#125;
    </td>
    <td>
      &lt;Child foo='{"serialized": "object"}' /&gt;
    </td>
    <td>
      &lt;div v-show="shouldShow">hi<div/&gt;
    </td>
  </tr>

  <tr>
    <td>DOM add/remove</td>
    <td>
      shouldShow ? &lt;div>hi</div&gt; : null
    </td>
    <td>
      &lt;div ng-if="shouldShow" /&gt;
    </td>
    <td>
      &#123;{#if shouldShow}&#125;
        <div>hi</div>
      &#123;{/if}&#125;
    </td>
    <td>
      &lt;div dom-if="shouldShow"></div&gt;
    </td>
    <td>
      &lt;div v-if="shouldShow">hi<div/&gt;
    </td>
  </tr>

</table>
