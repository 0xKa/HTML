# 🎯 CSS Specificity Cheat Sheet

CSS specificity determines which style is applied when multiple rules target the same element. The **more specific** rule wins.

---

## 🔢 Specificity Scoring System

| Selector Type                                                                         | Points |
| ------------------------------------------------------------------------------------- | ------ |
| Inline styles (`style="..."`)                                                         | 1000   |
| ID selectors (`#id`)                                                                  | 100    |
| Class selectors (`.class`), attribute selectors (`[type]`), pseudo-classes (`:hover`) | 10     |
| Element selectors (`div`, `p`), pseudo-elements (`::before`)                          | 1      |
| Universal selector (`*`), combinators (`+`, `>`, `~`)                                 | 0      |

---

## 🧮 Specificity Format

Specificity is expressed as a 4-part value:  
**Inline styles – ID selectors – Class/Attribute/Pseudo-class – Elements/Pseudo-elements**

Example: `0-1-2-3`

---

## 🧪 Examples

```css
/* Specificity: 0-0-0-1 */
p {
  color: red;
}

/* Specificity: 0-0-1-0 */
.highlight {
  color: blue;
}

/* Specificity: 0-1-0-0 */
#main {
  color: green;
}

/* Specificity: 0-1-1-2 */
div#main .highlight p {
  color: orange;
}

/* Specificity: 1-0-0-0 */
<p style="color: purple;">Text</p>
```

---

## ⚖️ Conflict Resolution

- Higher specificity wins.
- If specificity is the same, the **later rule** in the stylesheet takes effect.
- `!important` overrides everything (except another `!important` with higher specificity).

---

## 🚫 Use `!important` with caution

```css
p {
  color: red !important;
}
```

> Use `!important` only when truly necessary — it's best to rely on proper specificity.

---

## 🛠️ Useful Tools

- [Specificity Calculator](https://specificity.keegan.st/)
- Browser DevTools (Inspect styles and see what rules apply)

---

## ✅ Quick Tips

- Avoid overly complex selectors.
- Keep specificity low when possible (use class-based selectors).
- Use IDs sparingly in CSS for better maintainability.
- Use consistent naming with BEM or similar conventions for clarity.

---
