# 📄 meta_tag_and_attribute — Metadata, Viewport Mechanics & Key-Value Pairing

Is document me HTML Metadata ("Data about Data"), Meta tags ke `name` vs `content` attributes ka exact pairing mechanism aur Mobile Viewport Scaling rules explain kiye gaye hain.

---

## 🎯 1. What is Metadata?

- **Definition**: Metadata ka matlab hai *"Data about Data"*. Yani HTML page ke baare me wo technical background information jo direct page par visible nahi hoti, par browser, search engine bots (Google) aur mobile devices ke rendering engine ke liye essential hoti hai.

---

## 🔑 2. The `name` vs `content` Pairing Concept

Har standard `<meta>` tag key-value pair ke format me work karta hai:

1. **`name="..."`** $\rightarrow$ **"Kis cheez ki info de rahe ho?"** (Property / Metric Name)
2. **`content="..."`** $\rightarrow$ **"Us info ki actual setting / value kya hai?"** (Actual Value)

```html
<!-- Viewport Settings -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- SEO Description -->
<meta name="description" content="Complete guide on modern HTML5 architecture">

<!-- Search Engine Indexing Rules -->
<meta name="robots" content="index, follow">

<!-- Page Author -->
<meta name="author" content="Maheep">
```

---

## 📱 3. Mobile Viewport Deep Dive

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 🔍 Parameter Analysis:
1. `name="viewport"`: Browser ko instruct karta hai ki mobile screen ke visual viewport settings apply karein.
2. `content="width=device-width"`: Page ki layout width ko phone ki physical pixel width (e.g. 360px, 390px) ke equal karta hai.
3. `initial-scale=1.0`: Initial zoom level 100% (normal) par lock karta hai.

### ⚠️ Agar Ye Tag Na Ho To Kya Hoga?
- Mobile browser webpage ko desktop viewport (e.g. 980px) assume karega aur poore page ko tiny zoom-out karke dikhayega.
- Text chhota aur unreadable ho jayega.
- Sabse bada issue: **CSS `@media` queries mobile screen par trigger nahi hongi!**
