# 📄 form_registration — Student Registration Form Application

Is document me HTML `<fieldset>`, `<legend>`, diverse input types (`email`, `password`, `tel`, `date`), grouped selection dropdowns, multi-checkbox skills layout aur reset button ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html>
<head>
  <title>Student Registration Form</title>
</head>
<body>
  <h1>Student Registration Form</h1>
  <p>Fill the form carefully.</p>

  <form>
    <!-- Section 1: Personal Details -->
    <fieldset>
      <legend>Personal Details</legend>
      <label for="name">Full Name:</label>
      <input id="name" name="name" type="text" placeholder="Enter full name" required><br><br>

      <label for="email">Email:</label>
      <input id="email" type="email" placeholder="Enter email"><br><br>

      <label for="password">Password:</label>
      <input id="password" type="password" placeholder="Enter password"><br><br>

      <label for="tel">Phone:</label>
      <input id="tel" type="tel" placeholder="Enter phone"><br><br>

      <label for="date">Date of Birth:</label>
      <input id="date" type="date"><br><br>

      <label>Gender:</label><br>
      <input type="radio" name="gender" value="male"> Male
      <input type="radio" name="gender" value="female"> Female
      <input type="radio" name="gender" value="other"> Other
    </fieldset>

    <!-- Section 2: Education Details -->
    <fieldset>
      <legend>Education Details</legend>
      <label>Course:</label>
      <select name="course">
        <option value="">Select Course</option>
        <option value="bca">BCA</option>
        <option value="btech">BTech</option>
        <option value="mca">MCA</option>
      </select>
    </fieldset>

    <!-- Section 3: Skills -->
    <fieldset>
      <legend>Skills</legend>
      <input type="checkbox" name="skills" value="html"> HTML <br>
      <input type="checkbox" name="skills" value="css"> CSS <br>
      <input type="checkbox" name="skills" value="js"> JavaScript <br>
      <input type="checkbox" name="skills" value="react"> React
    </fieldset>

    <br>
    <!-- Actions -->
    <button type="submit">Register</button>
    <button type="reset">Clear Form</button>
  </form>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Form Sectioning with `<fieldset>` & `<legend>`
- `<fieldset>`: Grouped form fields ke charon taraf ek clean boundary border draw karta hai.
- `<legend>`: Us border box ke upar embedded title label define karta hai.

### 2. Diverse Input Types
- `type="email"`: Built-in browser validation karta hai (invalid email enter karne par form submit block ho jata hai).
- `type="password"`: Typed characters ko secret dots (`•••`) me mask karta hai.
- `type="tel"`: Mobile devices par numeric dial keypad open karta hai.
- `type="date"`: Built-in date-picker calendar widget launch karta hai.

### 3. Reset Button Action (`type="reset"`)
- `<button type="reset">Clear Form</button>`: Pure form ke sabhi fields ko ek click me unki default initial state par restore/clear kar deta hai.
