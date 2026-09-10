# 📄 2ordered and unordered — Lists Architecture (UL, OL, DL)

Is document me HTML ki teeno major list types: Unordered List (`<ul>`), Ordered List (`<ol>`), aur Definition / Description List (`<dl>`) ke concepts explain kiye gaye hain.

---

## 🎯 1. Code Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lists</title>
</head>
<body>
    <!-- Unordered List -->
    <ul>
        <li>Maheep</li>
        <li>Rohan</li>
        <li>Paarth</li>
        <li>Ram</li>
    </ul>

    <!-- Ordered List -->
    <ol type="A">
        <li>Maheep</li>
        <li>Rohan</li>
        <li>Paarth</li>
        <li>Ram</li>
    </ol>

    <!-- Definition List -->
    <dl>
        <dt>Haloalkanes</dt>
        <dd>Alkyl halides containing alkane with halogen replacement.</dd>

        <dt>Haloarenes</dt>
        <dd>Halogen derivatives directly attached to aromatic hydrocarbons.</dd>
    </dl>
</body>
</html>
```

---

## 🔑 2. Core Concepts & Explanations

### 1. Unordered List (`<ul>`) & List Items (`<li>`)
- **Use Case**: Jab list items ka order ya sequence matter nahi karta (e.g. shopping list, features).
- **Bullet Types**:
  - Default: `disc` (solid black circle).
  - Custom attribute: `<ul type="square">` ya `<ul type="circle">`.

### 2. Ordered List (`<ol>`)
- **Use Case**: Jab list items ka chronological / sequential order matter karta hai (e.g. step-by-step recipes, rankings).
- **Numbering Types (`type="..."`)**:
  - `type="1"`: Numeric (1, 2, 3...) — Default
  - `type="A"`: Uppercase letters (A, B, C...)
  - `type="a"`: Lowercase letters (a, b, c...)
  - `type="I"`: Uppercase Roman numerals (I, II, III...)
  - `type="i"`: Lowercase Roman numerals (i, ii, iii...)
- **Custom Starting Point (`start="..."`)**:
  - `<ol start="5">`: List ko 5 number se start karta hai.

### 3. Definition / Description List (`<dl>`)
- **Use Case**: Dictionary, terms glossary, FAQ pairs ya key-value metadata display karne ke liye.
- **Components**:
  - `<dl>`: Description List wrapper container.
  - `<dt>` (Definition Term): Term ya item heading.
  - `<dd>` (Definition Description): Term ka explanation / definition (by default browser isme left indentation apply karta hai).
