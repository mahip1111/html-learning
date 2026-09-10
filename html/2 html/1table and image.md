# 📄 1table and image — HTML Tables, Images & Error Tolerance

Is document me HTML Tables (`<table>`), Table Headers, Rows, Data cells, Column/Row Spanning (`colspan`, `rowspan`), Image embedding (`<img>`) aur HTML Parser Error Forgiveness ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tables and Images</title>
</head>
<body>
  <!-- Image Tag -->
  <img width="400" height="230" src="train image.jpg" alt="Train image">

  <!-- Table Structure -->
  <table>
    <caption>Student Details</caption>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Country</th>
    </tr>
    <tr>
      <td>Maheep</td>
      <td>18</td>
      <td>India</td>
    </tr>
    <tr>
      <td>Paarth</td>
      <td>16</td>
      <td>India</td>
    </tr>
  </table>  
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Image Element (`<img>`) & Attributes
- `src="..."`: Image file ka source/path specify karta hai.
- `alt="..."` (Alternative Text):
  - Agar image network issue ya broken path ki wajah se load na ho, to screen par `alt` text display ho jata hai.
  - Visually impaired users ke screen readers is text ko padh kar image ka context samjhate hain.
  - SEO ke liye mandatory attribute hai.
- `width` & `height`: Dimensions in pixels. Explicit width/height define karne se page load ke dauran browser pehle se space reserve kar leta hai, jisse **Cumulative Layout Shift (CLS)** prevent hota hai.

### 2. Table Elements Structure
- `<table>`: Table ka parent container.
- `<caption>`: Table ke upar uska title / caption define karta hai.
- `<tr>` (Table Row): Horizontal line/row create karta hai.
- `<th>` (Table Header): Header cells create karta hai (by default bold aur center-aligned text).
- `<td>` (Table Data): Standard table data cell (by default normal text aur left-aligned).

### 3. Merging Cells (`colspan` & `rowspan`)
- `colspan="2"`: Ek cell ko horizontal direction me **2 columns** jitna merge karta hai (Excel ke *merge across* ki tarah).
- `rowspan="2"`: Ek cell ko vertical direction me **2 rows** jitna merge karta hai.

```html
<!-- Colspan example -->
<tr>
  <th colspan="2">Full Name (Takes 2 Columns)</th>
  <th>Roll No</th>
</tr>

<!-- Rowspan example -->
<tr>
  <td rowspan="2">Science (Spans across 2 rows)</td>
  <td>Physics</td>
</tr>
<tr>
  <td>Chemistry</td>
</tr>
```

### 4. HTML Parser Forgiving Nature
- HTML ek "forgiving" language hai. Agar aap kisi tag ka closing slash bhool jayein (jaise `<td>data<td>`), to browser crash nahi hota ya error throw nahi karta, balki DOM tree banate waqt use automatically auto-correct karke render kar deta hai.
