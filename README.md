# KN Chemizol Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the KN Chemizol landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<div class="text-xl font-bold">KN Chemizol</div>
```

To update the company name:
1. Locate this div in the header section
2. Replace "KN Chemizol" with your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (current size)
   - `text-2xl` (larger)
   - `text-lg` (smaller)

### Hero Section
The main headline and subheading are located in:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8">
    KN Chemizol Precision Tribology Lab Instruments & Lubricant Testing Solutions
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accelerate your lubricant R&D and quality assurance with KN
</p>
```

To modify:
1. Replace text content within the `<h1>` and `<p>` tags
2. Responsive text sizes are controlled by:
   - `text-4xl` (mobile)
   - `md:text-5xl` (medium screens)
   - `lg:text-6xl` (large screens)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-50 rounded-xl p-8 hover:shadow-lg transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Custom Proprietary Testing</h3>
    <p class="text-gray-600">Specialized testing solutions...</p>
</div>
```

To add or modify features:
1. Copy the entire feature card div
2. Replace the heading in `<h3>` tags
3. Update the description in `<p>` tags
4. Modify the SVG icon if needed

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. For internal links (same page):
   - Use `#section-id` format
   - Ensure corresponding section IDs exist
3. For external links:
   - Replace with full URL (e.g., `https://example.com`)

### Contact Links
Current contact links:

```html
<a href="mailto:sudha@knchemizol.com" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">
    Email Us
</a>
<a href="https://wa.link/lkqqud" class="inline-block bg-green-500 text-white px-8 py-4 rounded-lg">
    WhatsApp
</a>
```

To update:
1. Replace email address in `mailto:` link
2. Update WhatsApp link with your specific URL

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 KN Chemizol. All rights reserved.</p>
    <!-- Add this below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

To implement:
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the above code into your footer section
3. Style consistently using similar Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Verify section IDs match href attributes
   - Section IDs should be unique
   - Check for typos in both href and id attributes

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Test on different screen sizes

3. **Missing Styles**
   - Confirm Tailwind CDN is loaded
   - Check for typos in class names
   - Verify class combinations are valid

### Need Help?
For additional support:
- Review [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser console for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.