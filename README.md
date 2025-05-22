# Fridget Landing Page Maintenance Guide

This guide will help you maintain and customize the Fridget mini fridge landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Fridget</a>
```
- Replace "Fridget" with your desired company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight">
    Mini Fridges, Maximum Efficiency
</h1>
<p class="mt-6 text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto">
    Discover compact refrigeration solutions for every space.
</p>
```

To modify:
1. Replace the headline text between the `<h1>` tags
2. Update the subheading text in the `<p>` tag
3. The responsive text sizes (`text-4xl md:text-5xl lg:text-6xl`) ensure proper scaling:
   - `text-4xl`: Mobile devices
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Energy Efficient</h3>
    <p class="text-gray-600">Low power consumption without compromising performance</p>
</div>
```

To add or modify features:
1. Copy the entire `<div>` block
2. Replace the heading text in `<h3>`
3. Update the description in `<p>`
4. Maintain the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
The navigation menu contains both internal and external links:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="https://fridget.curatedspot.com/" class="inline-flex items-center...">Shop Now</a>
</div>
```

To update links:
1. Internal links (starting with #) connect to page sections
   - Ensure the href matches the section's id attribute
   - Example: `href="#features"` links to `<section id="features">`
2. External links (starting with http/https)
   - Replace the full URL in `href=""`
   - Keep the `class` attributes unchanged for consistent styling

### Shop Now Button Links
Update all "Shop Now" button links:

```html
<!-- Hero section button -->
<a href="https://fridget.curatedspot.com/" class="inline-flex items-center...">
    Find Your Perfect Mini Fridge
</a>

<!-- Bottom CTA button -->
<a href="https://fridget.curatedspot.com/" class="inline-flex items-center...">
    Shop Now
</a>
```

## Adding Privacy and Terms Pages

### Footer Legal Links
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive: `#FAQ` is different from `#faq`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These ensure proper display on different screen sizes

3. **Style Inconsistencies**
   - Always copy entire `class=""` attributes when duplicating elements
   - Maintain the same color schemes:
     - Blue: `text-blue-600`
     - Gray text: `text-gray-600`
     - White backgrounds: `bg-white`

### Need Help?
- Verify changes in multiple browsers
- Test on both desktop and mobile devices
- Keep a backup of the original HTML file
- Use browser developer tools (F12) to inspect elements

Remember to test all changes thoroughly before publishing to your live site!