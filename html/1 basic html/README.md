# 📘 Folder 1: Basic HTML Concepts

Is folder me HTML document ke foundational structure, meta configuration, external resources ko link karne aur basic content formatting ke concepts diye gaye hain.

---

## 📄 1. `1basic.html` — Document Anatomy & Encoding

### 🎯 Main Concepts
1. **HTML ka Core Structure**:
   - `<!DOCTYPE html>`: Browser ko instruct karta hai ki page **HTML5** standard use kar raha hai.
   - `<html lang="en">`: Root container jo poore webpage ko hold karta hai. `lang="en"` accessibility aur search engines ko document ki language batata hai.
   - `<head>`: Isme webpage ka metadata aur browser settings hoti hain jo user ko directly screen par nahi dikhti (par browser aur SEO ke liye critical hain).
   - `<body>`: Visible UI area — jo bhi text, image ya elements yahan likhe jayenge wo actual webpage par display honge.

2. **Character Encoding (`UTF-8`)**:
   - `<meta charset="UTF-8">`: Computer har character (English, Hindi, symbols, emojis jaise 🚀, 🔥) ko binary numbers (0 aur 1) me encode/decode karta hai. `UTF-8` globally universal character set hai jo sabhi languages ko correctly render karta hai bina text corrupt huye.

3. **Responsive Mobile Viewport**:
   - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Mobile responsiveness ke liye sabse zaroori tag. Ye browser ko bolta hai ki webpage ki width ko device screen ki physical width ke barabar rakhe aur initial zoom level 1.0 (100%) set kare.

4. **Document Title**:
   - `<title>`: Browser tab ke upar display hone wala naam define karta hai aur bookmarks / search results me use hota hai.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My first website</title>
</head>
<body>
    Hello World
</body>
</html>
```

---

## 📄 2. `2basic.html` — SEO, Asset Linking & Tag Types

### 🎯 Main Concepts
1. **SEO Meta Description**:
   - `<meta name="description" content="...">`: Jab website Google ya search engine results page (SERP) par appear hoti hai, to title ke neeche jo 1-2 line ka summary snippet dikhta hai, wo is description se pick hota hai.

2. **Linking External CSS**:
   - `<link rel="stylesheet" href="style.css">`: External CSS file ko HTML ke sath connect karta hai.
     - `rel="stylesheet"`: Browser ko batata hai ki linked file ek styling sheet hai.
     - `href="..."`: CSS file ka relative/absolute path.

3. **Linking External JavaScript**:
   - `<script src="script.js"></script>`: External JavaScript file load karne ke liye. Usually ise `<body>` ke end me lagaya jata hai taaki pehle HTML elements render ho sakein.

4. **Basic Video Embedding**:
   - `<video src="video.mp4" controls></video>`: Video play karne ke liye tag. `controls` attribute browser ke native play/pause/volume controls provide karta hai.

5. **Paired vs. Unpaired (Void) Tags**:
   - **Paired Tags**: Inka opening aur closing tag dono hota hai aur ye content ko wrap karte hain. Jaise `<p>...</p>`, `<h1>...</h1>`, `<head>...</head>`, `<body>...</body>`.
   - **Unpaired (Void / Self-Closing) Tags**: Inme koi closing tag nahi hota aur na hi inner text content hota hai. Jaise `<meta>`, `<link>`, `<img>`, `<br>`, `<hr>`, `<input>`.

```html
<head>
    <meta name="description" content="Website summary for search engines">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <video src="video.mp4" controls></video>
    <script src="script.js"></script>
</body>
```

---

## 📄 3. `3basic.html` — Headings, Links, Paragraphs & Attributes

### 🎯 Main Concepts
1. **Headings Hierarchy (`<h1>` to `<h6>`)**:
   - `<h1>`: Document ki primary heading (Page par ideal practice me sirf 1 `<h1>` honi chahiye for SEO).
   - `<h2>` se `<h6>`: Sub-headings aur nested sub-sections create karne ke liye. Size aur semantic importance hierarchically decrease hoti hai.

2. **Anchor Tag (`<a>`) & Hyperlinking**:
   - Webpages ko link karne ke liye use hota hai.
   - `href="https://..."`: Destination URL specify karta hai.
   - `target="_blank"`: Link ko current tab ke badle **new browser tab** me open karta hai.

3. **Paragraphs & Dummy Text Generator**:
   - `<p>`: Text paragraphs define karne ke liye block-level container.
   - `lorem` shorthand (VS Code Emmet): `lorem20` likhkar tab/enter dabane se 20 words ka sample dummy text generate ho jata hai taaki layout testing ho sake.

4. **HTML Attributes & Inline Styling**:
   - **Attribute**: Tag ke opening bracket ke andar `name="value"` format me extra information/behavior add karta hai (e.g., `href`, `target`, `src`, `style`).
   - **Inline CSS (`style="..."`)**: Kisi specific HTML element par directly CSS properties apply karna. Inline style ki priority (specificity) external CSS file se zyada hoti hai.

```html
<h1>Main Title</h1>
<h2>Sub Title</h2>

<!-- External link opening in new tab -->
<a href="https://www.google.com" target="_blank">Open Google</a>

<!-- Paragraph with inline style -->
<p style="background-color: rgb(215, 187, 187);">
    Lorem ipsum dolor sit amet consectetur adipisicing elit.
</p>
```
