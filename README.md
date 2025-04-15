# Onyx Landing Page - Maintenance Guide

This guide will help you maintain and customize the Onyx Landing Page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Onyx" to your brand name:
```html
<div class="text-2xl font-bold text-gray-900">Onyx</div>
```

2. **Navigation Items**: Update the menu items in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Kenmerken</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
</div>
```

### Hero Section
Located right after the header, containing the main offer:

1. **Promotion Banner**: Update the discount text:
```html
<span class="inline-block px-4 py-2 rounded-full bg-red-100 text-red-800 text-sm font-semibold mb-6">
    ⚡ NOG MAAR 30% KORTING - BEPERKTE TIJD!
</span>
```

2. **Main Heading**: Change the product title:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Onyx Koffer 65 Liter
</h1>
```

### Tailwind CSS Classes Explained
Common classes used throughout the page:

- `container mx-auto`: Centers content with automatic margins
- `px-4 sm:px-6 lg:px-8`: Responsive padding (increases on larger screens)
- `text-gray-600`: Sets text color
- `hover:scale-105`: Enlarges element on hover
- `md:grid-cols-2`: Creates 2 columns on medium screens

## Managing Links

### Navigation Links
Internal section links are found in the header:

```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```

To update:
1. Change the `href` value to match your section ID
2. Update the text between `<a>` tags
3. Ensure corresponding sections have matching IDs

### Product Links
The main call-to-action buttons link to Amazon:

```html
<a href="https://amzn.to/42JzAch" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 px-8 rounded-lg">
    Bekijk Aanbieding
</a>
```

To update:
1. Replace `https://amzn.to/42JzAch` with your product URL
2. Update button text as needed

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<footer class="bg-gray-900 text-gray-400 py-12">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

2. Add new links (insert before the copyright notice):
```html
<div class="text-sm">
    <h3 class="text-white font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify all `md:` and `lg:` prefixed classes
   - Test different screen sizes

3. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names
   - Use browser inspector to verify applied styles

### Need Help?
- Inspect the page using browser developer tools (F12)
- Check the console for error messages
- Verify all files are in the correct directory
- Ensure all external resources (TailwindCSS, AlpineJS) are loading

Remember to test all changes across different devices and browsers before publishing updates to your live site.