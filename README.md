# jv-ot

https://logicxd.github.io/jv-ot/

# Occupational Therapist Profile Website

A clean, modern, and responsive personal profile website for occupational therapy professionals. Built with vanilla HTML and CSS, optimized for GitHub Pages hosting.

## Features

- **Fully Responsive**: Works beautifully on desktop, tablet, and mobile devices
- **Modern Design**: Clean aesthetic with sage green and warm neutral color palette
- **Fast Loading**: No heavy frameworks, just optimized HTML/CSS
- **Accessible**: WCAG compliant with semantic HTML and proper contrast ratios
- **Easy to Customize**: Simple structure with clear sections and CSS variables
- **GitHub Pages Ready**: Designed for quick deployment

## Quick Start

### 1. Deploy to GitHub Pages

1. Create a new GitHub repository (or use this one)
2. Go to repository **Settings** > **Pages**
3. Under **Source**, select your main branch
4. Click **Save**
5. Your site will be published at `https://[username].github.io/[repository-name]/`

### 2. Customize Your Information

Edit `index.html` and replace the placeholder text with your actual information:

#### Personal Information (Lines 28-35)
```html
<h1 class="hero-title">Your Name</h1>
<p class="hero-subtitle">Occupational Therapist, OTR/L</p>
<p class="hero-tagline">Your personalized tagline here</p>
```

#### About Section (Lines 58-78)
- Update your bio and introduction
- Add your credentials:
  - State license number
  - Years of experience
  - Education details
  - Certifications
  - Professional affiliations

#### Services Section (Lines 85-134)
Customize the four service cards with your specializations:
- Pediatric Therapy
- Hand Therapy
- Ergonomic Consulting
- Rehabilitation
- Or add your own focus areas

#### Company Information (Lines 142-157)
```html
<h3 class="company-name">[Company/Practice Name]</h3>
<p class="company-description">
    [Brief description of the company]
</p>
<a href="https://www.company-website.com" ...>
```

#### Contact Information (Lines 174-215)
Update your contact details:
- Email address
- Phone number
- LinkedIn profile URL

### 3. Add Your Professional Photo

Replace the placeholder image icon:

1. Add your professional headshot to the repository (e.g., `photo.jpg`)
2. In `index.html` around line 38, replace the placeholder div:

```html
<!-- Before (placeholder): -->
<div class="image-placeholder">
    <svg xmlns="https://www.w3.org/2000/svg" ...>
    </svg>
</div>

<!-- After (with your photo): -->
<div class="image-placeholder">
    <img src="photo.jpg" alt="Your Name, Occupational Therapist">
</div>
```

## Customization Guide

### Change Colors

All colors are defined as CSS variables in `styles.css` (lines 5-17). Update these to change the entire color scheme:

```css
:root {
    --color-primary: #6B8E6F;        /* Sage green - main brand color */
    --color-accent: #E8836C;         /* Coral - accent color */
    --color-neutral-light: #FAFAF8;  /* Cream background */
    --color-text-dark: #2C3E50;      /* Dark text */
    /* ... more colors ... */
}
```

#### Alternative Color Schemes

**Cool Blues:**
```css
--color-primary: #5A7D9A;
--color-accent: #7FB3D5;
```

**Warm Earthy:**
```css
--color-primary: #8B7355;
--color-accent: #D4A574;
```

### Change Fonts

To use custom Google Fonts:

1. Add to `<head>` in `index.html`:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600&family=Open+Sans:wght@400;500&display=swap" rel="stylesheet">
```

2. Update CSS variables in `styles.css`:
```css
--font-heading: 'Montserrat', sans-serif;
--font-base: 'Open Sans', sans-serif;
```

### Modify Sections

#### Add a New Service Card

Copy an existing service card block in `index.html` (lines 86-95) and customize:

```html
<div class="service-card">
    <div class="service-icon">
        <!-- Add your SVG icon here -->
    </div>
    <h3>Your Service Name</h3>
    <p>Service description here.</p>
</div>
```

#### Add a Testimonials Section

Add between the services and company sections:

```html
<section class="testimonials">
    <div class="container">
        <h2 class="section-title">What Clients Say</h2>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <p>"Testimonial text here..."</p>
                <p class="client-name">- Client Name</p>
            </div>
        </div>
    </div>
</section>
```

Add corresponding CSS to `styles.css`.

### Adjust Spacing and Layout

Spacing is controlled by CSS variables (lines 23-28):

```css
--spacing-xs: 0.5rem;
--spacing-sm: 1rem;
--spacing-md: 2rem;
--spacing-lg: 3rem;
--spacing-xl: 4rem;
--spacing-xxl: 6rem;
```

## File Structure

```
jv-ot/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── README.md          # This file
└── [your-photo.jpg]   # Your professional photo (add this)
```

## Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Accessibility Features

- Semantic HTML5 elements
- ARIA labels where needed
- High contrast text (WCAG AA compliant)
- Keyboard navigation support
- Responsive images with alt text
- Screen reader friendly

## SEO Optimization

Update the `<head>` section in `index.html` for better SEO:

```html
<meta name="description" content="[Your name], licensed Occupational Therapist specializing in [your specialties]. [City, State]">
<meta name="keywords" content="occupational therapist, OT, [specialties], [city]">
<title>[Your Name], OTR/L - Occupational Therapist | [City]</title>
```

## Tips for Professional Use

1. **Professional Photo**: Use a high-quality headshot (ideally 400x400px or larger)
2. **Keep it Updated**: Regularly update your credentials and experience
3. **Mobile Testing**: Always test on mobile devices after changes
4. **Privacy**: Don't include client names in testimonials without permission
5. **HIPAA Compliance**: Avoid sharing any protected health information
6. **Contact Form**: Consider adding a contact form service (e.g., Formspree, Google Forms)

## Adding a Contact Form

To add a working contact form, you can use free services like:

### Option 1: Formspree
1. Sign up at [formspree.io](https://formspree.io)
2. Get your form endpoint
3. Add to your HTML:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="email" name="email" placeholder="Your Email" required>
    <textarea name="message" placeholder="Your Message" required></textarea>
    <button type="submit" class="btn btn-primary">Send Message</button>
</form>
```

### Option 2: Google Forms
1. Create a Google Form
2. Get the shareable link
3. Embed or link to it from your contact section

## Performance Optimization

The site is already optimized, but you can further improve:

1. **Compress Images**: Use tools like TinyPNG or ImageOptim
2. **Lazy Loading**: Add `loading="lazy"` to images
3. **Minify CSS**: Use online CSS minifiers before deployment

## Support & Troubleshooting

### Common Issues

**Site not showing on GitHub Pages:**
- Check Settings > Pages is enabled
- Ensure `index.html` is in the root directory
- Wait 5-10 minutes for deployment

**Images not loading:**
- Verify file paths are correct (case-sensitive)
- Ensure images are committed to the repository
- Use relative paths (e.g., `./photo.jpg` not `/photo.jpg`)

**Styling looks broken:**
- Check that `styles.css` is in the same directory as `index.html`
- Verify the `<link>` tag in the HTML is correct
- Clear browser cache and reload

## Next Steps

1. Customize all placeholder text with your information
2. Add your professional photo
3. Update colors/fonts if desired
4. Test on multiple devices
5. Deploy to GitHub Pages
6. Share your new professional profile!

## License

Free to use and modify for personal or professional purposes.

---

**Questions or need help?** Feel free to reach out or consult the GitHub Pages documentation at [docs.github.com/pages](https://docs.github.com/pages)