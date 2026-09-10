# 📘 Folder: HTML Project 2 — Multi-Page Website Architecture

Is folder me pure HTML se ek complete **Multi-Page Website** banayi gayi hai jisme interconnected navigation bar aur distinct pages hain.

---

## 🎯 Architecture & Structure

Website 4 dedicated pages se milkar bani hai:
1. `1.index.html` $\rightarrow$ **Home Page** (Welcome hero section, project highlights).
2. `2.about.html` $\rightarrow$ **About Me** (Bio, carrier goals with ordered list `<ol>`).
3. `3.contact.html` $\rightarrow$ **Contact Page** (Contact query form with `<input>` & `<textarea>`).
4. `4.services.html` $\rightarrow$ **Services Page** (Pricing/offering breakdown using `<table>`).

---

## 🔑 Core Concepts & Techniques

1. **Relative Hyperlink Navigation**:
   - Har page ke top par ek consistent navigation bar banaya gaya hai jo relative filenames ke zariye seamlessly ek page se doosre page par switch karta hai:
```html
<a href="1.index.html">Home</a> 
<a href="2.about.html">About</a> 
<a href="3.contact.html">Contact</a> 
<a href="4.services.html">Services</a>
```

2. **Page-Specific Titles for SEO & UX**:
   - Har file ke `<head>` section me relevant title diya gaya hai (e.g. `<title>Home - My Website</title>`, `<title>About - My Website</title>`), jo browser tabs aur search engine history me easily distinguish hota hai.

3. **Consistent Section Separators (`<hr>`)**:
   - Header, navigation aur body content ke beech standard visual dividers.
