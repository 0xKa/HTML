# 🎨 CSS Selectors Cheat Sheet

## 🟦 Basic Selectors

- `*` — Universal selector (selects all elements)

  ```css
  * {
    margin: 0;
  }
  ```

- `element` — Type selector (selects all elements of that type)

  ```css
  p {
    color: black;
  }
  ```

- `.class` — Class selector

  ```css
  .btn {
    background-color: blue;
  }
  ```

- `#id` — ID selector (must be unique)

  ```css
  #main {
    padding: 10px;
  }
  ```

- `element, element` — Group selector
  ```css
  h1,
  h2,
  h3 {
    font-family: Arial;
  }
  ```

## 🟨 Combinators

- `ancestor descendant` — Descendant selector

  ```css
  div p {
    color: gray;
  }
  ```

- `parent > child` — Direct child selector

  ```css
  ul > li {
    list-style-type: square;
  }
  ```

- `element1 + element2` — Adjacent sibling selector

  ```css
  h1 + p {
    color: blue;
  }
  ```

- `element1 ~ element2` — General sibling selector
  ```css
  h1 ~ p {
    font-style: italic;
  }
  ```

## 🟥 Attribute Selectors

- `[attr]` — Select elements with a given attribute

  ```css
  input[required] {
    border: 2px solid red;
  }
  ```

- `[attr="value"]` — Exact match

  ```css
  input[type="text"] {
    width: 200px;
  }
  ```

- `[attr^="value"]` — Attribute starts with value

  ```css
  a[href^="https"] {
    color: green;
  }
  ```

- `[attr$="value"]` — Attribute ends with value

  ```css
  img[src$=".jpg"] {
    border: 1px solid black;
  }
  ```

- `[attr*="value"]` — Attribute contains value
  ```css
  div[class*="card"] {
    box-shadow: 0 0 5px #aaa;
  }
  ```

## 🟩 Pseudo-classes

- `:hover` — When hovered
- `:focus` — When focused
- `:active` — When active (clicked)

  ```css
  button:hover {
    background-color: lightblue;
  }
  ```

- `:first-child`, `:last-child`, `:nth-child(n)`

  ```css
  ul li:first-child {
    font-weight: bold;
  }
  ```

- `:not(selector)` — Exclude certain elements
  ```css
  p:not(.highlight) {
    color: gray;
  }
  ```

## 🟪 Pseudo-elements

- `::before` / `::after` — Add content before/after

  ```css
  p::after {
    content: " ✔";
    color: green;
  }
  ```

- `::first-letter`, `::first-line`
  ```css
  p::first-letter {
    font-size: 2em;
    color: red;
  }
  ```

---
