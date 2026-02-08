# Fairplay Editing - Portfolio Website

A modern, sleek portfolio website for Fairplay Editing, showcasing video editing work with smooth animations, abstract design elements, and professional layouts.

## 🎬 Features

- **Modern Design**: Sleek, dark theme with red accent colors matching your brand
- **Smooth Animations**: Scroll-triggered animations and interactive hover effects
- **Abstract Elements**: Dynamic background shapes and visual effects
- **Portfolio Filtering**: Filter projects by category (Commercial, Narrative, Documentary, Music Videos)
- **Responsive Design**: Fully responsive across all devices
- **Project Modals**: Detailed project view in elegant modals
- **Contact Form**: Ready-to-integrate contact form
- **SEO Optimized**: Proper meta tags and semantic HTML
- **No Backend Required**: Fully static, perfect for GitHub Pages

## 📁 File Structure

```
fairplay-editing-portfolio/
├── index.html          # Main HTML file
├── styles.css          # All styles and animations
├── script.js           # Interactive functionality
├── README.md           # This file
└── assets/
    ├── logo.png        # Your logo (add your logo here)
    └── portfolio/      # Portfolio images folder
        ├── placeholder-1.jpg
        ├── placeholder-2.jpg
        └── ... (add your project images)
```

## 🚀 Quick Start

### 1. Set Up Your Repository

```bash
# Clone or download this repository
git clone https://github.com/yourusername/fairplay-editing-portfolio.git
cd fairplay-editing-portfolio

# Create assets directory
mkdir -p assets/portfolio
```

### 2. Add Your Logo

1. Choose one of your logo files (recommend `FairplayEditingBAWTransp.png` for the navbar)
2. Rename it to `logo.png`
3. Place it in the `assets/` folder

### 3. Add Your Portfolio Images

1. Add your project images to `assets/portfolio/`
2. Update the image paths in `index.html`:
   - Find all instances of `placeholder-1.jpg`, `placeholder-2.jpg`, etc.
   - Replace with your actual image filenames

Example:
```html
<!-- Before -->
<img src="assets/portfolio/placeholder-1.jpg" alt="Project 1">

<!-- After -->
<img src="assets/portfolio/my-awesome-project.jpg" alt="Brand Campaign">
```

### 4. Customize Content

#### Update Project Information
Edit the portfolio items in `index.html`:

```html
<div class="portfolio-item" data-category="commercial">
    <div class="portfolio-image-wrapper">
        <img src="assets/portfolio/your-image.jpg" alt="Your Project">
        <div class="portfolio-overlay">
            <div class="portfolio-overlay-content">
                <h3 class="portfolio-title">Your Project Title</h3>
                <p class="portfolio-category">Commercial</p>
                <button class="view-project-btn">View Project</button>
            </div>
        </div>
    </div>
</div>
```

#### Update Stats
Edit the stats in the stats section:

```html
<div class="stat-number" data-target="150">0</div>
<div class="stat-label">Projects Completed</div>
```

#### Update Contact Information
Edit your contact details:

```html
<a href="mailto:your-email@fairplayediting.com">your-email@fairplayediting.com</a>
<a href="tel:+1234567890">+1 (234) 567-890</a>
```

#### Update Social Links
Add your actual social media URLs:

```html
<a href="https://instagram.com/yourhandle" class="social-link">
<a href="https://youtube.com/yourchannel" class="social-link">
```

## 📤 Deploy to GitHub Pages

### Method 1: Through GitHub Website

1. **Create a new repository** on GitHub
   - Name it: `fairplay-editing-portfolio` (or any name you prefer)
   - Make it public
   - Don't initialize with README

2. **Upload your files**
   - Click "uploading an existing file"
   - Drag and drop all files (index.html, styles.css, script.js, assets folder)
   - Commit changes

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Source", select "main" branch
   - Click Save
   - Your site will be live at: `https://yourusername.github.io/fairplay-editing-portfolio`

### Method 2: Using Git Command Line

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit - Fairplay Editing Portfolio"

