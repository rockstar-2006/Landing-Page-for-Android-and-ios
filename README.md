# 🌐 Faculty Quest Landing Page

A premium, modern landing page for downloading the Faculty Quest mobile apps (Android & iOS).

## 📁 Files

- `index.html` - Main landing page with all sections
- `styles.css` - Premium styling with animations and glassmorphism
- `script.js` - Interactive features and animations
- `downloads/` - Folder for APK and app files
- `vercel.json` - Deployment configuration

## 🎨 Features

✨ **Premium Design:**
- Glassmorphism effects
- Animated gradient backgrounds
- Smooth scroll animations
- Responsive design (mobile, tablet, desktop)
- Dark theme with vibrant accents

📱 **Download Options:**
- Android APK download button
- iOS TestFlight link
- Web app launch button

🎯 **Sections:**
- Hero with animated orbs
- Features showcase (6 cards)
- Download cards (Android/iOS/Web)
- Installation guide (4 steps)
- FAQ section (6 questions)
- Call-to-action
- Professional footer

## 🚀 Quick Start

### 1. Add Your APK

After building your Android app, copy the APK here:

```bash
# Build the Android app first
cd ..
npm run build:mobile
npx cap sync android
npx cap open android
# In Android Studio: Build → Generate Signed APK

# Then copy it to landing page
cp ../android/app/build/outputs/apk/release/app-release.apk downloads/faculty-quest.apk
```

### 2. Update Links

Edit `index.html` and replace these placeholders:

- `https://your-app.vercel.app` → Your actual Vercel app URL
- `https://testflight.apple.com/join/your-code` → Your TestFlight link (if you have iOS app)

### 3. Test Locally

Open `index.html` in your browser or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve

# Then open: http://localhost:8000
```

### 4. Deploy to Vercel

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Deploy to production
vercel --prod
```

## 🎨 Customization

### Update Colors

Edit `styles.css` CSS variables (lines 8-15):

```css
:root {
    --primary: #6366f1;      /* Main brand color */
    --secondary: #8b5cf6;    /* Accent color */
    --success: #10b981;      /* Success states */
    /* ... */
}
```

### Update Content

Edit `index.html`:

- **Hero Title** (line ~60): Change the main headline
- **Hero Description** (line ~65): Update the tagline
- **Features** (lines ~100-150): Modify feature cards
- **FAQ** (lines ~250-300): Update questions and answers
- **Footer** (lines ~350-400): Add your links

### Add Images

Replace emoji icons with actual images:

1. Add images to a new `images/` folder
2. Update `<div class="logo-icon">📚</div>` with `<img src="images/logo.png">`
3. Update feature icons similarly

## 📊 SEO Optimization

The landing page includes:

- ✅ Meta tags for social sharing
- ✅ Open Graph tags (Facebook, LinkedIn)
- ✅ Twitter Card tags
- ✅ Semantic HTML structure
- ✅ Mobile-friendly viewport
- ✅ Fast loading (no external dependencies except fonts)

### Add More SEO

1. Create `sitemap.xml`:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://your-landing.vercel.app/</loc>
    <lastmod>2024-12-23</lastmod>
    <priority>1.0</priority>
  </url>
</urlset>
```

2. Create `robots.txt`:
```
User-agent: *
Allow: /
Sitemap: https://your-landing.vercel.app/sitemap.xml
```

## 📱 Mobile Responsiveness

The landing page is fully responsive:

- **Desktop** (1920x1080+): Full layout with all features
- **Laptop** (1366x768): Optimized spacing
- **Tablet** (768x1024): 2-column grid
- **Mobile** (375x667): Single column, mobile menu

## 🎯 Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🚀 Performance

- **Load Time:** < 2 seconds
- **Size:** ~50KB (HTML + CSS + JS)
- **No external dependencies** except Google Fonts
- **Optimized animations** using CSS transforms
- **Lazy loading** for scroll animations

## 📈 Analytics (Optional)

Add Google Analytics by inserting before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 🎨 Design Credits

- **Fonts:** Inter & Space Grotesk (Google Fonts)
- **Icons:** SVG (inline)
- **Colors:** Custom gradient palette
- **Animations:** CSS transforms & keyframes

## 📝 Checklist

Before deploying:

- [ ] APK file added to `downloads/` folder
- [ ] All URLs updated (Vercel app, TestFlight)
- [ ] Colors customized (optional)
- [ ] Content updated (hero, features, FAQ)
- [ ] Tested on mobile device
- [ ] SEO meta tags updated
- [ ] Analytics added (optional)

## 🆘 Troubleshooting

**APK download not working:**
- Ensure APK is in `downloads/faculty-quest.apk`
- Check file permissions
- Verify file size is correct

**Animations not smooth:**
- Check browser supports CSS transforms
- Reduce animation complexity on low-end devices
- Disable animations with `prefers-reduced-motion`

**Mobile menu not opening:**
- Check JavaScript console for errors
- Ensure `script.js` is loaded
- Verify mobile menu button ID matches

## 🎉 You're Done!

Your premium landing page is ready! Deploy it and share the link with your students.

**Example URL:** `https://faculty-quest.vercel.app`

---

**Need help?** Check the main project's `LANDING_PAGE_GUIDE.md` for detailed instructions.
