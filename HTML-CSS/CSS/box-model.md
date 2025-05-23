# 📦 CSS Box Model Cheat Sheet: Margin, Border & Padding

The **CSS box model** describes how elements are displayed and spaced on the page. It consists of:

![box-model|640x480](./imgs/box-model.gif)

---

## 🟨 Margin

**Margin** is the space **outside** the border of the element.

```css
/* All sides */
margin: 20px;

/* Top, Right, Bottom, Left */
margin: 10px 15px 20px 25px;

/* Shorthand */
margin-top: 10px;
margin-right: 15px;
margin-bottom: 20px;
margin-left: 25px;
```

💡 Use `auto` to horizontally center block elements:

```css
margin: 0 auto;
```

---

## 🟩 Padding

**Padding** is the space **inside** the element, between content and border.

```css
/* All sides */
padding: 10px;

/* Top, Right, Bottom, Left */
padding: 5px 10px 15px 20px;

/* Individual sides */
padding-top: 5px;
padding-right: 10px;
padding-bottom: 15px;
padding-left: 20px;
```

🔄 Content will shrink or grow depending on padding **unless `box-sizing: border-box;` is used**.

---

## 🟥 Border

**Border** is the line between padding and margin. You can set width, style, and color.

```css
/* Full border */
border: 2px solid black;

/* Individual sides */
border-top: 4px dashed red;
border-right: 2px dotted blue;
border-bottom: 1px solid gray;
border-left: 5px double green;
```

### 🌀 Border Radius

Used to create rounded corners.

```css
border-radius: 10px; /* All corners */
border-radius: 10px 0; /* Top-left and bottom-right */
border-radius: 50%; /* Circle if element is square */
```

---

## 🧠 Extra Tips

- Use `outline` instead of `border` if you don’t want the element's size to change.
- Combine `margin` and `padding` for spacing and layout control.
- Set `box-sizing: border-box;` to include padding and border in the total width/height.

```css
* {
  box-sizing: border-box;
}
```

---

## 🧪 Quick Practice Example

```css
.box {
  margin: 20px;
  padding: 15px;
  border: 2px solid #333;
  border-radius: 8px;
}
```

---

✅ Mastering margin, border, and padding is essential for layout and spacing in CSS.
