# Landing Page Maintenance Guide
## 101Headshots Website Documentation

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    101Headshots  <!-- Edit this text to change the logo -->
</a>
```

**Key Tailwind Classes Explained:**
- `text-2xl`: Sets large text size
- `bg-gradient-to-r`: Creates right-flowing gradient
- `text-transparent`: Makes text transparent to show gradient

### Hero Section
To modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Grain Valley, Missouri Corporate Headshot Photography Services
    <!-- Edit this text to change the main headline -->
</h1>

<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Photography helping Grain Valley professionals stand out.
    <!-- Edit this text to change the subtitle -->
</p>
```

**Responsive Design Classes:**
- `md:text-5xl`: Changes text size on medium screens
- `lg:text-6xl`: Changes text size on large screens

### Features Section
To modify feature cards:

```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-bold mb-4">
        Comparisons  <!-- Edit feature title -->
    </h3>
    <p class="text-gray-400">
        Compare different shots...  <!-- Edit feature description -->
    </p>
</div>
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. Replace the value with:
   - Internal sections: Use `#section-name`
   - External pages: Use full URL (e.g., `https://example.com`)

### Book Session Link
Update the main CTA button:

```html
<a href="https://www.101headshots.com" class="inline-flex items-center...">
    Book Your Session
</a>
```

Replace `https://www.101headshots.com` with your booking page URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
   - Ensure all gradient classes include both `from-` and `to-` values
   - Example: `bg-gradient-to-r from-purple-400 to-pink-500`

2. **Responsive Issues**
   - Check media query classes (md:, lg:)
   - Verify proper spacing classes are applied
   - Test on multiple screen sizes

3. **Link Problems**
   - Confirm all `href` attributes have valid values
   - Internal links should match section IDs exactly
   - External links should include `https://`

### Need Help?
- Double-check HTML syntax and closing tags
- Verify Tailwind CSS classes are spelled correctly
- Test all links in a web browser
- Use browser developer tools to inspect elements

Remember to always backup your files before making changes, and test your updates across different devices and browsers.