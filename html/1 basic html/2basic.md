# 📄 2basic — SEO Meta, Resource Linking & Tag Classifications

Is document me SEO Meta Description, External CSS & JavaScript file linking, Video embedding basics aur Paired vs Unpaired (Void) tags ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="This is my first website">
    <title>basic.html</title>
    <link rel="stylesheet" href="style.css">
</head>
<body> 
    <h1>My first website</h1>
    Hello World how are you.

    <video src="video.mp4" controls></video>

    <script src="script.js"></script> 
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. SEO Meta Description (`<meta name="description">`)
- **Meaning**: Jab user Google par search karta hai to search engine results page (SERP) par webpage ke title ke neeche jo 1-2 line ka summary snippet dikhta hai, wo description se fetch hota hai.
- **Syntax**: `<meta name="description" content="Brief summary of your webpage">`
- **Emmet Shortcut**: VS Code me `meta:desc` type karke Tab/Enter dabane se ye tag generate ho jata hai.

### 2. External CSS Linking (`<link>`)
- **Function**: HTML structure ko alag se banayi gayi CSS styling file (`style.css`) ke sath connect karta hai.
- **Attributes**:
  - `rel="stylesheet"`: Browser ko clarify karta hai ki linked file ek styling rulesheet hai.
  - `href="style.css"`: CSS file ka relative / absolute path.

### 3. External JavaScript Linking (`<script>`)
- **Function**: JavaScript code (`script.js`) ko load karke webpage ko interactive banata hai (e.g. alert popup, dynamic changes).
- **Placement**: Best practice hoti hai ise `<body>` ke end me (closing `</body>` se theek pehle) lagana taaki pehle HTML structure load ho jaye.
- **Emmet Shortcut**: `script:src`

### 4. Basic Video Embedding (`<video>`)
- **Syntax**: `<video src="video.mp4" controls></video>`
- **`controls` Attribute**: Agar `controls` na lagaya jaye to user ko play, pause, seekbar aur volume ka control nahi milega.

---

## 🏷️ 3. Paired vs. Unpaired (Void) Tags

HTML me tags do main categories me divide hote hain:

| Category | Definition | Examples |
| :--- | :--- | :--- |
| **Paired Tags (Container Tags)** | Inka opening tag `<tag>` aur closing tag `</tag>` dono hota hai. Ye apne andar content/text ko hold karte hain. | `<head></head>`, `<body></body>`, `<h1></h1>`, `<p></p>`, `<script></script>` |
| **Unpaired / Void Tags (Self-Closing)** | Inka koi closing tag nahi hota aur na hi ye text wrap karte hain. Ye attributes ke through behave karte hain. | `<meta>`, `<link>`, `<img>`, `<input>`, `<br>`, `<hr>` |