# Add GitHub repository as remote
git remote add origin https://github.com/yourusername/fairplay-editing-portfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in repository settings as described in Method 1.

## 🎨 Customization Guide

### Change Color Scheme

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #FF0000;        /* Main brand color */
    --primary-dark: #CC0000;         /* Darker shade */
    --bg-dark: #0A0A0A;              /* Dark background */
    --bg-darker: #050505;            /* Darker background */
    --bg-card: #111111;              /* Card background */
}
```

### Add More Portfolio Items

Copy and paste this template in the portfolio grid:

```html
<div class="portfolio-item" data-category="your-category">
    <div class="portfolio-image-wrapper">
        <img src="assets/portfolio/your-image.jpg" alt="Project Name">
        <div class="portfolio-overlay">
            <div class="portfolio-overlay-content">
                <h3 class="portfolio-title">Project Name</h3>
                <p class="portfolio-category">Category</p>
                <button class="view-project-btn">View Project</button>
            </div>
        </div>
    </div>
</div>
```

### Add New Filter Categories

1. Add a new filter button:
```html
<button class="filter-btn" data-filter="yourcategory">Your Category</button>
```

2. Update portfolio items with the new category:
```html
<div class="portfolio-item" data-category="yourcategory">
```

## 📧 Contact Form Integration

The contact form is currently set up for demonstration. To make it functional, integrate with one of these services:

### Option 1: Formspree (Easiest)

1. Sign up at [Formspree.io](https://formspree.io/)
2. Update the form in `index.html`:
```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: EmailJS

1. Sign up at [EmailJS.com](https://www.emailjs.com/)
2. Follow their integration guide
3. Update the form handler in `script.js`

### Option 3: Netlify Forms

If deploying to Netlify instead of GitHub Pages:

1. Add `netlify` attribute to form:
```html
<form class="contact-form" name="contact" method="POST" data-netlify="true">
```

## 🎥 Adding Video Embeds

To add video previews instead of images:

```html
<div class="portfolio-item" data-category="commercial">
    <div class="portfolio-image-wrapper">
        <iframe 
            src="https://www.youtube.com/embed/VIDEO_ID" 
            frameborder="0" 
            allowfullscreen>
        </iframe>
    </div>
</div>
```

## 📱 Testing Locally

Simply open `index.html` in your browser to test locally. For a better development experience:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (install live-server first: npm install -g live-server)
live-server
```

Then visit `http://localhost:8000` in your browser.

## 🔧 Troubleshooting

### Images Not Showing

1. Check file paths are correct
2. Ensure images are in the `assets/portfolio/` folder
3. Verify image file names match exactly (case-sensitive)

### Logo Not Appearing

1. Make sure logo file is named exactly `logo.png`
2. Place it in the `assets/` folder
3. Check file path in HTML: `<img src="assets/logo.png">`

### Portfolio Filter Not Working

1. Ensure each portfolio item has a `data-category` attribute
2. Filter button `data-filter` must match portfolio item categories
3. Check JavaScript console for errors

## 📊 Performance Tips

1. **Optimize Images**: Compress images before uploading (use TinyPNG or similar)
2. **Use WebP Format**: Convert images to WebP for better compression
3. **Lazy Loading**: Images lazy load automatically via Intersection Observer
4. **Minify Assets**: Before deploying, consider minifying CSS and JS

## 🎯 SEO Optimization

The site includes:
- Semantic HTML5 elements
- Meta description
- Open Graph tags (add your own)
- Alt text for images
- Proper heading hierarchy

To improve further, add to `<head>`:

```html
<!-- Open Graph / Facebook -->
<meta property="og:title" content="Fairplay Editing | Professional Video Editing">
<meta property="og:description" content="Your description here">
<meta property="og:image" content="https://yoursite.com/assets/og-image.jpg">

<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Fairplay Editing">
<meta name="twitter:description" content="Your description here">
```

## 📝 License

© 2024 Fairplay Editing. All rights reserved.

## 🤝 Support

For questions or issues, please open an issue on GitHub or contact via the website's contact form.

---

**Built with ❤️ for Fairplay Editing**
