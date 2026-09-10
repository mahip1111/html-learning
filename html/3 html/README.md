# 📘 Folder 3: Elements, Selectors, Multimedia, Semantics & Iframe Targeting

Is folder me Block vs Inline elements, IDs vs Classes, HTML5 Multimedia (Audio, Video, SVG), Semantic tags, Quotations, Entities, Code formatting aur Iframe dynamic targeting ke concepts cover kiye gaye hain.

---

## 📄 1. `1blockandinline.html` — Block vs Inline Elements

### 🎯 Main Concepts
1. **Block-level Elements**:
   - Webpage par **poori available width (100%)** occupy karte hain.
   - Hamesha nayi line se start hote hain (automatic line break).
   - *Examples*: `<p>`, `<div>`, `<h1>`-`<h6>`, `<ul>`, `<ol>`, `<form>`, `<section>`.
   - `<div>`: Generic container jo styling aur layout structuring ke liye use hota hai.

2. **Inline Elements**:
   - Sirf utni hi width lete hain jitni unke content/text ko chahiye.
   - Ek doosre ke bagal me (same line par) render hote hain jab tak line bhar na jaye.
   - *Examples*: `<a>`, `<span>`, `<strong>`, `<em>`, `<img>`.
   - `<span>`: Generic inline container jo kisi text ke chote se hisse ko bina layout disturb kiye style/target karne ke liye use hota hai.

3. **Behavior Customization**:
   - CSS `display` property (`display: block;`, `display: inline;`, `display: inline-block;`) ke through kisi bhi element ka default behavior change kiya ja sakta hai.

```html
<!-- Block element: Takes full width -->
<p>I am a block element</p>

<!-- Inline elements: Sit side-by-side -->
<span>Part 1</span>
<a href="https://bing.com" target="_blank">Part 2 (Link)</a>
```

---

## 📄 2. `2idandclass.html` — ID vs Class Selectors & URL Bookmarking

### 🎯 Main Concepts
1. **`id` Attribute (Aadhaar Card Concept)**:
   - Page par unique identifier hota hai (ek ID sirf ek hi element ko di jani chahiye).
   - CSS specificity me `id` ki priority `class` se **higher** hoti hai.

2. **`class` Attribute (Category/Properties Concept)**:
   - Multiple elements ko share kiya ja sakta hai (e.g., `class="btn red"`).
   - Ek element me space dekar multiple classes assign ki ja sakti hain.

3. **Direct Section Bookmarking / URL Hash (`#id`)**:
   - Kisi bhi webpage ke specific section par directly navigate karne ke liye URL ke aage `#id_name` lagaya jata hai (e.g., `site.com/page.html#section2`).

```html
<!-- ID (unique) vs Class (reusable) -->
<h1 class="heading">Page Title</h1>
<div id="firstdiv" class="red text-large">Unique Block</div>
```

---

## 📄 3. `3.video and audio.html` — HTML5 Multimedia, SVG & Iframe

### 🎯 Main Concepts
1. **HTML5 `<video>` Tag Attributes**:
   - `src`: Video file path.
   - `controls`: Native play/pause, seekbar aur volume button enable karta hai.
   - `autoplay` & `muted`: Page load par auto-play (Note: modern browsers bina `muted` ke autoplay block kar dete hain).
   - `loop`: Video khatam hone par dubara start karta hai.
   - `poster="image.jpg"`: Video play hone se pehle thumbnail image display karta hai.

2. **HTML5 `<audio>` Tag Attributes & `preload`**:
   - `preload="none"`: User ke play click karne tak audio download start nahi hoti (bandwidth bachti hai).
   - `preload="metadata"`: Sirf audio duration aur basic track info pehle load hoti hai.
   - `preload="auto"`: Browser background me audio data load karke ready rakhta hai.

3. **Scalable Vector Graphics (`<svg>`)**:
   - Resolution-independent vector shapes jo bina pixelate/blur huye kisi bhi screen size par zoom ho sakte hain.
   - `<svg width="100" height="100">`: Drawing canvas.
   - `<circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />`:
     - `cx`, `cy`: Circle ka center coordinates.
     - `r`: Circle ka radius (40px -> 80px diameter).
     - `stroke` & `stroke-width`: Border color aur thickness.
     - `fill`: Inner background color.

4. **Inline Frames (`<iframe>`)**:
   - Apni website ke frame me kisi doosri webpage ya document ko embed karna.

```html
<!-- Video with poster and loop -->
<video src="video.mp4" width="400" height="300" poster="nature.jpg" controls muted loop></video>

<!-- Audio with preload auto -->
<audio src="audio.mp3" controls preload="auto"></audio>

<!-- SVG vector circle -->
<svg height="100" width="100">
    <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>
```

---

## 📄 4. `4.semantic tags.html` — Semantic Layout Architecture

