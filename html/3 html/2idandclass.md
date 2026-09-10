# 📄 2idandclass — ID vs Class Selectors & URL Fragment Bookmarking

Is document me HTML `id` vs `class` attributes, CSS Specificity priority rules aur URL hash fragment (`#id`) bookmarking ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ID and Classes in HTML</title>
</head>
<body>
    <h1 class="black">IDs and Classes in Detail</h1>

    <!-- ID + Class together -->
    <div id="firstdiv" class="red">First Div</div>

    <div id="seconddiv" class="bg-black">Second Div</div>

    <span class="bg-yellow">Inline Text</span>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. `id` Attribute (Aadhaar Card Concept)
- **Unique Identifier**: Ek webpage par kisi `id` ki value unique honi chahiye (ek ID sirf ek hi element ko di ja sakti hai).
- **CSS Selector**: `#` symbol se target kiya jata hai (e.g. `#firstdiv { background: red; }`).
- **Higher Priority / Specificity**: Agar kisi element par class aur id dono se conflicting CSS styles lage hon, to **`id` selector** ki styling jeet jati hai kyunki `id` ki specificity class se high hoti hai.

### 2. `class` Attribute (Category / Trait Concept)
- **Reusable Grouping**: Multiple elements ko same class assign ki ja sakti hai (e.g. class="btn" sabhi buttons par).
- **Multiple Classes**: Ek single element me space dekar multiple classes apply ki ja sakti hain (e.g. `class="card shadow rounded"`).
- **CSS Selector**: `.` (dot) symbol se target kiya jata hai (e.g. `.red { color: red; }`).

### 3. URL Fragment Navigation & Bookmarking (`#id`)
- **Direct Section Scrolling**: Webpage ke kisi specific element tak direct scroll karne ke liye URL ke aage `#` ke sath us element ki `id` add ki jati hai.
- **Example**: `https://en.wikipedia.org/wiki/Computer_programming#Algorithmic_complexity`
- Jab user ye URL open karega, browser automatically us page ke `#Algorithmic_complexity` ID wale heading/section par jump kar dega.
