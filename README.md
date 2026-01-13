# MBW Tech Services - HTML Version

This is the static HTML version of the MBW Tech Services React website. All layouts, stylings, and structure have been preserved from the original React application.

## 📁 File Structure

```
html-version/
├── index.html          # Home page
├── about.html          # About page
├── services.html       # Services page with modals
├── contact.html        # Contact page with form
├── blogs.html          # Blog listing page
├── styles.css          # Custom CSS styles (includes Tailwind via CDN)
├── script.js           # JavaScript for interactivity
└── README.md           # This file
```

## 🚀 Features

- **All pages converted to static HTML** - No React dependencies
- **Tailwind CSS via CDN** - All styling preserved
- **Interactive modals** - Service previews and blog reading
- **Mobile responsive menu** - Works on all devices
- **Contact form** - Integrated with Formspree
- **Animations** - CSS animations replacing Framer Motion
- **Same design** - All layouts, colors, and styling maintained

## 📄 Pages

1. **index.html** - Home page with hero section, services overview, and features
2. **about.html** - About page with company information and services
3. **services.html** - Services page with guidance and assistance services (includes modals)
4. **contact.html** - Contact page with contact form and details
5. **blogs.html** - Blog listing page with all blog posts (includes reading modal)

## 🎨 Styling

- **Tailwind CSS** - Loaded via CDN in each HTML file
- **Custom CSS** - Additional styles in `styles.css` for:
  - Brain background animations
  - Glass morphism effects
  - Neon shadows
  - Fade animations
  - Modal animations

## ⚙️ JavaScript Functionality

The `script.js` file handles:
- Mobile menu toggle
- Service modal opening/closing
- Blog modal opening/closing
- Contact form success message
- Scroll animations
- Intersection Observer for fade-in effects

## 🔗 Asset Paths

All asset paths are relative to the `html-version` folder:
- Images: `../mbw-website/src/assets/`
- Logo: `../mbw-website/src/assets/mbwlogo.png`
- Brain image: `../mbw-website/src/assets/mind.png`
- Favicon: `../mbw-website/public/favIcon/mbwlogo.png`

## 📝 Notes

- The contact form uses Formspree (same endpoint as React version)
- All blog content is embedded in the HTML
- Service data is embedded in the HTML
- No build process required - just open HTML files in a browser
- All animations use CSS instead of Framer Motion
- All routing is done via standard HTML links

## 🌐 Usage

Simply open any HTML file in a web browser. For best results, serve via a local web server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000/index.html`

## ✅ What's Preserved

- ✅ All layouts and structure
- ✅ All Tailwind CSS classes
- ✅ All colors and styling
- ✅ All content and text
- ✅ All images and assets
- ✅ All animations (converted to CSS)
- ✅ All functionality (modals, forms, menus)
- ✅ Responsive design
- ✅ SEO meta tags

## 🔄 Differences from React Version

- No React Router - using standard HTML links
- No Framer Motion - using CSS animations
- No React state - using vanilla JavaScript
- No component structure - all inline HTML
- No build process - static files only

