# 📄 5 — HTML Boolean Attributes Complete Reference

Is document me HTML Boolean Attributes ke syntax rules, truthy/falsy behavior aur har common boolean attribute ki practical working explain kiye gaye hain.

---

## 🎯 1. Boolean Attribute Core Mechanism

- **ON / OFF Rule**:
  - Attribute present in element = **TRUE** ✅
  - Attribute absent from element = **FALSE** ❌
- **No Value Required**: Inhe koi value specify karna mandatory nahi hai:
  - `<input disabled>` $\equiv$ `<input disabled="disabled">` $\equiv$ `<input disabled="">`

---

## 📋 2. Comprehensive Boolean Attributes Reference Table

| Boolean Attribute | Compatible Tags | Purpose & Effect |
| :--- | :--- | :--- |
| `required` | `<input>`, `<select>`, `<textarea>` | Form submit karne ke liye field ko compulsory banata hai |
| `disabled` | `<input>`, `<button>`, `<select>`, `<textarea>` | Element ko non-clickable, non-focusable aur greyed out karta hai |
| `readonly` | `<input>`, `<textarea>` | Text ko read/copy karne deta hai par modify karne se block karta hai |
| `checked` | `<input type="checkbox">`, `<input type="radio">` | Element ko by-default checked/ticked state me render karta hai |
| `selected` | `<option>` | Dropdown list me item ko default highlighted option banata hai |
| `autofocus` | All form controls | Page load hote hi input field par cursor focus karta hai |
| `multiple` | `<select>`, `<input type="file">` | Ek sath multiple items/files select karne deta hai |
| `hidden` | All HTML elements | Element ko visually page se hide kar deta hai |
| `controls` | `<video>`, `<audio>` | Play, pause, seek bar aur volume controls render karta hai |
| `autoplay` | `<video>`, `<audio>` | Page load hote hi media playback start karta hai |
| `loop` | `<video>`, `<audio>` | Media khatam hone par wapis starting se play karta hai |
| `muted` | `<video>`, `<audio>` | Audio ko by-default silent/mute rakhta hai |
