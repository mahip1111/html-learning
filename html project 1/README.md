# 📘 Folder: HTML Project 1 — Real World Applications

Is folder me HTML ke core concepts ko use karke 2 complete real-world projects banaye gaye hain: **Student Registration Form** aur **Professional Resume / Portfolio**.

---

## 📄 1. `form_registration.html` — Comprehensive Registration Form

### 🎯 Main Concepts
1. **Form Sectioning (`<fieldset>` & `<legend>`)**:
   - `<fieldset>`: Related form controls ke around ek visible grouped border box draw karta hai.
   - `<legend>`: Us fieldset box ka caption / title banata hai (e.g. "Personal Details", "Education Details").
2. **Diverse Input Types**:
   - `type="email"`: Auto browser email format validation (`@` and domain check).
   - `type="password"`: Entered text ko masked dots me chupata hai.
   - `type="tel"`: Phone number input ke liye.
   - `type="date"`: Built-in calendar picker provide karta hai.
3. **Reset Button (`type="reset"`)**:
   - `<button type="reset">Clear</button>`: Pure form ke sabhi fields ko ek click me unki default initial state par reset kar deta hai.

```html
<form>
  <fieldset>
    <legend>Personal Details</legend>
    <label for="dob">Date of Birth:</label>
    <input type="date" id="dob">
  </fieldset>

  <button type="submit">Register</button>
  <button type="reset">Clear</button>
</form>
```

---

## 📄 2. `resume.html` — Semantic CV / Resume Website

### 🎯 Main Concepts
1. **Thematic Breaks (`<hr>`)**:
   - Horizontal rule line draw karta hai sections ke beech clear visual separation ke liye.
2. **Tabular Education Details**:
   - `<table border="3" cellpadding="20">`: Tabular data layout with cell padding spacing.
3. **Structured Information Layout**:
   - Unordered list (`<ul>`) for bulleted skills & achievements.
   - Ordered list (`<ol>`) for numbered project portfolio.
   - Inline bold emphasis (`<b>`) and direct mail/profile links.

```html
<h2>Education</h2>
<table border="1" cellpadding="10">
  <tr>
    <th>Course</th>
    <th>Institute</th>
    <th>Year</th>
  </tr>
  <tr>
    <td>B.Tech</td>
    <td>IIIT BBSR</td>
    <td>2024-2028</td>
  </tr>
</table>

<hr>

<h2>Projects</h2>
<ol>
  <li><b>Resume Website</b> — HTML-only project</li>
</ol>
```
