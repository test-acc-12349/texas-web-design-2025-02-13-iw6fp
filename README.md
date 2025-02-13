# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Location Guide
The page is divided into these main sections:
- Header (navigation): Lines 16-35
- Hero section: Lines 37-50
- Features section: Lines 52-85
- Benefits section: Lines 87-106
- Video section: Lines 108-116
- FAQ section: Lines 118-141
- Contact section: Lines 143-156
- Footer: Lines 158-184

### Updating Text Content

To update text content, locate the specific section and modify the text between the HTML tags. For example:

```html
<!-- Original hero title -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>

<!-- To update, change the text between the tags -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Your New Title Here</h1>
```

### Understanding Tailwind CSS Classes

Key Tailwind classes used in this landing page:

1. Text Sizes:
   - `text-4xl`: Large text
   - `md:text-5xl`: Larger text on medium screens
   - `lg:text-6xl`: Largest text on large screens

2. Colors:
   - `text-gray-900`: Dark gray text
   - `text-blue-600`: Blue text
   - `bg-white`: White background

3. Spacing:
   - `px-6`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-6`: Bottom margin

To modify a style, change the corresponding class. For example:
```html
<!-- Original blue button -->
<a href="#" class="bg-blue-600 text-white">

<!-- Change to red -->
<a href="#" class="bg-red-600 text-white">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com">Get Started</a>
```

### Updating Links
1. Internal Links (same page sections):
   ```html
   <!-- Format for internal links -->
   <a href="#section-id">Link Text</a>
   ```

2. External Links:
   ```html
   <!-- Replace placeholder URL -->
   <a href="https://twd.com">Get Started</a>
   <!-- Change to your actual URL -->
   <a href="https://your-actual-domain.com">Get Started</a>
   ```

### Common Link Locations to Update
1. Header navigation (Line 19)
2. "Get Started" buttons (Lines 26, 42)
3. Footer quick links (Lines 158-184)
4. Contact email (Line 146)

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Locate the footer section and update the placeholder links:

```html
<!-- Original footer links -->
<li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- Updated footer links -->
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Creating New Policy Pages
1. Create two new files in your project directory:
   - `privacy.html`
   - `terms.html`

2. Use consistent styling by copying the header and footer from `index.html`

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
   - Ensure section IDs match href attributes
   - Check for typos in ID names
   - Verify that # is included in internal links

2. Responsive Design Issues
   - Check media query classes (md:, lg:)
   - Verify container class is present
   - Test on different screen sizes

3. Style Inconsistencies
   - Maintain consistent color classes
   - Use provided Tailwind classes
   - Check for missing responsive classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test your changes across different devices and browsers before pushing to production.