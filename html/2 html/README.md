# 📘 Folder 2: Tables, Lists, Media, SEO/Web Vitals & Forms

Is folder me HTML tables, images, lists (ordered, unordered, description), Core Web Vitals (SEO performance), interactive forms aur HTML boolean attributes ke concepts cover kiye gaye hain.

---

## 📄 1. `1table and image.html` — Tables & Images

### 🎯 Main Concepts
1. **Image Tag (`<img>`)**:
   - `src="..."`: Image file ka source/path specify karta hai.
   - `alt="..."` (Alternative Text): Agar image load na ho ya screen reader use ho raha ho, to ye text display hota hai. Accessibility aur SEO ke liye compulsory hai.
   - `width` & `height`: Image ke dimensions define karte hain. Explicit width/height specify karne se page load ke time layout shift (CLS) nahi hota.

2. **Data Tables Structure**:
   - `<table>`: Table ka main container.
   - `<caption>`: Table ke upar uski heading / title define karta hai.
   - `<tr>` (Table Row): Ek horizontal row create karta hai.
   - `<th>` (Table Header): Header cell (by default bold aur center-aligned hota hai).
   - `<td>` (Table Data): Standard data cell.

3. **Merging Cells (`colspan` & `rowspan`)**:
   - `colspan="2"`: Excel ke *merge across* ki tarah cell ko **2 columns** ki width jitna stretch/merge karta hai.
   - `rowspan="2"`: Cell ko vertically **2 rows** me merge karta hai.

4. **HTML Forgiving Nature**:
   - Agar kisi tag ka closing slash bhool jayein, to HTML browser parser use automatically fix karne ki koshish karta hai bina fatal error throw kiye.

```html
<img src="train image.jpg" alt="Train image" width="400" height="230">

<table>
  <caption>Student Details</caption>
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Maheep</td>
    <td>Gupta</td>
    <td>18</td>
  </tr>
</table>
```

---

## 📄 2. `2ordered and unordered .html` — Lists Architecture

### 🎯 Main Concepts
1. **Unordered List (`<ul>`)**:
   - Bullet points wali list. By default `disc` bullets aate hain.
   - `type="square"` / `type="circle"`: Bullet style change karne ke liye.

2. **Ordered List (`<ol>`)**:
   - Numbered/sequence wali list. By default numeric (`1, 2, 3...`) aate hain.
   - `type="A"` / `type="a"` / `type="I"` / `type="i"`: Alphabetic ya Roman numbering set karne ke liye.

3. **Description / Definition List (`<dl>`)**:
   - Glossary ya dictionary style terms & explanations ke liye use hota hai.
   - `<dt>` (Definition Term): Term ya heading.
   - `<dd>` (Definition Description): Us term ka detail/explanation (by default indented hota hai).

```html
<!-- Unordered List -->
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>

<!-- Ordered List with Letters -->
<ol type="A">
  <li>First Step</li>
  <li>Second Step</li>
</ol>

<!-- Definition List -->
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>
```

---

## 📄 3. `3towatch.html` — SEO & Core Web Vitals (Performance Metrics)

### 🎯 Main Concepts
1. **SEO (Search Engine Optimization)**:
   - Search engines (Google) fast-loading, well-structured aur high-quality user experience wale pages ko top rank dete hain.

2. **Google Core Web Vitals**:
   - **CLS (Cumulative Layout Shift)**: Page load hone ke dauran elements screen par kitna hilte/jump karte hain. Score kam se kam hona chahiye. *(Images par `width` aur `height` dene se layout jump prevent hota hai).*
   - **LCP (Largest Contentful Paint)**: Page ka sabse bada visual element (hero banner/image/heading) kitni der me render hota hai. Ideal time: **< 2.5 seconds**.
   - **FID / INP (First Input Delay / Interaction to Next Paint)**: Jab user kisi button ya link par click karta hai, to browser kitni jaldi respond karta hai. Target: **< 100ms**.

