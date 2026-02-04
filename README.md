# Acceltra Website

This repository contains the static website for Acceltra, ready to be hosted on GitHub Pages.

## Structure

```
.
├── index.html          # Main homepage
├── impressum.html      # Imprint/Legal page
├── tos.html           # Terms of Service
├── privacy.html       # Privacy Policy
├── css/               # Stylesheets
├── js/                # JavaScript files
├── images/            # Image assets
├── fonts/             # Font files
└── .nojekyll          # GitHub Pages configuration
```

## Deployment to GitHub Pages

### Option 1: Automatic Deployment (Recommended)

1. Push this repository to GitHub
2. Go to your repository settings
3. Navigate to "Pages" in the left sidebar
4. Under "Source", select the branch (usually `main` or `master`)
5. Select the folder (usually `/ (root)`)
6. Click "Save"
7. Your site will be available at `https://[username].github.io/[repository-name]/`

### Option 2: Using GitHub Actions

If you want to use GitHub Actions for deployment, you can set up a workflow file in `.github/workflows/deploy.yml`.

## Local Development

To view the website locally:

1. Clone this repository
2. Open `index.html` in a web browser, or
3. Use a local server:
   ```bash
   # Using Python 3
   python3 -m http.server 8000
   
   # Using Node.js (if you have http-server installed)
   npx http-server
   ```
4. Navigate to `http://localhost:8000` in your browser

## Notes

- All external URLs have been converted to relative paths for GitHub Pages compatibility
- The website uses Webflow-generated HTML/CSS/JS
- Images and assets are stored locally in the repository
- External fonts (Google Fonts) are loaded from CDN
- The cookie consent script has been removed (you can add it back if needed)

## Customization

- To update content, edit the HTML files directly
- To modify styles, edit files in the `css/` directory
- To change functionality, edit files in the `js/` directory
- Images can be replaced in the `images/` directory

## License

Copyright © Acceltra. All rights reserved.
