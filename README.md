# SANVIA Website

A professional website for SANVIA LLC - an intellectual property holding company specializing in antimicrobial technologies and advanced material processing innovations.

## Quick Deploy to Render

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

## Manual Deployment Steps

1. **Connect Repository to Render**
   - Go to [Render Dashboard](https://dashboard.render.com)
   - Click "New +" → "Static Site"
   - Connect your GitHub repository
   - Select this repository

2. **Configure Build Settings**
   - **Build Command:** Leave empty (no build process needed)
   - **Publish Directory:** `.` (root directory)
   - **Auto Deploy:** Yes (recommended)

3. **Environment Variables**
   - No environment variables needed for static site

## Project Structure

```
├── index.html              # Main website file
├── css/
│   └── style.css          # Responsive styling
├── js/
│   └── script.js          # Interactive functionality
├── assets/
│   ├── sanvia-logo.svg    # Main logo
│   ├── sanvia-logo-white.svg # Footer logo
│   └── hero-antimicrobial-tech.svg # Hero background
├── .github/
│   └── copilot-instructions.md
├── render.yaml            # Render configuration
└── README.md              # This file
```

## About SANVIA

SANVIA is founded by Dr. Chad Roy and Dr. Joe Buell, with a comprehensive patent portfolio covering:

- **EQ12™ Quaternary Chemistry** - Advanced antimicrobial compounds
- **Supercritical CO₂ Integration** - Revolutionary material processing methods  
- **Manufacturing Technologies** - Specialized implementations for filtration media and textiles
- **Processing Methods** - Proprietary antimicrobial agent incorporation techniques

## Patent Portfolio

- **5 Patent Families** (0001-0005)
- **Global Scope** (US + PCT)
- **Portfolio Life** through 2039-2045
- **Core Technology** EQ12™ platform

## Features

- **Zero Build Process**: Pure HTML/CSS/JavaScript - perfect for Render static sites
- **Responsive Design**: Mobile-first approach with responsive layouts
- **Modern UI/UX**: Clean, professional design inspired by Dyna.co
- **Interactive Elements**: Smooth scrolling, hover effects, and form handling
- **Optimized Assets**: SVG graphics for fast loading and crisp display
- **SEO Ready**: Semantic HTML structure with proper meta tags
- **Accessibility**: ARIA labels and keyboard navigation support
- **Performance Optimized**: Minified and optimized for production

## Sections

1. **Hero Section**: Main introduction with company mission
2. **Industries**: Target markets and applications
3. **Technology**: EQ12 platform features and benefits
4. **Team**: Careers and company background
5. **Contact**: Lead generation form and newsletter signup
6. **Footer**: Navigation and social links

## Deployment

## Deployment to Render

### Option 1: Direct GitHub Connection
1. Push your code to GitHub
2. Go to [Render Dashboard](https://dashboard.render.com)
3. Click "New +" → "Static Site"
4. Connect your GitHub repository
5. Configure:
   - **Build Command:** Leave empty
   - **Publish Directory:** `.`
   - **Auto Deploy:** Enable

### Option 2: Manual Upload
1. Download/zip your project files
2. In Render Dashboard, create new Static Site
3. Upload zip file directly

### Custom Domain Setup (sanvia.co)
1. In Render Dashboard, go to your site settings
2. Add custom domain: `sanvia.co` and `www.sanvia.co`
3. Update GoDaddy DNS records:
   - **CNAME**: www → your-render-site.onrender.com
   - **A Record**: @ → Render's IP (provided in dashboard)

## Customization

### Content Updates
- Update company information in `index.html`
- Modify styling in `css/style.css`
- Add custom functionality in `js/script.js`

### Images
Replace placeholder images in the `assets/` directory:
- `sanvia-logo.png` - Main logo
- `sanvia-logo-white.png` - White logo for footer
- `hero-placeholder.jpg` - Hero section image
- Industry and technology icons
- Team/company logos

### Colors and Branding
Primary colors used:
- Primary Blue: `#007bff`
- Success Green: `#28a745`
- Danger Red: `#dc3545`
- Dark: `#1a1a1a`
- Light Gray: `#f8f9fa`

### Forms
- Contact form and newsletter signup are currently frontend-only
- Add backend integration for form processing
- Consider services like Formspree, Netlify Forms, or custom API

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- iOS Safari
- Chrome for Android

## Performance

- Optimized images (replace placeholders with properly compressed images)
- Minified CSS and JavaScript for production
- Lazy loading for images
- CDN integration for better global performance

## SEO Considerations

- Add proper meta descriptions
- Include Open Graph tags for social sharing
- Implement structured data (JSON-LD)
- Add sitemap.xml and robots.txt
- Optimize images with alt tags

## Next Steps

1. **Replace Placeholder Images**: Add actual Sanvia branding and product images
2. **Content Review**: Review and refine all copy to match Sanvia's messaging
3. **Form Integration**: Connect forms to email marketing and CRM systems
4. **Analytics**: Add Google Analytics or similar tracking
5. **Testing**: Cross-browser and device testing
6. **Domain Setup**: Configure www.sanvia.co to point to deployed site

## File Structure Summary

```
sanvia-website/
├── 📄 index.html                    # Main website file
├── 📁 css/
│   └── 🎨 style.css                 # Responsive styling with animations
├── 📁 js/
│   └── ⚡ script.js                 # Interactive functionality
├── 📁 assets/
│   ├── 🖼️ sanvia-logo.svg           # Main logo (SVG)
│   ├── 🖼️ sanvia-logo-white.svg     # Footer logo
│   └── 🖼️ hero-antimicrobial-tech.svg # Animated hero background
├── 📁 .github/
│   └── 📝 copilot-instructions.md
├── ⚙️ render.yaml                   # Render deployment configuration
├── 🤖 robots.txt                    # Search engine instructions  
├── 🗺️ sitemap.xml                   # Site structure for SEO
├── 📋 DEPLOYMENT.md                 # Detailed deployment guide
└── 📖 README.md                     # This file
```

## Live Preview

- **Development:** `http://localhost:8000` (local server)
- **Production:** `https://sanvia.co` (after deployment)
- **Render URL:** `https://sanvia-website.onrender.com` (temporary)

## Quick Deploy

See `DEPLOYMENT.md` for complete step-by-step instructions.

## Support

For questions about this website implementation, please contact the development team or refer to the project documentation.

## License

This project is proprietary to Sanvia Inc. All rights reserved.