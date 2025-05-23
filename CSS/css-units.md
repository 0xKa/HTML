# 📐 CSS Units Cheat Sheet

This file covers the most common CSS units: `px`, `%`, `em`, `rem`, `vw`, `vh`, and more.

---

## 🔹 Absolute Units

These are fixed-size units. They don’t scale based on screen or user settings.

| Unit             | Meaning                          | Example            | Notes                      |
| ---------------- | -------------------------------- | ------------------ | -------------------------- |
| `px`             | Pixels                           | `margin: 10px;`    | Most common, not scalable  |
| `pt`             | Points                           | `font-size: 12pt;` | Used in print, not on web  |
| `cm`, `mm`, `in` | Centimeters, Millimeters, Inches | `width: 2cm;`      | Rarely used in web layouts |

✅ Use `px` when you need precise control and no scaling (not recommended for fonts on responsive designs).

---

## 🔸 Relative Units

These scale based on other values (like parent or root element).

### `%` — Percentage

- Relative to **parent element’s size**.

```css
width: 50%; /* 50% of parent’s width */
```

### `em` — Relative to **parent element’s font-size**

```css
font-size: 1.5em; /* 1.5 × parent font-size */
margin: 2em; /* 2 × current font-size */
```

🔁 **Nested `em` values can compound!**

### `rem` — Relative to **root (`html`) font-size**

```css
font-size: 2rem; /* 2 × root font-size */
```

✅ Better for consistent, scalable layouts than `em`.

---

## 🌐 Viewport Units

Relative to the size of the browser’s **viewport**.

| Unit   | Description               | Example             |
| ------ | ------------------------- | ------------------- |
| `vw`   | 1% of viewport **width**  | `width: 50vw;`      |
| `vh`   | 1% of viewport **height** | `height: 100vh;`    |
| `vmin` | 1% of smaller dimension   | `font-size: 3vmin;` |
| `vmax` | 1% of larger dimension    | `padding: 2vmax;`   |

📱 Great for **responsive designs**, especially full-screen layouts.

---

## ⚖️ Comparison Table

| Unit  | Relative To      | Responsive? | Notes                       |
| ----- | ---------------- | ----------- | --------------------------- |
| `px`  | Screen pixels    | ❌          | Fixed size, no scaling      |
| `%`   | Parent element   | ✅          | Common in fluid layouts     |
| `em`  | Parent font-size | ✅          | Inherited and compounding   |
| `rem` | Root font-size   | ✅          | Stable across elements      |
| `vw`  | Viewport width   | ✅          | 1vw = 1% of viewport width  |
| `vh`  | Viewport height  | ✅          | 1vh = 1% of viewport height |

---

## 💡 Best Practices

- ✅ Use `rem` for base spacing and typography
- ✅ Use `%` or `vw/vh` for layout and responsiveness
- ⚠️ Avoid using too many `em` units deep in nested elements unless intentional
- ✅ Combine units smartly: `max-width: 90vw;`, `padding: 2rem;`

---

## 🧪 Example

```css
html {
  font-size: 16px; /* 1rem = 16px */
}

.container {
  width: 80%;
  padding: 2rem;
}

.title {
  font-size: 2em; /* 2 × parent’s font-size */
}

.button {
  font-size: 1rem;
  padding: 0.5em 1em;
}
```

---

✅ Mastering units helps create clean, responsive, and accessible designs.
