# 📘 Folder: Self HTML Learning Notes

Is folder me HTML ke advanced attributes, meta architecture, link tag relationships aur boolean attributes ke in-depth conceptual notes diye gaye hain.

---

## 📄 1. `about_link_tag.html` — The `<link>` Tag Mechanics

### 🎯 Main Concepts
1. **Purpose**:
   - External documents / resources ko HTML document ke sath link karta hai (sabse common use: external CSS stylesheets connect karna).
2. **Attribute Breakdown**:
   - `<link>`: Void/unpaired tag jo `<head>` section me place hota hai.
   - `rel="stylesheet"` (Relationship): Browser ko batata hai ki target file kis relation me jud rahi hai (yahan: styling rulesheet).
   - `href="style.css"` (Hypertext Reference): CSS file ka relative/absolute path.

```html
<link rel="stylesheet" href="style.css">
<!-- Browser ko instruct karta hai: "style.css se styling rules le kar is page par apply karo" -->
```

---

## 📄 2. `boolearn_attribute.html` — HTML Boolean Attributes Deep Dive

### 🎯 Main Concepts
1. **Core Rule**:
   - Boolean attribute ka **presence (exist hona) = TRUE** hota hai aur **absence (na hona) = FALSE** hota hai.
   - Inhe value assign karna zaroori nahi hota (`<input disabled>` is equivalent to `<input disabled="disabled">`).

2. **Categorized Boolean Attributes**:

| Category | Attributes | Use-case & Description |
| :--- | :--- | :--- |
| **Forms & Inputs** | `disabled` | Input/button ko inactive aur unclickable banata hai |
| | `readonly` | Text editable nahi hota, par user copy kar sakta hai |
| | `required` | Form submission se pehle field fill karna mandatory hai |
| | `checked` | Checkbox ya radio button ko default ticked rakhta hai |
| | `selected` | `<option>` ko dropdown me default selected rakhta hai |
| | `multiple` | Dropdown ya file input me multiple items select karne deta hai |
| | `autofocus` | Page load par cursor automatically field me place karta hai |
| | `novalidate` | `<form novalidate>` default browser validation disable karta hai |
| **Media (`<video>`/`<audio>`)** | `controls` | Native play/pause/volume UI dikhata hai |
| | `autoplay` | Page load hote hi media play karta hai |
| | `loop` | End hone par wapis replay karta hai |
| | `muted` | Audio mute rakhta hai |
| | `playsinline` | Mobile browsers me fullscreen jane ke badle inline play karta hai |
| **Interactive UI** | `hidden` | Element ko completely visually hide karta hai |
| | `<details open>` | Collapsible accordion ko default expanded rakhta hai |
| | `draggable` | Element ko drag-and-drop enabled banata hai |

3. **React / JSX Comparison**:
   - Standard HTML: `<input disabled>`
   - React / JSX: `<input disabled={true} />` ya `<input disabled={false} />`

---

## 📄 3. `meta_tag_and_attribute.html` — Metadata, Viewport & Attributes Pairing

### 🎯 Main Concepts
1. **Metadata Definition ("Data about Data")**:
   - `<meta>` tags webpage ka underlying data represent karte hain jo browser, search engine bots aur devices read karte hain.

2. **The `name` vs `content` Pairing Mechanism**:
   - `name="..."` $\rightarrow$ Batata hai ki **"Kis cheez ki information de rahe ho?"** (Property / Key).
   - `content="..."` $\rightarrow$ Batata hai ki **"Us information ki actual value kya hai?"** (Data / Value).

```html
<!-- Example 1: Viewport -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Example 2: SEO Description -->
<meta name="description" content="Tutorial on modern HTML5 architecture">

<!-- Example 3: Search Engine Robots -->
<meta name="robots" content="index, follow">
```

3. **Viewport Deep Dive (`width=device-width, initial-scale=1.0`)**:
   - `width=device-width`: Page ki layout width ko mobile device ki physical screen width ke barabar karta hai (360px screen = 360px layout).
   - `initial-scale=1.0`: Default zoom level ko 100% par lock karta hai.
   - **Why Critical?**: Agar ye tag na ho, to mobile browser desktop resolution (e.g. 980px) assume karke page ko tiny zoom-out karke dikhayega, aur CSS `@media` queries mobile me trigger nahi hongi!

---

## 📄 4. `video_tag.html` — Modern Video Tag Standards & Fallbacks

### 🎯 Main Concepts
1. **Multi-source Video Architecture**:
   - Alag-alag browsers alag video formats support karte hain (MP4, WebM, Ogg). Multiple `<source>` tags dene se browser best compatible format automatically select kar leta hai.

```html
<video width="640" height="360" controls poster="thumbnail.jpg" preload="metadata">
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    Your browser does not support the video tag.
</video>
```
