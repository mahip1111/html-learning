# 📄 about_link_tag — The `<link>` Tag Mechanics

Is document me HTML `<head>` section me use hone wale `<link>` tag ke deep technical mechanics, attributes (`rel`, `href`) aur stylesheets connection ke concepts explain kiye gaye hain.

---

## 🎯 1. Syntax & Core Meaning

```html
<link rel="stylesheet" href="style.css">
```

### 🔍 Breakdown:
1. `<link>`: External resources ko current HTML document ke sath link karne ke liye void/self-closing tag.
2. `rel="stylesheet"` (Relationship): Browser ko clarify karta hai: *"Yeh target file ek CSS stylesheet hai jisme design and formatting rules defined hain."*
3. `href="style.css"` (Hypertext Reference): CSS file ka local relative path ya remote web URL.

---

## 🔑 2. Summary
- **Primary Function**: HTML structure + CSS presentation ko attach karne wali main pipeline.
- **Common Relations**:
  - `rel="stylesheet"` $\rightarrow$ CSS styling
  - `rel="icon"` $\rightarrow$ Favicon tab icon
  - `rel="preconnect"` $\rightarrow$ Performance font/DNS optimization
