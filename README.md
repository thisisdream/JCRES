# Jones and Company Real Estate Website

A professional, SEO-optimized static website for Jones and Company Real Estate, a premier Silicon Valley real estate brokerage.

## 🚀 Quick Start

### File Structure
```
jones-realestate/
├── index.html          # Home page
├── about.html          # About Us page
├── style.css           # All styles
├── script.js           # JavaScript functionality
├── README.md           # This file
└── images/             # Image folder (create this)
    └── og-image.jpg    # Social media preview image
```

## 📦 GitHub Pages Deployment

### Step 1: Create Repository
1. Go to GitHub.com and create a new repository
2. Name it `jones-realestate` (or your preferred name)
3. Make it public
4. Don't initialize with README (we have our own files)

### Step 2: Upload Files
```bash
# Initialize git in your project folder
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit - Jones and Company Real Estate website"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR-USERNAME/jones-realestate.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings**
3. Scroll to **Pages** section (left sidebar)
4. Under "Source", select **main** branch
5. Click **Save**
6. Your site will be live at: `https://YOUR-USERNAME.github.io/jones-realestate/`

### Step 4: Update URLs in Code
After deployment, update these URLs in `index.html`:
- Line 11: `<meta property="og:url" content="https://YOUR-USERNAME.github.io/jones-realestate">`
- Line 12: `<meta property="og:image" content="https://YOUR-USERNAME.github.io/jones-realestate/images/og-image.jpg">`
- Line 13: `<link rel="canonical" href="https://YOUR-USERNAME.github.io/jones-realestate">`

## 🖼️ Adding Your Images

### Required Images
1. **Hero Background** - Replace placeholder at line 107 in `index.html`
2. **Linda Garcia Photo** - Add to `images/` folder and update `about.html` line 291
3. **Social Media Preview** - Create `og-image.jpg` (1200x630px recommended)

### Recommended Image Structure
```
images/
├── og-image.jpg              # Social sharing image
├── linda-garcia.jpg          # Broker photo
├── hero-background.jpg       # Optional: custom hero image
└── favicon.png              # Website icon
```

### Adding Images
```bash
# Create images folder
mkdir images

# Add your images to this folder
# Then commit and push
git add images/
git commit -m "Add website images"
git push
```

## 🎨 Customization

### Brand Colors
The website uses your brand colors:
- Primary: `#8B1A1E` (Deep Red)
- Secondary: `#D4C4A3` (Gold/Beige)

To change colors, update the CSS variables in `style.css`:
```css
:root {
    --primary-color: #8B1A1E;
    --secondary-color: #D4C4A3;
    /* ... other variables */
}
```

### Content Updates

#### Homepage (`index.html`)
- **Mission Statement** - Line 113
- **Services** - Lines 128-186
- **Differentiators** - Lines 200-225
- **Promise** - Lines 238-245

#### About Page (`about.html`)
- **Linda's Bio** - Lines 294-309
- **Credentials** - Lines 311-321
- **Company Story** - Lines 356-371

### Adding a Favicon
1. Create a 32x32px or 512x512px PNG/ICO file
2. Add to root folder as `favicon.ico`
3. Add this line to `<head>` in both HTML files:
```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

## 🔍 SEO Optimization Features

### Built-in SEO Features
✅ Semantic HTML5 structure  
✅ Meta descriptions and keywords  
✅ Open Graph tags for social sharing  
✅ Canonical URLs  
✅ Descriptive alt text on images  
✅ Proper heading hierarchy (H1 → H6)  
✅ Mobile-responsive design  
✅ Fast loading times  
✅ Schema markup ready  

### Google Search Console Setup
1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add your property: `https://YOUR-USERNAME.github.io/jones-realestate/`
3. Verify ownership (HTML tag method recommended)
4. Submit sitemap (see below)

### Creating a Sitemap
Create `sitemap.xml` in root folder:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://YOUR-USERNAME.github.io/jones-realestate/</loc>
    <lastmod>2025-09-30</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://YOUR-USERNAME.github.io/jones-realestate/about.html</loc>
    <lastmod>2025-09-30</lastmod>
    <priority>0.8</priority>
  </url>
</urlset>
```

### Adding Schema Markup
Add to `<head>` section for better search results:
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "RealEstateAgent",
  "name": "Jones and Company Real Estate",
  "description": "Premier Silicon Valley real estate brokerage",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Silicon Valley",
    "addressRegion": "CA",
    "addressCountry": "US"
  },
  "email": "lindavon@msn.com",
  "areaServed": "Silicon Valley, California"
}
</script>
```

## 📱 Features

### Responsive Design
- Mobile-first approach
- Breakpoints at 640px, 968px
- Touch-friendly navigation
- Optimized images for all devices

### Interactive Elements
- Smooth scrolling navigation
- Mobile hamburger menu
- Animated scroll effects
- Hover interactions on cards
- Parallax background effects
- Scroll-to-top button
- Form validation

### Contact Form
- Opens user's default email client
- Pre-fills subject and body
- Form validation
- Success/error messaging

## 🔧 Advanced Customization

### Adding Google Analytics
Add before closing `</head>` tag:
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Custom Domain
1. Buy domain from registrar (GoDaddy, Namecheap, etc.)
2. Create `CNAME` file in root with your domain:
   ```
   www.jonesandcompanyrealestate.com
   ```
3. Update DNS records at your registrar:
   - Type: CNAME
   - Host: www
   - Value: YOUR-USERNAME.github.io
4. Enable HTTPS in GitHub Pages settings

### Adding More Pages
1. Create new HTML file (e.g., `listings.html`)
2. Copy header and footer from existing pages
3. Add navigation link in all pages
4. Update sitemap.xml

## 📊 Performance Optimization

### Current Optimizations
- Minified external resources
- Font preloading
- CSS/JS defer loading
- Optimized images
- Lazy loading ready

### Further Improvements
1. **Compress Images**: Use TinyPNG or ImageOptim
2. **Enable Caching**: GitHub Pages does this automatically
3. **CDN**: GitHub Pages uses Fastly CDN by default
4. **Minify Code**: Use tools like UglifyJS (optional)

## 🐛 Troubleshooting

### Site Not Loading
- Wait 10-15 minutes after enabling GitHub Pages
- Check that main branch is selected in Settings
- Verify index.html is in root folder

### Images Not Showing
- Check file paths are correct
- Ensure images are committed and pushed
- Verify image URLs start with `images/`

### Form Not Working
- Ensure user has default email client configured
- Test mailto: links directly in browser
- Check browser console for JavaScript errors

## 📞 Support

For issues with:
- **GitHub Pages**: [GitHub Pages Documentation](https://docs.github.com/en/pages)
- **Domain Setup**: [Custom Domain Guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- **SEO**: [Google Search Central](https://developers.google.com/search)

## 📝 License & Credits

- Font: [Google Fonts](https://fonts.google.com) (Playfair Display, Inter)
- Images: [Unsplash](https://unsplash.com) (placeholders)
- Icons: Custom SVG icons
- Framework: Vanilla HTML/CSS/JavaScript

---

**Built for Jones and Company Real Estate**  
Silicon Valley, California  
© 2025 All Rights Reserved