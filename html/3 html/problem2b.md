# 📄 problem2b — Dynamic Media Switching via Named `<iframe>` Targeting

Is document me pure HTML (without JavaScript) me ek single `<iframe>` target attribute ke zariye dynamic media player build karne ka concept explain kiya gaya hai.

---

## 🎯 1. The Core Pattern & Architecture

Anchor tags (`<a>`) ka `target` attribute sirf `_blank` ya `_self` tak limited nahi hota. Aap kisi `<iframe>` ko ek unique `name="..."` de sakte hain, aur anchor links me `target="iframe_name"` set karke media files ko usi iframe ke andar dynamically load karwa sakte hain!

---

## 💻 2. Implementation Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Media Player with Iframe</title>
</head>
<body>
    <!-- Audio Section with Iframe Target -->
    <h1>Audio Player Window</h1>
    <iframe src="alvida.mp3" name="audio_player" width="400" height="100" title="Audio Player"></iframe>
    
    <p><a href="audio1.mp3" target="audio_player">▶️ Play Track 1</a></p>
    <p><a href="audio2.mp3" target="audio_player">▶️ Play Track 2</a></p>
    <p><a href="audio3.mp3" target="audio_player">▶️ Play Track 3</a></p>

    <!-- Video Section with Iframe Target -->
    <h1>Video Player Window</h1>
    <iframe src="video.mp4" name="video_player" width="500" height="300" title="Video Player"></iframe>

    <p><a href="video1.mp4" target="video_player">🎬 Switch to Video 1</a></p>
    <p><a href="video2.mp4" target="video_player">🎬 Switch to Video 2</a></p>
    <p><a href="video3.mp4" target="video_player">🎬 Switch to Video 3</a></p>
</body>
</html>
```

---

## 🔑 3. How It Works
1. `<iframe>` ko `name="video_player"` assign kiya jata hai.
2. User jab `<a href="video1.mp4" target="video_player">` par click karta hai, to browser poora webpage reload nahi karta, balki targetted iframe ke `src` ko silently badal deta hai.
3. Yeh bina single line of JavaScript likhe interactive media switcher banane ka classic HTML technique hai!