3. **Chrome DevTools Lighthouse & Emulation**:
   - `Right click -> Inspect -> Lighthouse`: Page ka Performance, Accessibility, Best Practices aur SEO score audit karta hai.
   - Device Mode (`Ctrl + Shift + M`): Webpage ko alag-alag mobile screen sizes par test karne ke liye.

---

## 📄 4. `4.from and input,.html` — Comprehensive Forms & User Input

### 🎯 Main Concepts
1. **Form Container (`<form>`)**:
   - User se data collect karke server par bhejta hai.
   - `method="GET"` (URL query params me data bhejta hai) vs `method="POST"` (request body me securely data bhejta hai).

2. **Labels & Accessibility Connection**:
   - `<label for="inputId">` ko `<input id="inputId">` ke sath map kiya jata hai. Label par click karne se automatically related input focus/check ho jata hai.

3. **Input Types & Attributes**:
   - `type="text"`: Single-line text input.
   - `placeholder="..."`: Box ke andar faint hint text.
   - `required`: Validation — bina fill kiye form submit nahi hoga.
   - `autofocus`: Page load hote hi cursor automatically is input me focus ho jayega.

4. **Radio Buttons vs. Checkboxes**:
   - **Radio (`type="radio"`)**: Mutually exclusive choice (sirf ek select ho sakta hai). Sabhi options ka `name="..."` **same** hona chahiye (e.g. `name="gender"`).
   - **Checkbox (`type="checkbox"`)**: Multiple ya independent on/off options select karne ke liye.

5. **Multi-line Text (`<textarea>`)**:
   - Paragraphs / comments enter karne ke liye. `rows` (vertical lines) aur `cols` (width in characters) se size control hota hai.

6. **Dropdown Selection (`<select>` & `<option>`)**:
   - Options ki drop-down list provide karta hai space save karne ke liye.

7. **Script Execution & DOM Blocking**:
   - Agar `<script>` tag ko HTML content ke beech me likha jaye, to browser HTML parsing pause karke pehle JavaScript execute karta hai (jaise alert prompt aana). Isliye scripts ko usually `</body>` ke theek pehle rakha jata hai.

```html
<form method="POST">
  <div>
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" placeholder="Enter username" required autofocus>
  </div>

  <div>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
  </div>

  <div>
    <select name="country" id="country">
      <option value="in">India</option>
      <option value="us">USA</option>
    </select>
  </div>

  <div>
    <textarea name="feedback" rows="4" cols="50" placeholder="Your feedback"></textarea>
  </div>
</form>
```

---

## 📄 5. `5.html` — HTML Boolean Attributes

### 🎯 Main Concepts
**Boolean Attribute Mechanism**:
HTML me boolean attributes ON/OFF switch ki tarah kaam karte hain:
- **Present in tag = TRUE** (Enable)
- **Absent from tag = FALSE** (Disable)

| Boolean Attribute | Kisme Use Hota Hai | Function / Meaning |
| :--- | :--- | :--- |
| `required` | `<input>`, `<select>`, `<textarea>` | Field ko mandatory banata hai |
| `disabled` | Any form control / button | Element ko un-clickable aur inactive kar deta hai |
| `readonly` | `<input>`, `<textarea>` | User text edit nahi kar sakta par copy kar sakta hai |
| `checked` | `radio`, `checkbox` | Default pre-selected state |
| `selected` | `<option>` | Dropdown me default selected item |
| `autofocus` | Form controls | Page load par automatic focus |
| `multiple` | `<select>`, `<input type="file">` | Multiple files ya options select karne deta hai |
| `hidden` | Any HTML tag | Element ko visual display se hide kar deta hai |
| `controls` | `<video>`, `<audio>` | Play/pause/volume controls dikhata hai |
| `autoplay` | `<video>`, `<audio>` | Page load hote hi media play karta hai |
| `loop` | `<video>`, `<audio>` | Media khatam hone par wapis repeat karta hai |
| `muted` | `<video>`, `<audio>` | Default sound silent / mute rakhta hai |
