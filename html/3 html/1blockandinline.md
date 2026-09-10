# 📄 1blockandinline — Block vs Inline Elements & Display Behavior

Is document me Block-level elements, Inline elements, generic containers (`<div>`, `<span>`) aur CSS display control ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inline and Block Elements</title>
</head>
<body>
    <!-- Block element -->
    <p>Hey I am a para and i am block element therefore my background color takes full width</p>

    <!-- Inline elements (side by side) -->
    <a href="https://google.com" target="_blank">Google</a>

    <!-- Block container -->
    <div>I am a block element container</div>

    <!-- Inline container -->
    <span>I am span and I am inline element</span>

    <a href="https://bing.com" target="_blank">Bing</a>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Block-Level Elements
- **Characteristics**:
  - Hamesha nayi line (new line) se start hote hain.
  - Webpage / parent container ki **poori horizontal width (100%)** occupy karte hain.
  - Background color lagane par poori screen width tak failta hai.
- **Common Tags**: `<p>`, `<div>`, `<h1>` to `<h6>`, `<ul>`, `<ol>`, `<li>`, `<form>`, `<section>`, `<article>`, `<header>`, `<footer>`.
- **`<div>` Container**: Generic block container jo layout structuring, grouping aur CSS styling ke liye use hota hai.

### 2. Inline Elements
- **Characteristics**:
  - Nayi line create nahi karte; doosre inline elements ke bagal me (same horizontal line par) fit ho jate hain.
  - Sirf apne inner content / text jitni hi width occupy karte hain.
- **Common Tags**: `<a>`, `<span>`, `<img>`, `<strong>`, `<em>`, `<label>`, `<input>`, `<button>`, `<svg>`.
- **`<span>` Container**: Generic inline container jo sentence ke kisi specific word ya phrase ko wrap karke style karne ke liye use hota hai bina layout ko tode.

### 3. CSS Display Switching
- HTML elements ka block ya inline hona permanent nahi hota. CSS ki `display` property se ise change kiya ja sakta hai:
  - `display: block;`
  - `display: inline;`
  - `display: inline-block;` (Inline ki tarah bagal me baithta hai, par width/height customize karne deta hai)
  - `display: none;` (DOM me rehte huye screen se gayab kar deta hai)
