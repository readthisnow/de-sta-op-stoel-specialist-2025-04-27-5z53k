# Landing Page Maintenance Guide

This guide will help you maintain and customize the Sta-Op-Stoel landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">
    Sta-Op-Stoel  <!-- Change this text to update your logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Voordelen</a>
    <!-- Update text between <a> tags to change menu items -->
</div>
```

### Hero Section
Located at the top of the page under the header:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight">
    De Sta-Op-Stoel Specialist  <!-- Main headline -->
</h1>
<p class="mt-6 text-xl md:text-2xl text-gray-600">
    Tijdelijk 10% Korting op ons gehele assortiment  <!-- Subheadline -->
</p>
```

#### Tailwind CSS Class Guide for Beginners
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, etc.
- Spacing: `mt-6` (margin-top), `px-4` (padding-left and right)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#benefits">Waarom Wij</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Find the `href` attribute
2. Replace the value with your new link:
   - For internal sections: Use `#section-name`
   - For external pages: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center justify-center px-8 py-4 text-lg font-medium text-white bg-blue-600 rounded-full hover:bg-blue-700">
    Profiteer Nu
</a>
```

To update:
1. Locate the `href` attribute
2. Replace `https://sta-opstoelen.nl` with your desired URL
3. Update button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
```

### Maintaining Consistent Styling
When creating new pages, copy these classes for consistent link styling:
- Normal links: `text-gray-600 hover:text-gray-900 transition-colors duration-300`
- Footer links: `hover:text-white transition-colors duration-300`

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href values
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check responsive prefixes (`sm:`, `md:`, `lg:`)
   - Test on different screen sizes
   - Verify `hidden` and `flex` classes are properly used

3. **Style Changes Not Working**
   - Confirm Tailwind CSS is properly loaded
   - Check for conflicting classes
   - Verify class names are spelled correctly

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers

Remember to:
- Back up your files before making changes
- Test all links after updates
- Verify changes on mobile and desktop views
- Keep your content and links up to date