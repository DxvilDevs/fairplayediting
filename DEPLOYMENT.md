# Quick Deployment Guide for GitHub Pages

## 🚀 5-Minute Setup

### Step 1: Prepare Your Content

Before uploading to GitHub, make sure you have:

- [ ] Replaced placeholder images in `assets/portfolio/` with your actual project images
- [ ] Updated project titles and descriptions in `index.html`
- [ ] Added your contact information (email, phone)
- [ ] Added your social media links
- [ ] Updated the stats numbers to reflect your actual achievements
- [ ] Logo is in place at `assets/logo.png`

### Step 2: Create GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Click the "+" icon in top right → "New repository"
3. Repository name: `fairplay-editing` (or your choice)
4. Description: "Professional video editing portfolio"
5. Public repository
6. **DO NOT** check "Initialize with README"
7. Click "Create repository"

### Step 3: Upload Files

**Option A: Drag & Drop (Easiest)**

1. On your new repository page, click "uploading an existing file"
2. Drag ALL these files and folders into the browser:
   - index.html
   - styles.css
   - script.js
   - README.md
   - DEPLOYMENT.md
   - assets/ (entire folder)
3. Scroll down and click "Commit changes"

**Option B: Command Line**

```bash
# Navigate to the portfolio folder
cd path/to/fairplay-editing-portfolio

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial portfolio website"

# Add your GitHub repository
git remote add origin https://github.com/YOUR_USERNAME/fairplay-editing.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (top menu)
3. Scroll down and click "Pages" (left sidebar)
4. Under "Source":
   - Branch: select "main"
   - Folder: select "/ (root)"
5. Click "Save"
6. Wait 1-2 minutes for the site to build

### Step 5: Visit Your Site

Your site will be live at:
```
https://YOUR_USERNAME.github.io/fairplay-editing
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## 🔄 Making Updates

After your site is live, to make changes:

1. Edit files on your computer
2. Commit and push changes:

```bash
git add .
git commit -m "Updated portfolio images"
git push
```

3. Wait 1-2 minutes for GitHub to rebuild your site
4. Refresh your browser to see changes

## 🌐 Custom Domain (Optional)

To use your own domain (e.g., fairplayediting.com):

1. Buy a domain from a registrar (Namecheap, GoDaddy, etc.)
2. In repository Settings → Pages:
   - Enter your custom domain
   - Click "Save"
3. In your domain registrar:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`
4. Wait for DNS to propagate (up to 24 hours)

Example DNS settings:
```
Type:  CNAME
Host:  www
Value: YOUR_USERNAME.github.io
```

## 📧 Contact Form Setup

To make the contact form work, use [Formspree](https://formspree.io):

1. Sign up at formspree.io (free tier available)
2. Create a new form
3. Copy your form endpoint
4. In `index.html`, find the `<form>` tag and update:

```html
<!-- Before -->
<form class="contact-form" id="contactForm">

<!-- After -->
<form 
    class="contact-form" 
    action="https://formspree.io/f/YOUR_FORM_ID" 
    method="POST">
```

5. Remove or comment out the form submission handler in `script.js`

## ✅ Pre-Launch Checklist

Before making your site public:

- [ ] All portfolio images are high quality and properly sized
- [ ] Logo displays correctly on all pages
- [ ] All links work (navigation, social media, contact)
- [ ] Contact form is connected (Formspree or similar)
- [ ] Stats numbers are accurate
- [ ] About section text is personalized
- [ ] All placeholder text has been replaced
- [ ] Tested on mobile devices
- [ ] Tested on different browsers (Chrome, Firefox, Safari)
- [ ] Meta description and title are customized
- [ ] All images have proper alt text

## 🎨 Quick Customizations

### Change Brand Colors

In `styles.css`, find the `:root` section at the top:

```css
:root {
    --primary-color: #FF0000;     /* Change this to your brand color */
    --primary-dark: #CC0000;      /* Darker version of your color */
}
```

### Add More Projects

Copy this template and paste in the portfolio section of `index.html`:

```html
<div class="portfolio-item" data-category="commercial">
    <div class="portfolio-image-wrapper">
        <img src="assets/portfolio/project-name.jpg" alt="Project Name">
        <div class="portfolio-overlay">
            <div class="portfolio-overlay-content">
                <h3 class="portfolio-title">Project Name</h3>
                <p class="portfolio-category">Commercial</p>
                <button class="view-project-btn">View Project</button>
            </div>
        </div>
    </div>
</div>
```

## 🐛 Common Issues

### Issue: Images not showing
**Solution**: 
- Check image file names match exactly (case-sensitive)
- Ensure images are in `assets/portfolio/` folder
- Verify paths start with `assets/` not `/assets/`

### Issue: Site shows 404 error
**Solution**:
- Ensure GitHub Pages is enabled in Settings
- Wait 2-3 minutes after enabling
- Check that `index.html` is in the root directory

### Issue: Mobile menu not working
**Solution**:
- Clear your browser cache
- Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)
- Check JavaScript console for errors

## 📊 Analytics (Optional)

To track visitors, add Google Analytics:

1. Create a Google Analytics account
2. Get your tracking code
3. Add before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🎯 Next Steps

After deployment:

1. Share your portfolio link on social media
2. Add it to your email signature
3. Submit to portfolio directories
4. Update LinkedIn profile with portfolio link
5. Regularly update with new projects
6. Consider adding a blog section for industry insights

## 💡 Tips for Success

- **Update regularly**: Add new projects as you complete them
- **High-quality images**: Use professional screenshots/stills
- **Fast loading**: Compress images before uploading
- **Mobile-first**: Most visitors will view on mobile
- **SEO**: Add descriptive alt text to all images
- **Backup**: Keep local copies of all files

---

Need help? Check the main README.md for detailed documentation!
