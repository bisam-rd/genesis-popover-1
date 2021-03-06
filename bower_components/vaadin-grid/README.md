![Bower version](https://badge.fury.io/bo/vaadin-grid.svg)
[![npm version](https://badge.fury.io/js/%40vaadin%2Fvaadin-grid.svg)](https://badge.fury.io/js/%40vaadin%2Fvaadin-grid)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/vaadin/vaadin-grid)
[![Build Status](https://travis-ci.org/vaadin/vaadin-grid.svg?branch=master)](https://travis-ci.org/vaadin/vaadin-grid)
[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/vaadin/web-components?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

[![Published on Vaadin  Directory](https://img.shields.io/badge/Vaadin%20Directory-published-00b4f0.svg)](https://vaadin.com/directory/component/vaadinvaadin-grid)
[![Stars on vaadin.com/directory](https://img.shields.io/vaadin-directory/star/vaadinvaadin-grid.svg)](https://vaadin.com/directory/component/vaadinvaadin-grid)

# &lt;vaadin-grid&gt;

[Live Demo ↗](https://vaadin.com/components/vaadin-grid/html-examples)
|
[API documentation ↗](https://vaadin.com/components/vaadin-grid/html-api)

[&lt;vaadin-grid&gt;](https://vaadin.com/components/vaadin-grid) is a free, high quality data grid / data table [Polymer](http://polymer-project.org) element, part of the [Vaadin components](https://vaadin.com/components).

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../iron-ajax/iron-ajax.html">
    <link rel="import" href="vaadin-grid.html">
    <link rel="import" href="vaadin-grid-selection-column.html">
    <link rel="import" href="vaadin-grid-sorter.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<dom-bind>
  <template>
    <iron-ajax auto url="https://demo.vaadin.com/demo-data/1.0/people?count=20" handle-as="json" last-response="{{users}}"></iron-ajax>

    <vaadin-grid theme="row-dividers" items="[[users.result]]" column-reordering-allowed multi-sort>

      <vaadin-grid-selection-column auto-select frozen> </vaadin-grid-selection-column>

      <vaadin-grid-column width="9em">
        <template class="header">
          <vaadin-grid-sorter path="firstName">First Name</vaadin-grid-sorter>
        </template>
        <template>[[item.firstName]]</template>
      </vaadin-grid-column>

      <vaadin-grid-column width="9em">
        <template class="header">
          <vaadin-grid-sorter path="lastName">Last Name</vaadin-grid-sorter>
        </template>
        <template>[[item.lastName]]</template>
      </vaadin-grid-column>

      <vaadin-grid-column width="15em" flex-grow="2">
        <template class="header">
          <vaadin-grid-sorter path="address.street">Address</vaadin-grid-sorter>
        </template>
        <template>[[item.address.street]], [[item.address.city]]</template>
      </vaadin-grid-column>

    </vaadin-grid>
  </template>
</dom-bind>
```

[<img src="https://raw.githubusercontent.com/vaadin/vaadin-grid/master/screenshot.png" alt="Screenshot of vaadin-grid, using the default Lumo theme">](https://vaadin.com/components/vaadin-grid)

## Getting Started

Vaadin components use the Lumo theme by default.

## The file structure for Vaadin components

- `src/vaadin-grid.html`

  Unstyled component.

- `theme/lumo/vaadin-grid.html`

  Component with Lumo theme.

- `vaadin-grid.html`

  Alias for theme/lumo/vaadin-grid.html

## Running demos and tests in browser

1. Fork the `vaadin-grid` repository and clone it locally.

1. Make sure you have [npm](https://www.npmjs.com/) installed.

1. When in the `vaadin-grid` directory, run `npm install` and then `bower install` to install dependencies.

1. Run `polymer serve --open`, browser will automatically open the component API documentation.

1. You can also open demo or in-browser tests by adding **demo** or **test** to the URL, for example:

  - http://127.0.0.1:8080/components/vaadin-grid/demo
  - http://127.0.0.1:8080/components/vaadin-grid/test


## Running tests from the command line

1. When in the `vaadin-grid` directory, run `polymer test`


## Following the coding style

We are using [ESLint](http://eslint.org/) for linting JavaScript code. You can check if your code is following our standards by running `gulp lint`, which will automatically lint all `.js` files as well as JavaScript snippets inside `.html` files.


## Creating a pull request

  - Make sure your code is compliant with our code linters: `gulp lint`
  - Check that tests are passing: `polymer test`
  - [Submit a pull request](https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github) with detailed title and description
  - Wait for response from one of Vaadin components team members


## License

Apache License 2.0

Vaadin collects development time usage statistics to improve this product. For details and to opt-out, see https://github.com/vaadin/vaadin-usage-statistics.
