# PolicyPals Landing Page Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-500">PolicyPals</a>
```
To update the company name:
1. Locate the header section (first `<header>` tag)
2. Find the anchor tag with class `text-2xl`
3. Replace "PolicyPals" with your desired text

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
To update the main headline:
1. Find the hero section (after header)
2. Locate the `<h1>` tag
3. Replace the text between the tags

### Tailwind CSS Class Modifications

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `sm:` (640px and up)
- `md:` (768px and up)
- `lg:` (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Class Modifications

To change button colors:
```html
<!-- Original -->
<a href="#" class="bg-blue-600 hover:bg-blue-700">

<!-- To change to green -->
<a href="#" class="bg-green-600 hover:bg-green-700">
```

To modify spacing:
```html
<!-- Original -->
<div class="mb-8">

<!-- To increase spacing -->
<div class="mb-12">
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://PolicyPals.Co.Uk">Get Started</a>
```

To update:
1. Locate the navigation section in the header
2. For internal links (starting with #):
   - Ensure the href matches the ID of the target section
   - Example: `href="#features"` should match `id="features"`
3. For external links:
   - Replace `https://PolicyPals.Co.Uk` with your actual domain
   - Ensure URLs include `https://`

### Footer Links
```html
<div class="Quick Links">
    <ul class="space-y-2">
        <li><a href="#features">Features</a></li>
        <li><a href="#benefits">Benefits</a></li>
        <li><a href="#faq">FAQ</a></li>
    </ul>
</div>
```

To update:
1. Find the footer section (last section before closing body tag)
2. Locate the Quick Links list
3. Update href attributes following the same rules as navigation links

## 3. Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Current footer legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Cookie Policy</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting Tips

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Always test changes at different screen sizes
   - Use browser dev tools to preview mobile/tablet views
   - Keep responsive classes (sm:, md:, lg:) when modifying

3. **Style Inconsistencies**
   - Copy existing classes for new elements to maintain consistency
   - Check text colors match the theme (blue-500, gray-400, etc.)
   - Maintain hover states on interactive elements

## Need Help?

If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all files are in the correct directory
3. Ensure all links start with either `http://`, `https://`, or `/`
4. Compare your changes against the original code
5. Test the page in multiple browsers

Remember to always backup your files before making changes!