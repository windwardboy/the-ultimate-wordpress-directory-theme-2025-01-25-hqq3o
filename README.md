# Directory Kings Landing Page - Maintenance Guide

Welcome to the maintenance guide for the Directory Kings landing page. This document will help you make common updates and modifications to the page, even if you're new to web development.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-indigo-500 bg-clip-text text-transparent">
    Directory Kings  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-200">Features</a>
<!-- To add a new menu item, copy and paste this line and update the href and text -->
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
    The Ultimate WordPress Directory Theme  <!-- Update this text for your main headline -->
</h1>
```

#### Understanding Tailwind Classes
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-8`: Margin bottom spacing
- `bg-gradient-to-r`: Right-directed gradient background

### Features Section
To update feature cards:

1. Locate the feature card container:
```html
<div class="bg-gray-800 rounded-xl p-8 transform hover:scale-105 transition-all duration-300 border border-gray-700 hover:border-purple-500">
```

2. Update icon:
```html
<i class="fas fa-magic text-3xl"></i>
<!-- Change fa-magic to any Font Awesome icon name -->
```

3. Update heading and description:
```html
<h3 class="text-xl font-semibold mb-4">Intuitive and easy to use</h3>
<p class="text-gray-400">Simple and powerful interface that makes directory building a breeze.</p>
```

## Managing Links

### Navigation Links
Current links in the navigation:
- Features: `#features`
- Benefits: `#benefits`
- Get Started: `#contact`

To update:
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-200">
    Features  <!-- Update href and text as needed -->
</a>
```

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://directory-kings.com/contact" class="inline-block px-8 py-4 rounded-full bg-gradient-to-r from-purple-600 to-indigo-600...">
    Start Building Today  <!-- Update href and button text -->
</a>
```

### Social Media Links
Located in the footer:
```html
<a href="#" class="text-gray-400 hover:text-white transition-colors">
    <i class="fab fa-twitter"></i>
</a>
<!-- Replace # with your social media profile URLs -->
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the Quick Links section in the footer and add:
```html
<ul class="space-y-2">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors">Features</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors">Benefits</a></li>
    <!-- Add these new lines -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create `privacy.html` and `terms.html` in the same directory as `index.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all href attributes start with either:
     - `#` for page sections
     - `https://` for external links
     - Relative paths (`/`, `./`) for local pages

2. **Styling Issues**
   - If gradients aren't showing:
     ```html
     <!-- Make sure these classes are present -->
     bg-gradient-to-r from-purple-500 to-indigo-500
     ```
   
3. **Icons Not Displaying**
   - Verify Font Awesome CSS is loaded:
     ```html
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
     ```

### Need More Help?
- Double-check all class names match exactly (Tailwind is case-sensitive)
- Ensure all HTML tags are properly closed
- Verify all custom URLs are correctly spelled and accessible

Remember to test all changes across different screen sizes using your browser's developer tools (F12 key).