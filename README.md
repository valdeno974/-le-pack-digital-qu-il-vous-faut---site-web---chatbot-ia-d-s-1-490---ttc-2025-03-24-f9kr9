# Landing Page Maintenance Guide

This guide will help you maintain and customize the Valdeno landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold text-gray-800">Valdeno</a>

<!-- How to modify -->
<a href="/" class="text-2xl font-bold text-gray-800">Your Company Name</a>
```

#### Hero Section
The main headline and subtext can be found in:
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Le pack digital qu'il vous faut : site web + chatbot IA dès 1 490 € TTC
</h1>
<p class="text-xl md:text-2xl mb-8">Des solutions digitales simples, efficaces et rentables</p>
```

To modify:
1. Locate the text within the `<h1>` or `<p>` tags
2. Replace with your new content
3. Maintain the existing HTML structure

### Tailwind CSS Classes Explained

#### Responsive Design Classes
The landing page uses these key responsive prefixes:
- `md:` - applies styles on medium screens (768px and up)
- No prefix - applies to all screen sizes

Example from navigation:
```html
<div class="hidden md:flex items-center space-x-8">
```
- `hidden` hides element on mobile
- `md:flex` shows element as flex container on medium screens

#### Common Class Patterns

Button styling:
```html
class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition-colors duration-300"
```
- `bg-blue-600`: Background color
- `text-white`: Text color
- `px-6`: Horizontal padding
- `py-2`: Vertical padding
- `rounded-full`: Rounded corners
- `hover:bg-blue-700`: Color change on hover
- `transition-colors`: Smooth color transition

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<a href="#features">Fonctionnalités</a>
<a href="#benefits">Avantages</a>
<a href="#faq">FAQ</a>
```

To update:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use full URL: `https://example.com`

### Footer Links
Current footer links need updating:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
</ul>
```

Replace `#` with actual URLs:
```html
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
```

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
In the footer section, locate:
```html
<li><a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
```

Update to:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
```

### Adding Terms Link
Similarly, update the terms link:
```html
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
```

### Maintaining Consistent Styling
Keep these classes for all footer links:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - Verify that sections have unique IDs

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` classes are correctly applied
   - Test at different screen sizes

3. **Missing Styles**
   - Confirm Tailwind CSS CDN link is working
   - Check for typos in class names
   - Verify class combinations are valid

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test changes in a development environment first
- Keep a backup of the original HTML file
- Use browser developer tools to inspect elements

Remember to test all changes across different devices and browsers before deploying to production.