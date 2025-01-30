# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Antikythera business automation landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-xl font-bold text-blue-600">Antikythera</div>
```
- Replace "Antikythera" with your company name
- The `text-xl` class controls size
- `text-blue-600` controls color

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep the `href` attributes matching section IDs
- Maintain the class structure for consistent styling

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Business Automation with AI Agents and n8n
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    AI Automation will change how you run your business
</p>
```
- Update heading and paragraph text as needed
- Keep responsive classes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain spacing classes (`mb-8`, `mb-12`)

### Features and Benefits
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text here.</p>
</div>
```
- Update titles in `<h3>` tags
- Modify descriptions in `<p>` tags
- Keep all styling classes intact for consistent design

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match href values
2. For external links, use full URLs:
```html
<a href="https://example.com">External Link</a>
```

### Call-to-Action Buttons
Current placeholder:
```html
<a href="www.google.com/" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started
</a>
```
To fix:
1. Replace `www.google.com/` with your actual URL
2. Add `https://` prefix for external links
3. Verify the link works before deploying

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Styles**
- Verify Tailwind CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for typos in class names
- Ensure responsive classes use correct breakpoints (md:, lg:)

2. **Animation Issues**
- Verify AOS script and CSS are loaded:
```html
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
```
- Check data-aos attributes on elements
- Ensure AOS.init() is called

3. **Navigation Problems**
- Verify section IDs match href values
- Check for duplicate IDs (must be unique)
- Ensure smooth scroll behavior is working

### Best Practices
- Always test changes in multiple browsers
- Validate links before deploying
- Maintain consistent spacing and alignment
- Keep backup copies before making major changes
- Test responsive design at different screen sizes

Remember to validate your HTML using [W3C Validator](https://validator.w3.org/) after making changes to ensure everything remains properly formatted and accessible.