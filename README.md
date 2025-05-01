# Landing Page Maintenance Guide

This guide will help you maintain and customize the Best Websites Paris landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu:

```html
<div class="text-2xl font-bold text-gray-800">
    Best Websites Paris  <!-- Update company name here -->
</div>
```

To modify:
1. Locate this section at the top of the page
2. Replace "Best Websites Paris" with your company name
3. Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
Update main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Custom Websites For Your Business  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Professional web development services tailored for businesses in Paris  <!-- Subheadline -->
</p>
```

Key Tailwind classes explained:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `leading-tight`: Line height control

### Features and Benefits Sections
Each card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-magic text-3xl"></i>  <!-- Icon -->
    </div>
    <h3 class="text-xl font-bold mb-4 text-gray-900">Easy to Use</h3>  <!-- Title -->
    <p class="text-gray-600 leading-relaxed">  <!-- Description -->
        Intuitive interfaces and user-friendly designs that make website management effortless.
    </p>
</div>
```

To modify:
1. Change icon by replacing `fa-magic` with any [Font Awesome](https://fontawesome.com/icons) icon class
2. Update title text in the `<h3>` tag
3. Modify description in the `<p>` tag

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

To update:
1. The `#` symbol indicates an internal page link
2. Ensure section IDs match these links (e.g., `id="features"` for `href="#features"`)
3. For external links, replace with full URL: `href="https://example.com"`

### Call-to-Action Buttons
Update the main CTA buttons:

```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started  <!-- Button text -->
</a>
```

Replace `https://sigmaseo.io` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Locate the legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4 text-white">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your website directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that section IDs match their corresponding links
   - Section IDs should be unique
   - Check for typos in both the ID and href attributes

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from Tailwind classes
   - Keep the viewport meta tag in the header
   - Test on multiple screen sizes using browser dev tools

3. **Icons Not Showing**
   - Ensure Font Awesome CSS is properly linked in the header
   - Check for correct icon class names
   - Verify internet connection as icons are loaded from CDN

Remember to:
- Test all changes in multiple browsers
- Validate links before publishing
- Keep backup copies of working versions
- Maintain consistent styling across all pages

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).