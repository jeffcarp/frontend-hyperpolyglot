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
      Ember.Component.extend({})
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
      &lt;div ng-show="shouldShow">hi</div&gt;
    </td>
    <td>
    </td>
    <td>
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
      &#123;{#if shouldShow}&#125;<br />
        &lt;div>hi</div&gt;<br />
      &#123;{/if}&#125;
    </td>
    <td>
      &lt;div dom-if="shouldShow"></div&gt;
    </td>
    <td>
      &lt;div v-if="shouldShow">hi<div/&gt;
    </td>
  </tr>

  <!-- prop validation -->

  <tr>
    <th colspan="6">
      Component lifecycle methods
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
    <td>Initialized</td>
    <td>
      componentWillMount
    </td>
    <td>
      ngOnInit
    </td>
    <td>
      init
    </td>
    <td>
      created
    </td>
    <td>
      created
    </td>
  </tr>

  <tr>
    <td>DOM Ready</td>
    <td>
      componentDidMount
    </td>
    <td>
      ngAfterContentInit
    </td>
    <td>
      didRender
    </td>
    <td>
      ready
    </td>
    <td>
      ready
    </td>
  </tr>

  <tr>
    <td>Before destroy</td>
    <td>
      componentWillUnmount?
    </td>
    <td>
      ngOnDestroy
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>

  <tr>
    <td>After destroy</td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
      destroyed
    </td>
  </tr>
</table>
