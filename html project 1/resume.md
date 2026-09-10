# 📄 resume — Semantic Developer Resume / Portfolio

Is document me HTML CV / Resume design, Thematic breaks (`<hr>`), Tabular academic history (`<table>`), Nested lists aur Contact form integration ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Resume</title>
</head>
<body>
  <h1>Manavendra Gupta</h1>
  <p><b>Email:</b> guptamanavendra6@gmail.com</p>
  <p><b>Phone:</b> +91-9796211326</p>
  <p><b>LinkedIn:</b> <a href="#">linkedin.com/in/Manavendra</a></p>

  <hr>

  <h2>Education</h2>
  <table border="3" cellpadding="15">
    <tr>
      <th>Course</th>
      <th>Institute</th>
      <th>Year</th>
      <th>Result</th>
    </tr>
    <tr>
      <td>B-Tech</td>
      <td>IIIT Bbsr</td>
      <td>2029</td>
      <td>8.5 CGPA</td>
    </tr>
    <tr>
      <td>12th</td>
      <td>Govt. High Secondary School</td>
      <td>2024</td>
      <td>85%</td>
    </tr>
  </table>

  <hr>

  <h2>Skills</h2>
  <ul>
    <li>HTML5</li>
    <li>C / C++</li>
    <li>Basic DSA</li>
  </ul>

  <hr>

  <h2>Projects</h2>
  <ol>
    <li><b>Resume Website</b> - HTML only project</li>
    <li><b>Restaurant Menu</b> - Menu layout using table</li>
  </ol>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Thematic Visual Breaks (`<hr>`)
- `<hr>`: Horizontal Rule tag jo resume ke alag-alag sections (Education, Skills, Projects, Contact) ke beech visual divider create karta hai.

### 2. Tabular Academic Data
- `<table border="3" cellpadding="15">`:
  - `border`: Table borders create karta hai.
  - `cellpadding`: Cells ke andar text aur border ke beech spacing (padding) deta hai.

### 3. Hierarchical Lists
- `<ul>`: Non-numbered bulleted list skills aur achievements ke liye.
- `<ol>`: Numbered sequential list major projects ke liye.
