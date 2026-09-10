# 📄 problem1 — Vertical Form Layout Without `<br>` Tags

Is document me without `<br>` tags clean vertically-aligned form structure design karne ka architectural solution explain kiya gaya hai.

---

## 🎯 1. Problem Statement & Challenge
> **Quiz**: Without using `<br>` tags, write a vertically aligned form asking for Name, City and Pincode of a user.

---

## 💡 2. Architectural Solution & Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vertically Aligned Form</title>
</head>
<body>
    <h1>Information Form</h1>
    <form method="POST">
        <!-- Div wrapper 1 -->
        <div>
            <label for="name">Enter your name:</label>
            <input type="text" id="name" name="username" placeholder="Enter your name" autofocus>
        </div>

        <!-- Div wrapper 2 -->
        <div>
            <label for="city">Enter your city:</label>
            <input type="text" id="city" name="city" placeholder="Enter your city">
        </div>

        <!-- Div wrapper 3 -->
        <div>
            <label for="pincode">Enter your pincode:</label>
            <input type="text" id="pincode" name="pincode" placeholder="Enter your pincode">
        </div>
    </form>
</body>
</html>
```

---

## 🔑 3. Why `<div>` is Superior to `<br>`

1. **Natural Block Line Breaking**: `<div>` ek block-level element hai, isliye har `<div>` block automatically 100% width occupy karke agle content ko natural nayi line par bhej deta hai.
2. **Clean Separation of Concerns**: `<br>` sirf visual line break deta hai, jabki `<div>` semantic field container banata hai jise CSS me padding, margin, flexbox ya grid ke zariye easily style kiya ja sakta hai.
