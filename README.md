# StoreNinja Landing Page Maintenance Guide

This guide will help you maintain and customize the StoreNinja landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Locate this section in the header:
```html
<a href="/" class="text-xl font-bold text-white hover:text-blue-400 transition duration-300">
    Store<span class="text-blue-500">Ninja</span>
</a>
```
- Change "Store" and "Ninja" to your desired text
- Keep the `<span>` tag to maintain the blue highlight on the second word

2. **Navigation Links**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition duration-300">FAQ</a>
</div>
```
- Update text between `>` and `</a>` for each link
- Keep the `text-gray-300` and other classes to maintain hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-8">
    How To Start An Online Store
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Find A Winning Product In 3 Steps
</p>
```
- Update text between the tags while maintaining the classes
- The `md:` and `lg:` prefixes control responsive text sizes
- Don't remove these classes or mobile responsiveness will break

### Tailwind CSS Class Guide
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[number]`: Adds margin bottom (4, 8, 12, etc.)
- `py-[number]`: Adds padding top and bottom
- `bg-[color]-[shade]`: Sets background color
- `hover:`: Prefix for hover effects

## Managing Links

### External Links
Look for links containing "https://ninja200.online":
```html
<a href="https://ninja200.online" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">
```
Replace with your desired URL while maintaining the classes.

### Internal Links
Navigation menu links use hashtags to scroll to sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
These correspond to section IDs:
```html
<section id="features">
<section id="benefits">
<section id="faq">
```
- Keep IDs and href values matching
- Don't change the `scroll-smooth` class in the HTML tag

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
- Check that you haven't removed any `md:` or `lg:` prefixed classes
- Verify the viewport meta tag is present in the head

2. **Smooth Scroll Not Working**
- Ensure the HTML tag has `class="scroll-smooth"`
- Verify section IDs match navigation href values exactly

3. **Hover Effects Missing**
- Look for missing `hover:` classes
- Check that `transition duration-300` is present

### Need Help?
- Contact: admin@ninja200.online
- Review the Tailwind CSS documentation for class references
- Test all changes in multiple browsers and screen sizes

Remember to always backup your files before making changes and test thoroughly on different devices and browsers.