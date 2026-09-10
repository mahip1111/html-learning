# 📄 boolearn_attribute — Boolean Attributes Architecture & JSX Comparison

Is document me HTML Boolean Attributes ke syntax rules, presence-based evaluation aur modern React/JSX comparison ke concepts explain kiye gaye hain.

---

## 🎯 1. Core Rule & Working Principle

- **Presence = True**: Tag me attribute ka likha hona hi use `true` (enabled) bana deta hai.
- **Absence = False**: Tag se attribute ko hata dena use `false` (disabled) bana deta hai.

```html
<!-- Disabled is active (True) -->
<input disabled>

<!-- Equivalent legacy representations (all mean True) -->
<input disabled="disabled">
<input disabled="">
```

---

## 📋 2. Comprehensive Categorized Reference

### 1. Forms & Inputs
- `disabled`: User interaction disable karta hai.
- `readonly`: Text edit nahi karne deta, par copy karne deta hai.
- `required`: Validation — field fill karna mandatory hai.
- `checked`: Checkbox / radio button default ticked rehta hai.
- `selected`: Dropdown me default active option.
- `multiple`: Multiple files ya multiple select options allow karta hai.
- `autofocus`: Page load par automatic cursor focus.
- `novalidate`: Form par browser validation bypass karta hai.

### 2. Media Controls (`<video>`, `<audio>`)
- `controls`: Play/pause UI show karta hai.
- `autoplay`: Automatic playback trigger karta hai.
- `loop`: End hone par wapis replay karta hai.
- `muted`: Sound ko silent rakhta hai.
- `playsinline`: Mobile par automatic fullscreen popup avoid karta hai.

### 3. Interactive UI Elements
- `hidden`: Element ko display se hide karta hai.
- `<details open>`: Accordion ko default expanded show karta hai.
- `draggable`: Element drag-and-drop enabled banata hai.

---

## ⚛️ 3. React / JSX Comparison

React/JSX me dynamic boolean logic support karne ke liye explicit boolean expressions pass kiye jate hain:

```jsx
// Enabled / True
<input disabled={true} />

// Disabled / False (attribute inactive)
<input disabled={false} />
```
