# 📄 1basic — HTML Document Anatomy & Character Encoding

Is document me HTML document ke basic structure, standard boilerplate aur character encoding (`UTF-8`) ke core concepts explain kiye gaye hain.

---

## 🎯 1. HTML Core Boilerplate Anatomy

Har standard HTML5 webpage ka basic skeleton is tarah organize hota hai:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Website</title>
</head>
<body>
    Hello World how are you king is back
</body>
</html>
```

---

## 🔑 2. Element-by-Element Breakdown

### 1. `<!DOCTYPE html>`
- **Meaning**: Document Type Declaration.
- **Function**: Browser ko batata hai ki ye modern **HTML5** standard document hai taaki browser *Standards Mode* me render kare na ki outdated *Quirks Mode* me.

### 2. `<html lang="en">`
- **Meaning**: Root Container.
- **Function**: Poori website ka outermost parent container hai jiske andar `<head>` aur `<body>` aate hain.
- `lang="en"`: Language attribute search engines (SEO) aur screen readers ko batata hai ki page ka primary content English me hai.

### 3. `<head>`
- **Meaning**: Metadata & Configuration Head.
- **Function**: Isme browser settings, character set, responsive scaling, CSS links aur tab title hote hain jo directly webpage ke UI par visible nahi hote par browser/search engine processing ke liye mandatory hain.

### 4. `<meta charset="UTF-8">` — Character Encoding Mechanism
- **Encoding ka Concept**: Computer har character (alphabet, number, special symbol, emoji jaise 🚀, 🔥, ya Hindi akshar) ko direct samajh nahi sakta, wo unhe binary digits (`0` aur `1`) me store karta hai.
- **Decoding**: Jab browser file open karta hai to binary values ko wapis readable text/symbols me convert karta hai.
- **UTF-8 Importance**: `UTF-8` globally standard Unicode encoding hai jo duniya ki lagbhag har language aur emojis ko bina corrupt huye seamlessly render karti hai.

### 5. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- **Function**: Mobile responsiveness ke liye sabse important meta tag:
  - `width=device-width`: Page layout ki width device screen ki actual width ke barabar karta hai.
  - `initial-scale=1.0`: Page load hone par default zoom level 100% rakhta hai.

### 6. `<title>`
- **Function**: Browser tab ke top header par aur bookmarks / Google search results me jo headline dikhti hai, wo yahan define hoti hai.

### 7. `<body>`
- **Function**: Visible Viewport Container. Iske andar jo bhi elements (headings, text, images, videos, forms) likhe jayenge, wahi user ko webpage par visually show honge.

---

## 💡 Key Summary
- `<!DOCTYPE html>` $\rightarrow$ HTML5 Declaration
- `<html>` $\rightarrow$ Full Website Wrapper
- `<head>` $\rightarrow$ Meta Settings & Browser Info
- `<meta charset="UTF-8">` $\rightarrow$ Universal Text/Emoji Encoding
- `<meta name="viewport">` $\rightarrow$ Mobile Screen Scaling
- `<title>` $\rightarrow$ Browser Tab Title
- `<body>` $\rightarrow$ Visible Page UI
