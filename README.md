# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

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
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#contact">Contact</a> <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent mb-6">
    Your financial success is our bottom line <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Expert accounting services... <!-- Subheadline -->
</p>
```

### Tailwind CSS Classes Explained
- `text-5xl`: Large text size (increases with md: and lg: prefixes)
- `font-bold`: Bold text weight
- `bg-gradient-to-r`: Right-directed gradient background
- `mb-6`: Margin bottom spacing (6 units)
- `hidden md:flex`: Hidden on mobile, flex display on medium screens
- `space-x-8`: Horizontal spacing between elements

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com" class="...">
    Get Started
</a>
```

### Updating Links
1. Internal Links (same page sections):
   - Keep the `#` symbol
   - Match the ID of the target section
   ```html
   <a href="#features">Features</a>
   <!-- Corresponds to -->
   <section id="features">
   ```

2. External Links:
   - Replace `https://theaccountants.com` with your actual URL
   - Always include `https://` or `http://`
   ```html
   <a href="https://your-actual-website.com">Get Started</a>
   ```

3. Email Links:
```html
<a href="mailto:support@example.com">
    support@example.com <!-- Update with actual email -->
</a>
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add New Pages
1. Create new files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update href attributes:
```html
<!-- Before -->
<a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a>

<!-- After -->
<a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
```

3. Maintain consistent styling:
   - Copy the header and footer from index.html
   - Use the same Tailwind CSS classes for consistency

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match href attributes
   - Check for typos in ID names
   - Ensure IDs are unique

2. **Responsive Design Issues**
   - Check media query prefixes (md:, lg:)
   - Verify container widths
   - Test on multiple screen sizes

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
     ```

### Tips
- Always test changes in multiple browsers
- Use browser developer tools to inspect elements
- Back up files before making changes
- Keep the original HTML as a reference

Remember to update the copyright year in the footer:
```html
<p>&copy; 2024 Albert Park Accounting. All rights reserved.</p>
```

For additional help or advanced customization, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).