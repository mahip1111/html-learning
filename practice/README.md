# 📘 Folder: Practice — DOM & Form Manipulation

Is folder me JavaScript DOM (Document Object Model) ke through HTML Form elements ko access aur dynamically read/manipulate karne ka concept demonstrate kiya gaya hai.

---

## 📄 1. `1.index.html` — Accessing Forms via JavaScript DOM

### 🎯 Main Concepts
1. **Accessing Form via `document.forms`**:
   - `document.forms["frm1"]`: Form ko uski `id` ya `name` se direct access karta hai bina `getElementById` ke.
2. **Reading Form Elements (`form.elements`)**:
   - `x.elements`: Form ke andar present sabhi inputs, buttons aur textareas ka array-like collection return karta hai.
   - `x.elements[i].value`: Har individual input field ki current entered value fetch karta hai.
3. **Dynamic DOM Injection (`innerHTML`)**:
   - `document.getElementById("demo").innerHTML = text;`: Extracted form data ko format karke dynamically webpage ke paragraph container me render karta hai.

```html
<form id="frm1" action="/action_page.php">
  First name: <input type="text" name="fname" value="Donald"><br>
  Last name: <input type="text" name="lname" value="Duck"><br>
  <input type="submit" value="Submit">
</form>

<p id="demo"></p>

<script>
  const myForm = document.forms["frm1"];
  let output = "";
  for (let i = 0; i < myForm.length; i++) {
    output += myForm.elements[i].value + "<br>";
  }
  document.getElementById("demo").innerHTML = output;
</script>
```
