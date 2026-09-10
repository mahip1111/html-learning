# 📄 3basic — Headings, Hyperlinks, Paragraphs & Styling Specificity

Is document me Headings hierarchy, Anchor tags (`<a>`), Dummy text generator (`lorem`), HTML Attributes concept aur Inline CSS vs External CSS Specificity ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Bookmarks</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>My Bookmarks</h1>
    <a target="_blank" href="https://www.google.com">Open Google</a>

    <h2>Subheading Level 2</h2>
    <h3>Subheading Level 3</h3>
    <h4>Subheading Level 4</h4>
    <h5>Subheading Level 5</h5>
    <h6>Subheading Level 6</h6>

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatibus.</p>

    <p style="background-color: rgb(215, 187, 187);">Styled Paragraph</p>

    <script src="script.js"></script>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Headings Hierarchy (`<h1>` to `<h6>`)
- HTML me total **6 levels** of headings hoti hain: `<h1>` (largest & most important) se lekar `<h6>` (smallest & least important).
- **SEO Best Practice**: Har page par ideal taur par sirf **ek** `<h1>` tag hona chahiye jo poore page ke primary topic ko represent kare. Baki sections ke liye `<h2>` se `<h6>` ka hierarchy sequence follow kiya jata hai.

### 2. Anchor Tag (`<a>`) & Hyperlinking
- **Function**: User ko kisi doosre webpage ya external URL par navigate karwane ke liye use hota hai.
- **Attributes**:
  - `href="https://..."`: Destination website / webpage ka address.
  - `target="_blank"`: Link par click karne par page ko **naye browser tab** me open karta hai (bina current page ko band kiye).

### 3. Paragraphs (`<p>`) & Dummy Text Generator (`lorem`)
- `<p>`: Paragraphs create karne ke liye block-level tag.
- **Emmet Lorem Generator**:
  - `lorem20` likhkar tab dabane se 20 dummy Latin words generate ho jate hain.
  - **Purpose**: Real content aane se pehle website ke UI/layout aur font readability ko test karne ke liye placeholder text ke roop me use hota hai.

### 4. HTML Attributes Concept
- Attributes tags ke opening tag me `name="value"` format me likhe jate hain.
- Ye tag ki functionality aur behavior ko enhance karte hain (e.g. `href`, `target`, `src`, `style`, `class`, `id`).

### 5. Inline Style (`style="..."`) vs External CSS Specificity
- **Inline Style**: Element tag ke andar direct CSS likhna, jaise `<p style="background-color: rgb(215, 187, 187);">`.
- **CSS Specificity Rule**: Inline style ki priority (specificity) external `style.css` file se zyada hoti hai. Agar external CSS me `<p>` ka background blue hai aur inline me red hai, to **inline style (red)** hi render hoga.
