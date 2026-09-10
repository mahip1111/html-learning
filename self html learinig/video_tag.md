# 📄 video_tag — Modern HTML5 Video Architecture & Fallbacks

Is document me HTML5 `<video>` tag ke standard properties, multiple `<source>` fallback mechanisms aur cross-device video optimization rules explain kiye gaye hain.

---

## 🎯 1. Modern Multi-Source Video Boilerplate

```html
<video width="640" height="360" controls poster="thumbnail.jpg" preload="metadata" playsinline>
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    <p>Your browser does not support HTML5 video. <a href="movie.mp4">Download video</a>.</p>
</video>
```

---

## 🔑 2. Critical Attributes Breakdown

1. **Multiple `<source>` Tags**:
   - Alag-alag browsers (Safari, Chrome, Firefox) alag-alag video codecs optimize karte hain. Multiple sources provide karne se browser best supported format (MP4 / WebM) choose karta hai.
2. **`poster="..."`**:
   - Video start hone se pehle customized image display karta hai.
3. **`playsinline`**:
   - iOS (iPhone) Safari me video ko automatic full-screen modal me open karne ke badle webpage ke andar inline play hone deta hai.
4. **`preload="metadata"`**:
   - Performance boost: Sirf video duration aur basic dimensions download karta hai, full video download ko user ke play karne tak hold rakhta hai.