### 🎯 Main Concepts
1. **Semantic Tags Ka Purpose**:
   - Non-semantic tags (`<div>`, `<span>`) sirf layout boxes banate hain par content ka matlab nahi batate.
   - Semantic tags browser, search engine crawlers (SEO) aur screen readers ko page ka exact structure samjhate hain.

2. **Key Semantic Elements**:
   - `<header>`: Page ya section ka top banner (logo, site title).
   - `<nav>`: Primary navigation links container.
   - `<main>`: Webpage ka unique central content area (page par 1 hi hona chahiye).
   - `<section>`: Thematic grouping of content (e.g. Services section, Testimonials).
   - `<article>`: Independent, self-contained reusable content (blog post, news card).
   - `<aside>`: Sidebars ya related contextual links.
   - `<footer>`: Bottom footer (copyright, privacy links, author info).
   - `<figure>` & `<figcaption>`: Image/chart with its associated caption.
   - `<time>`: Machine-readable dates/times.

```html
<header>
    <nav>
        <ul>
            <li>Home</li>
            <li>About</li>
        </ul>
    </nav>
</header>
<main>
    <article>
        <h1>Article Heading</h1>
        <p>Main content...</p>
    </article>
</main>
<footer>
    <p>&copy; 2026 All Rights Reserved.</p>
</footer>
```

---

## 📄 5. `5.Quotation.html` & `5.entities.html` — Quotes, Preformatted Text & HTML Entities

### 🎯 Main Concepts
1. **Quotations (`<q>` vs `<blockquote>`)**:
   - `<q cite="url">`: Short inline quotes ke liye. Browser automatically around quotation marks `“...”` add karta hai.
   - `<blockquote cite="url">`: Long block quotes ke liye. Browser automatically left/right indentation deta hai.
   - `cite="..."`: Source document ka URL define karta hai (SEO & semantic indexing ke liye).

2. **Preformatted Text (`<pre>`)**:
   - HTML normal spaces aur enter (line-breaks) ko collapse karke single space bana deta hai.
   - `<pre>` tag code, poetry ya text ke exact spaces, indentation aur new lines ko preserve karke monospace font me render karta hai.

3. **HTML Entities (Character Escaping)**:
   - HTML ke reserved characters (jaise `<` aur `>`) ko screen par display karne ke liye entities use ki jati hain:
     - `&lt;` $\rightarrow$ `<` (Less than)
     - `&gt;` $\rightarrow$ `>` (Greater than)
     - `&amp;` $\rightarrow$ `&` (Ampersand)
     - `&nbsp;` $\rightarrow$ Non-Breaking Space (extra visual spaces ke liye)
     - `&copy;` $\rightarrow$ `©` (Copyright symbol)

```html
<!-- Quotes -->
<p>He said, <q cite="source.html">Hard work never fails.</q></p>

<blockquote cite="https://example.com">
    This is a long quotation excerpt from a famous speech.
</blockquote>

<!-- Preserved spacing and entities -->
<pre>
Line 1        Spaced text
Line 2
</pre>
<p>&lt;p&gt;Copyright &copy;&nbsp;&nbsp;&nbsp;Company&lt;/p&gt;</p>
```

---

## 📄 6. `6.use of code tag.html` — Code Blocks & Syntax Presentation

### 🎯 Main Concepts
1. **`<code>` Tag**:
   - Computer code snippets ko semantically mark karne ke liye use hota hai (monospace font me render hota hai).
2. **Combining `<pre>` and `<code>`**:
   - Multi-line code block display karne ke liye `<pre><code>...</code></pre>` standard pattern use hota hai taaki indentation aur line breaks intact rahein.

```html
<pre>
  <code>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;body&gt;Hello&lt;/body&gt;
&lt;/html&gt;
  </code>
</pre>
```

---

## 📄 7. Practical Quiz & Problem Solutions

### 🎯 `problem1.html` — Vertical Form Without `<br>`
- **Technique**: Har `<label>` aur `<input>` pair ko ek `<div>` wrapper me wrap karne se automatic line breaks create hote hain kyunki `<div>` ek block-level element hai. Ye `<br>` tags use karne se zyada clean aur standard layout practice hai.

### 🎯 `problem2.html` — Media Collection Showcase
- Audio, video aur image tags ko multiple responsive container blocks me assemble karna with native controls and thumbnail posters.

### 🎯 `problem2b.html` — Dynamic Media Switching via Named `<iframe>`
- **Technique**: Ek `<iframe>` ko `name="iframe_a"` attribute diya jata hai, aur anchor links par `target="iframe_a"` lagaya jata hai. Jab user kisi link par click karta hai, to whole page reload hone ke badle media usi single iframe ke andar smoothly switch ho jata hai!

```html
<!-- Named iframe target pattern -->
<iframe src="video.mp4" name="media_frame" width="500" height="300"></iframe>

<p><a href="video1.mp4" target="media_frame">Play Video 1</a></p>
<p><a href="video2.mp4" target="media_frame">Play Video 2</a></p>
```
