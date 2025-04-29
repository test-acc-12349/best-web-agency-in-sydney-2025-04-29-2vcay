# Landing Page Maintenance Guide

This guide will help you maintain and customize your web agency landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Locate the header section (around line 18):
```html
<div class="text-xl font-bold tracking-tight">
    <a href="/" class="text-white hover:text-blue-400 transition duration-300">Sydney Web Agency</a>
</div>
```
- Replace "Sydney Web Agency" with your company name
- Keep the existing classes to maintain styling

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Grow your business with clicks
</p>
```

Understanding the classes:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `bg-gradient-to-r`: Creates right-flowing gradient
- `text-transparent`: Makes text transparent to show gradient

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8 transform hover:scale-105 transition duration-300 shadow-lg hover:shadow-blue-500/10">
    <div class="text-blue-400 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-400">Intuitive interfaces and user-friendly designs...</p>
</div>
```

To modify features:
1. Find the features section (around line 56)
2. Update the h3 text for the feature title
3. Update the p text for the feature description
4. Maintain the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-400 transition duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-400 transition duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-400 transition duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-400 transition duration-300">Contact</a>
</div>
```

To update links:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - For same-page sections, use `#section-name`
   - For other pages, use the full path (e.g., `/about.html`)
3. Update the link text between `<a>` tags

### Call-to-Action Links
There are two CTA buttons linking to "fixrr.online":
```html
<a href="https://fixrr.online" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold px-8 py-4 rounded-lg transform hover:scale-105 transition duration-300 shadow-lg hover:shadow-blue-500/25">
    Get Started Today
</a>
```

To update:
1. Replace `https://fixrr.online` with your desired URL
2. Ensure the URL includes `https://` for external links
3. Update button text as needed

## Adding Privacy and Terms Pages

### Footer Links Section
Locate the legal links in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check that all `href` attributes have correct paths
   - Verify file names match exactly (case-sensitive)
   - Test all links after updating

2. **Styling Issues**
   - Don't remove Tailwind classes unless you're sure about their purpose
   - Keep responsive classes (starting with `md:` or `lg:`)
   - Maintain hover effects (`hover:` classes)

3. **Layout Problems**
   - Keep the container classes (`container mx-auto px-6`)
   - Preserve grid classes for proper column layout
   - Don't remove padding/margin classes (`p-8`, `mb-4`, etc.)

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).