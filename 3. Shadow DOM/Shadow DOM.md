# Shadow DOM

Shadow DOM `serves for encapsulation`. It allows `a component to have its very own “shadow” DOM tree`, that `can’t be accidentally accessed` from the main document, may have `local style rules`, and more

## Built-in shadow DOM

The <input type="range"> input[type="range"] is one of example. The browser uses DOM/CSS internally to draw them

<br>
<img src="./Assets/shadow-dom-range.png" width="500" style="display: block; margin: 0 auto" />
<br>

## Shadow tree

A DOM element can have two types of DOM subtrees

- `Light tree` – `a regular DOM subtree`, made of HTML children. All subtrees that we’ve seen in previous chapters were “light”
- `Shadow tree` – `a hidden DOM subtree`, not reflected in HTML, hidden from prying eyes

## Encapsulation

Shadow DOM is strongly delimited from the main document

- Shadow DOM elements `are not visible to querySelector` from the light DOM. In particular, Shadow DOM elements may have ids that conflict with those in the light DOM. They must be unique only within the shadow tree

- Shadow DOM `has own stylesheets`. `Style rules` from the outer DOM `don’t get applied`
