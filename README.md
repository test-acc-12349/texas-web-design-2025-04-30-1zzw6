# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-md z-50">
    <div class="text-2xl font-bold text-blue-600">TWD</div>
</header>
```

To modify:
- Change "TWD" to your company name
- Adjust logo size by modifying `text-2xl` (options: text-sm, text-lg, text-3xl)
- Change logo color by updating `text-blue-600` (options: text-red-600, text-green-600)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Texas Web Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10 leading-relaxed">
    Best Websites In Texas
</p>
```

To modify:
- Replace "Texas Web Design" with your headline
- Update subheading "Best Websites In Texas"
- Adjust text size using the responsive classes:
  - `text-4xl`: mobile size
  - `md:text-5xl`: tablet size
  - `lg:text-6xl`: desktop size

### Features & Benefits Sections
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```

To modify:
- Change icon by updating `fa-server` to any Font Awesome icon
- Update heading and description text
- Adjust padding with `p-8` (options: p-4, p-6, p-12)
- Modify shadow with `shadow-lg` (options: shadow-sm, shadow-md, shadow-xl)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```

To update:
1. For internal section links, ensure the `href` matches the section's ID
2. For external links, replace `#` with full URL:
   ```html
   <a href="https://yoursite.com/page" class="text-gray-600 hover:text-blue-600">
   ```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <i class="fab fa-twitter text-xl"></i>
    </a>
    <!-- Similar structure for Facebook and LinkedIn -->
</div>
```

To update:
1. Replace `#` with your social media profile URLs
2. Add or remove social icons by copying the structure and changing the icon class

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the Quick Links section in the footer:

```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in ID names
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify all responsive classes (sm:, md:, lg:) are correct
   - Test different screen sizes

3. **Icon Not Showing**
   - Verify Font Awesome CDN link is present in header
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon style prefix (fas, fab, far)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check Font Awesome icons at [fontawesome.com](https://fontawesome.com/icons)
- Test your page using browser developer tools (F12)

Remember to always test changes across different devices and browsers before deploying to production.