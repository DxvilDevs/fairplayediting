# Logo Selection Guide

You have several logo variations in the `assets/` folder. Here's a guide to help you choose which one to use.

## Available Logo Files

### Standard Logos (Fairplay only)
1. **FairplayBAWTransp.png** - Black & White rectangular
2. **FairplayBAWSquTransp.png** - Black & White square
3. **FairplayTransp.png** - Color rectangular  
4. **FairplayTransp__1_.png** - Color rectangular (alternate)
5. **FairplaySWTransp.png** - White on transparent rectangular
6. **FairplaySWSquTransp.png** - White on transparent square

### Editing Logos (Fairplay Editing)
1. **FairplayEditingBAWTransp.png** - Black & White rectangular ✅ **CURRENTLY IN USE**
2. **FairplayEditingBAWSquTransp.png** - Black & White square
3. **FairplayEditingTransp.png** - Color rectangular
4. **FairplayEditingSquareTransp.png** - Color square
5. **FairplayEditingSWTransp.png** - White on transparent rectangular
6. **FairplayEditingSWSquTransp.png** - White on transparent square

## Current Setup

The website currently uses: **FairplayEditingBAWTransp.png** (renamed to `logo.png`)

This was chosen because:
- ✅ Includes "Editing" text (matches your business name)
- ✅ Black & White works on dark background
- ✅ Rectangular format fits navbar well
- ✅ Professional appearance

## Recommendations by Usage

### For Navbar (Current)
**Best Choice**: FairplayEditingBAWTransp.png or FairplayEditingSWTransp.png
- Rectangular shape fits horizontal navbar
- "Editing" text reinforces brand
- Clean, professional look

### For Favicon
**Best Choice**: FairplayEditingBAWSquTransp.png or FairplayEditingSquareTransp.png
- Square format perfect for favicon
- Compact design
- Recognizable at small sizes

### For Footer
**Best Choice**: Same as navbar for consistency
- FairplayEditingBAWTransp.png

## How to Change the Logo

### Option 1: Replace the File
```bash
# Delete current logo
rm assets/logo.png

# Copy your preferred logo and rename it
cp assets/FairplayEditingSWTransp.png assets/logo.png
```

### Option 2: Update HTML Reference
In `index.html`, find both logo references and update:

```html
<!-- Navbar logo -->
<img src="assets/YOUR_CHOSEN_LOGO.png" alt="Fairplay Editing" class="logo-img">

<!-- Footer logo -->
<img src="assets/YOUR_CHOSEN_LOGO.png" alt="Fairplay Editing">
```

## Testing Your Logo

After changing the logo, check:

1. **Visibility**: Is it clearly visible on dark background?
2. **Size**: Does it look good at navbar height (40px)?
3. **Mobile**: Does it scale well on small screens?
4. **Branding**: Does it match your overall aesthetic?

## Color Scheme Considerations

### Current Website Colors
- Background: Very dark (#0A0A0A)
- Accent: Red (#FF0000)
- Text: White (#FFFFFF)

### Logo Recommendations for Dark Theme
✅ **White logos** (SW versions) - High contrast, very visible
✅ **Black & White logos** (BAW versions) - Clean, professional
⚠️ **Color logos** - Make sure red is vibrant enough

## Quick Comparison

| Logo Type | Navbar | Footer | Favicon | Social Share |
|-----------|--------|--------|---------|--------------|
| BAW Rect  | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| BAW Square| ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| SW Rect   | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| SW Square | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Color Rect| ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Color Sq  | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |

## Multiple Logo Strategy (Recommended)

Use different logos for different purposes:

```html
<!-- Navbar - Rectangular for horizontal space -->
<img src="assets/FairplayEditingSWTransp.png" alt="Fairplay Editing">

<!-- Favicon - Square for icon -->
<link rel="icon" href="assets/FairplayEditingSquareTransp.png">

<!-- Social Share - Square with color for impact -->
<meta property="og:image" content="assets/FairplayEditingSquareTransp.png">
```

## Creating Additional Sizes

If you need different sizes, you can resize using CSS:

```css
.logo-img {
    height: 40px;  /* Navbar */
}

.footer-logo img {
    height: 35px;  /* Footer */
}

/* For high-DPI displays */
@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
    .logo-img {
        height: 40px;  /* Same size but sharper */
    }
}
```

## Next Steps

1. Review all logo options
2. Choose your preferred version
3. Replace `logo.png` or update HTML references
4. Test on different devices
5. Add favicon (see DEPLOYMENT.md for instructions)

---

**Current Default**: FairplayEditingBAWTransp.png ✅
**Need Help?**: Check the main README.md for support
