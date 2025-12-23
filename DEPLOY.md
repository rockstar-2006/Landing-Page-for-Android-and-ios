# 🚀 Landing Page - Quick Deploy Guide

## ✅ What You Have

A complete, premium landing page with:
- ✨ Modern design with animations
- 📱 Download buttons for Android, iOS, and Web
- 🎨 Glassmorphism effects
- 📊 Features showcase
- ❓ FAQ section
- 📱 Fully responsive

## 📋 Before Deploying

### 1. Add Your APK File

```bash
# First, build your Android app
cd ..  # Go back to Quiz folder
npm run build:mobile
npx cap sync android
npx cap open android

# In Android Studio:
# Build → Generate Signed Bundle/APK → APK
# Choose release build
# Sign with your keystore

# Copy the APK to landing page
cp android/app/build/outputs/apk/release/app-release.apk landing-page/downloads/faculty-quest.apk
```

### 2. Update URLs in index.html

Open `index.html` and replace:

**Line ~40:** Web app URL
```html
<a href="https://your-app.vercel.app" class="btn-primary-small">Launch Web App</a>
```
Replace `https://your-app.vercel.app` with your actual Vercel URL

**Line ~75:** Web app button
```html
<a href="https://your-app.vercel.app" class="btn-secondary">
```

**Line ~230:** iOS TestFlight link
```html
<a href="https://testflight.apple.com/join/your-code" class="btn-download">
```

**Line ~250:** Web app download
```html
<a href="https://your-app.vercel.app" class="btn-download">
```

**Multiple locations:** Search for `https://your-app.vercel.app` and replace all

## 🚀 Deploy to Vercel

### Option 1: Vercel CLI (Recommended)

```bash
# Install Vercel CLI globally
npm install -g vercel

# Navigate to landing page folder
cd landing-page

# Login to Vercel
vercel login

# Deploy (first time)
vercel

# Answer the prompts:
# - Set up and deploy? Yes
# - Which scope? Your account
# - Link to existing project? No
# - Project name: faculty-quest-landing
# - Directory: ./
# - Override settings? No

# Deploy to production
vercel --prod
```

### Option 2: Vercel Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Click "Add New Project"
3. Import your GitHub repository
4. Set **Root Directory** to `landing-page`
5. Click "Deploy"

## 🎯 After Deployment

### 1. Test Everything

Visit your landing page URL and check:

- [ ] Page loads correctly
- [ ] All sections visible
- [ ] Mobile menu works
- [ ] Smooth scrolling works
- [ ] Download buttons work
- [ ] APK downloads correctly
- [ ] Links to web app work
- [ ] Responsive on mobile

### 2. Update Main App

Add a link to your landing page in the main Faculty Quest app:

```tsx
// In your main app's navigation or footer
<a href="https://faculty-quest-landing.vercel.app" target="_blank">
  Download Mobile App
</a>
```

### 3. Share the Link

Your landing page URL will be something like:
- `https://faculty-quest-landing.vercel.app`
- Or with custom domain: `https://download.facultyquest.com`

## 🎨 Customization (Optional)

### Change Colors

Edit `styles.css` (lines 8-15):

```css
:root {
    --primary: #6366f1;      /* Your brand color */
    --secondary: #8b5cf6;    /* Accent color */
    /* ... */
}
```

### Add Your Logo

Replace the emoji logo (📚) with an image:

```html
<!-- Replace this: -->
<div class="logo-icon">📚</div>

<!-- With this: -->
<img src="images/logo.png" alt="Faculty Quest" width="40" height="40">
```

### Update Content

Edit `index.html`:
- Hero title and description
- Feature cards
- FAQ questions
- Footer links

## 📊 Add Analytics (Optional)

Add Google Analytics before `</head>` in `index.html`:

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

## 🌐 Custom Domain (Optional)

### Add Custom Domain to Vercel

1. Go to your project on Vercel
2. Settings → Domains
3. Add domain (e.g., `download.facultyquest.com`)
4. Follow DNS configuration instructions
5. Wait for DNS propagation (5-30 minutes)

### Recommended Domain Names

- `download.facultyquest.com`
- `app.facultyquest.com`
- `get.facultyquest.com`
- `mobile.facultyquest.com`

## 📱 QR Code for Easy Sharing

Generate a QR code pointing to your landing page:

1. Go to [qr-code-generator.com](https://www.qr-code-generator.com/)
2. Enter your landing page URL
3. Download the QR code
4. Add to presentations, posters, etc.

## 🎉 You're Live!

Your landing page is now deployed and students can download your app!

**Next Steps:**
1. Share the landing page URL with students
2. Add the link to your main app
3. Monitor downloads and feedback
4. Update the APK when you release new versions

---

## 📁 File Structure

```
landing-page/
├── index.html          ✅ Main page
├── styles.css          ✅ Styling
├── script.js           ✅ Interactivity
├── vercel.json         ✅ Deployment config
├── downloads/
│   ├── faculty-quest.apk  ⚠️ Add this!
│   └── README.md
├── README.md
└── DEPLOY.md (this file)
```

## 🆘 Troubleshooting

**APK not downloading:**
- Check file exists in `downloads/faculty-quest.apk`
- Verify file permissions
- Check browser console for errors

**Page not loading:**
- Check Vercel deployment logs
- Verify all files are uploaded
- Check for JavaScript errors

**Mobile menu not working:**
- Clear browser cache
- Check JavaScript console
- Verify `script.js` is loaded

**Links not working:**
- Verify you updated all URLs
- Check for typos in links
- Test in different browsers

---

## 📞 Support

- Main Project Docs: `../DEPLOYMENT_GUIDE.md`
- Landing Page Guide: `../LANDING_PAGE_GUIDE.md`
- Vercel Docs: https://vercel.com/docs

**Deployment Time:** ~5 minutes  
**Status:** ✅ Ready to Deploy!
