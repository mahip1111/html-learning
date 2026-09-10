# 📄 problem2 — Multi-Asset Media Showcase (Audio, Video & Images)

Is document me multiple multimedia files (4 videos, 5 audios aur 2 images) ko HTML5 me modularly showcase karne ka practical approach explain kiya gaya hai.

---

## 🎯 1. Problem Statement
> **Challenge**: 12 multimedia files (4 videos, 5 audios aur 2 images) ko include karte huye ek structured HTML media gallery webpage design karein.

---

## 💻 2. Implementation Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multimedia Gallery</title>
</head>
<body>
    <h1>Audio Files</h1>
    <div><audio src="alvida.mp3" muted loop controls preload="auto"></audio></div>
    <div><audio src="audio1.mp3" muted loop controls preload="auto"></audio></div>
    <div><audio src="audio2.mp3" muted loop controls preload="auto"></audio></div>
    <div><audio src="audio3.mp3" muted loop controls preload="auto"></audio></div>
    <div><audio src="audio4.mp3" muted loop controls preload="auto"></audio></div>

    <h1>Video Files</h1>
    <div><video src="video.mp4" controls loop muted poster="nature.jpg" width="400" height="300"></video></div>
    <div><video src="video1.mp4" controls loop muted poster="nature.jpg" width="400" height="300"></video></div>
    <div><video src="video2.mp4" controls loop muted poster="nature.jpg" width="400" height="300"></video></div>
    <div><video src="video3.mp4" controls loop muted poster="nature.jpg" width="400" height="300"></video></div>

    <h1>Image Files</h1>
    <div><img src="img.jpg" alt="Gallery Image 1" width="400"></div>
    <div><img src="nature.jpg" alt="Nature Image 2" width="400"></div>
</body>
</html>
```

---

## 🔑 3. Key Takeaways
- Audio aur Video elements by default inline hote hain; unhe `<div>` containers me wrap karne se vertical layout ban jata hai.
- Video tags par `poster` lagane se video load hone se pehle blank screen ke badle preview thumbnail show hota hai.
