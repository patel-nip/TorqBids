# TorqBids Landing Page

Clean, lightweight single-page landing page built with pure HTML5, CSS3, and minimal vanilla JavaScript.

## 📁 File Structure

```
torqbids-landing/
├── index.html          # Main HTML file
├── style.css           # Standalone CSS file
├── assets/             # Assets folder
│   └── logo.png        # TorqBids logo (you provide)
└── README.md           # This file
```

## 🚀 Setup Instructions

### 1. Create Project Folder
```bash
mkdir torqbids-landing
cd torqbids-landing
```

### 2. Add Files
- Copy `index.html` to root
- Copy `style.css` to root
- Create `assets` folder
- Add your logo to `assets/logo.png`

### 3. Configure Form Submission (Formspree)

**Steps:**
1. Go to https://formspree.io/
2. Sign up for free account
3. Create new form
4. Copy your form endpoint (looks like `https://formspree.io/f/xyzabc123`)
5. In `index.html`, replace `YOUR_FORM_ID` on line 70:
   ```html
   <form id="earlyAccessForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

**Alternative Options:**
- **Getform**: https://getform.io/ (similar setup)
- **Netlify Forms**: If hosting on Netlify, add `netlify` attribute to form tag

### 4. Prepare Logo
- Convert your logo to PNG format (SVG also works)
- Recommended size: 400x400px or similar
- Optimize with TinyPNG or similar tool
- Save as `assets/logo.png`

### 5. Test Locally
Open `index.html` in browser or use local server:
```bash
# Python 3
python -m http.server 8000

# Node.js (http-server)
npx http-server
```

Visit: `http://localhost:8000`

## 📊 Performance Checklist

### Before Deployment:
- [ ] Replace `YOUR_FORM_ID` with actual Formspree endpoint
- [ ] Add optimized logo to `assets/` folder
- [ ] Test form submission
- [ ] Test on mobile devices (320px minimum)
- [ ] Verify smooth scroll works
- [ ] Check Lighthouse scores (Target: 90+)

### Lighthouse Testing:
1. Open in Chrome
2. Right-click → Inspect → Lighthouse tab
3. Run audit for Mobile & Desktop
4. Target scores: Performance 90+, Accessibility 95+

## 🎨 Customization Guide

### Colors
Edit CSS variables in `style.css` (lines 8-16):
```css
--color-background: #0d0d0d;      /* Main background */
--color-primary: #00d4ff;          /* Electric blue accent */
--color-primary-hover: #00b8e6;    /* Button hover */
```

### Typography
Currently using Google Fonts (Inter). To change:
1. Update Google Fonts link in `index.html`
2. Update `--font-family` in `style.css`

### Content
Edit text directly in `index.html`:
- **Hero**: Lines 20-25
- **How It Works**: Lines 31-54
- **Trust Section**: Lines 61-79
- **Footer**: Lines 96-107

## 🌐 Deployment Options

### Netlify (Recommended)
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod
```

### Vercel
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

### Traditional Hosting (cPanel/FTP)
1. Upload all files maintaining folder structure
2. Ensure `assets/` folder uploads correctly
3. Test form submission after deployment

## ✅ Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile: iOS Safari 14+, Chrome Android 90+

## 📱 Responsive Breakpoints
- **Widescreen**: 1200px+
- **Desktop**: 769px - 1199px
- **Tablet**: 481px - 768px
- **Mobile**: 320px - 480px

## 🔒 Spam Protection
Built-in honeypot field prevents basic spam bots. Formspree provides additional spam filtering.

## 📝 Notes
- No external dependencies except Google Fonts
- Total file size: ~15KB (HTML + CSS)
- No jQuery, Bootstrap, or other frameworks
- Pure vanilla JavaScript for smooth scroll and form handling
- Optimized for Lighthouse scores 90+

## 🐛 Troubleshooting

**Form not submitting:**
- Check Formspree form ID is correct
- Verify internet connection
- Check browser console for errors

**Images not loading:**
- Verify logo is in `assets/logo.png`
- Check file path capitalization (case-sensitive on servers)
- Confirm image file extension matches HTML reference

**Styles not applying:**
- Confirm `style.css` is in same folder as `index.html`
- Check for typos in file names
- Clear browser cache

## 📧 Support
For issues with Formspree: https://help.formspree.io/
For general web hosting: Contact your hosting provider

---

**Built with performance and accessibility in mind.**
**Ready for production deployment.**
