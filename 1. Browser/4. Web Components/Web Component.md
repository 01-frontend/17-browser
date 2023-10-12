# Web Component

Web components are `a set of web platform APIs` that allow you to `create new custom, reusable, encapsulated HTML tags` to use in web pages and web apps

Web components are based on four main specifications

## 1. Custom Elements

The Custom Elements `lays the foundation` for `designing and using new types` of DOM elements

```
  class AppDrawer extends HTMLElement {...}
  window.customElements.define('app-drawer', AppDrawer);
```

To use the new tag

```
  <app-drawer></app-drawer>
```

Custom Elements lifecycle methods, includes

- `constructor()`: Called when an `instance of the element is created or upgraded`
- `connectedCallback()`: Called every time when the `element is inserted into the DOM`
- `disconnectedCallback()`: Called every time the `element is removed from the DOM`
- `attributeChangedCallback(attrName, oldValue, newValue)`: Called when `an attribute is added, removed, updated or replaced`

## 2. Shadow DOM

The shadow DOM `defines how to use encapsulated style and markup` in web components

- Used for `self-contained components`
- `Encapsulate` styles and markup
- Create with `element.attachShadow({ mode: open/closed })`
- Create a `shadowRoot` that we can reference and interact with

```
  const header = document.createElement('header');
  const shadowRoot = header.attachShadow({mode: 'open'});

  shadowRoot.innerHTML = '<h1>Hello Shadow DOM</h1>'; // Could also use appendChild().
  // header.shadowRoot === shadowRoot
  // shadowRoot.host === header
```

## 3. ES Modules

The ES Modules `defines the inclusion and reuse of JS documents` in a standards based, modular, performant way

## 4. HTML Template

- Defined the `encapsulated markup` of out web component
- Template tag stores markup on page
- `Include both HTML and CSS` in templates
- Use slots to add custom text

## # Reference

https://www.webcomponents.org/introduction
https://www.youtube.com/watch?v=PCWaFLy3VUo&ab_channel=TraversyMedia
