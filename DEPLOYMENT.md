# Deployment Guide

## What Has Been Done

✅ **Downloaded all static assets:**
- Main HTML pages (index, impressum, tos, privacy)
- All CSS files (Webflow styles, Slick carousel styles)
- All JavaScript files (jQuery, Webflow scripts, Slick carousel, Typer.js)
- All images (logos, service icons, hero images, etc.)
- Font files (Inter, Eina)

✅ **Converted URLs to relative paths:**
- All CSS links now point to local files
- All JavaScript files use relative paths
- All images use relative paths
- External CDN links (Google Fonts) remain as-is for performance

✅ **GitHub Pages setup:**
- Created `.nojekyll` file to disable Jekyll processing
- Created README with deployment instructions
- Created `.gitignore` for clean repository

## File Structure

```
acceltra-web2026/
├── index.html              # Homepage
├── impressum.html          # Legal/Imprint page
├── tos.html                # Terms of Service
├── privacy.html            # Privacy Policy
├── .nojekyll               # GitHub Pages config
├── .gitignore              # Git ignore rules
├── README.md               # Project documentation
├── DEPLOYMENT.md           # This file
├── css/
│   ├── webflow.shared.css  # Main Webflow styles
│   ├── slick.css           # Slick carousel styles
│   ├── slick-theme.css     # Slick carousel theme
│   └── fonts.css           # Google Fonts CSS (reference)
├── js/
│   ├── jquery.min.js       # jQuery library
│   ├── webflow.schunk.1.js # Webflow script chunk 1
│   ├── webflow.schunk.2.js # Webflow script chunk 2
│   ├── webflow.main.js     # Webflow main script
│   ├── slick.min.js        # Slick carousel
│   ├── typer.js            # Typer.js library
│   └── webfont.js          # WebFont loader
├── images/
│   ├── logo.svg            # Brand logo
│   ├── favicon.png         # Site favicon
│   ├── apple-touch-icon.png # Apple touch icon
│   ├── hero-bg.png         # Hero background
│   ├── companies-logo.svg  # Companies logo
│   ├── digital.png         # Digital Strategy icon
│   ├── agile.png           # Agile Transformation icon
│   ├── cloud.png           # Cloud icon
│   ├── devops.png          # DevOps icon
│   ├── sre.webp           # SRE icon
│   ├── sec.png            # Security icon
│   ├── software.jpeg       # Software Development icon
│   ├── data2.png          # Data Science icon
│   ├── ai2.png            # AI icon
│   ├── tech1.png          # Technology Solutions icon
│   ├── mobile.webp        # Success stories image
│   ├── rectangle-18.webp  # Background block
│   ├── world.jpg          # World image
│   ├── language-flag.png  # Language flag
│   └── linkedin-icon.png  # LinkedIn icon
└── fonts/
    ├── inter.woff2         # Inter font
    └── Eina03-SemiBold.otf # Eina font
```

## Next Steps

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit: Static website for GitHub Pages"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Select source branch (usually `main`)
   - Select folder: `/ (root)`
   - Click Save

3. **Verify Deployment:**
   - Wait a few minutes for GitHub to build
   - Visit `https://[username].github.io/[repo-name]/`
   - Check all pages load correctly
   - Verify images and styles load properly

## Notes

- **External Links:** Google Fonts are still loaded from CDN (this is fine and recommended)
- **Cookie Consent:** The cookie consent script was removed. Add it back if needed.
- **Webflow Badge:** The "Made in Webflow" badge was removed. You can add it back if desired.
- **Service Pages:** Links to `/services/*` and `/solutions/*` pages exist in navigation but those pages weren't downloaded. You may need to create them separately or remove the links.
- **Form Submission:** The contact form uses Webflow's form handler. You'll need to set up a custom form handler or use a service like Formspree for GitHub Pages.

## Troubleshooting

**Images not loading?**
- Check that all image files are in the `images/` directory
- Verify paths in HTML use `images/filename.ext` format

**Styles not applying?**
- Ensure `.nojekyll` file exists
- Check browser console for 404 errors
- Verify CSS files are in the `css/` directory

**JavaScript not working?**
- Check browser console for errors
- Verify all JS files are in the `js/` directory
- Ensure jQuery loads before other scripts

## Support

For issues or questions, check the README.md file or GitHub Pages documentation.
