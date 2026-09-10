# 📄 3towatch — Search Engine Optimization & Google Core Web Vitals

Is document me SEO ke fundamental rules, Google Core Web Vitals performance metrics (CLS, LCP, FID/INP), Chrome DevTools Lighthouse audit aur Mobile emulation ke concepts explain kiye gaye hain.

---

## 🎯 1. SEO (Search Engine Optimization) Fundamentals

- **Definition**: Google aur search engines chahte hain ki wo users ko fast-loading, highly-relevant aur smooth user-experience wale pages recommend karein.
- **Key Ranking Factors**:
  1. Semantic, clean HTML structure.
  2. Mobile responsiveness.
  3. Fast loading speed and user interaction smoothness (Core Web Vitals).

---

## ⚡ 2. Google Core Web Vitals Deep Dive

### 1. CLS (Cumulative Layout Shift) — Visual Stability
- **Meaning**: Page load hone ke dauran screen ke content elements kitna hilte/jump karte hain.
- **Problem**: User kisi button par click karne ja raha tha, achanak ek slow-loading banner load hua aur button neeche khisak gaya (accidental wrong click).
- **Solution**: Sabhi images aur videos par explicit `width` aur `height` attributes assign karein taaki browser unka placeholder space pehle se reserve kar le.
- **Target**: CLS score **< 0.1** hona chahiye.

### 2. LCP (Largest Contentful Paint) — Loading Performance
- **Meaning**: Webpage ka sabse bada visual element (e.g. hero image banner, primary heading, large block of text) screen par render hone me kitna time leta hai.
- **Target**: **< 2.5 seconds** (2.5 sec ke andar user ko main content dikh jana chahiye).

### 3. FID / INP (First Input Delay / Interaction to Next Paint) — Responsiveness
- **Meaning**: User ke pehle interaction (e.g. button click, dropdown select, link press) aur browser ke us par actual action perform karne ke beech ka delay.
- **Target**: **< 100 milliseconds**.

---

## 🛠️ 3. Chrome DevTools Audit & Testing Tools

### 1. Lighthouse Audit
- **Steps**: Webpage par `Right Click -> Inspect -> Lighthouse Tab -> Analyze Page Load`.
- **Outputs**: Performance score, Accessibility score, Best Practices aur SEO metrics ka detailed diagnostic report.

### 2. Mobile Device Emulation
- **Shortcut**: `Ctrl + Shift + M` (Windows) / `Cmd + Shift + M` (Mac).
- **Function**: Webpage ko alag-alag screen resolutions (iPhone, Pixel, iPad, Custom) par test karne ke liye browser viewport emulate karta hai.
