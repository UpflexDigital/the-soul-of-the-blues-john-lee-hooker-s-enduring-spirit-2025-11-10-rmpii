# Blues Heritage Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, customizing, and managing your John Lee Hooker Blues Heritage landing page.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Colors and Styling](#modifying-colors-and-styling)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Creating Privacy and Terms Pages](#creating-privacy-and-terms-pages)
6. [Responsive Design Basics](#responsive-design-basics)
7. [Common Issues & Troubleshooting](#common-issues--troubleshooting)
8. [File Structure Best Practices](#file-structure-best-practices)

---

## Quick Start Overview

### What You're Working With

This landing page uses three main technologies:

- **HTML**: The structure and content (text, images, links)
- **Tailwind CSS**: A styling system that makes your page look professional
- **JavaScript**: Interactive features like the mobile menu and FAQ accordion

### File Organization

Before you start editing, understand your file structure:

```
your-project-folder/
├── index.html          (Main landing page - the file you have)
├── privacy.html        (Create this for privacy policy)
├── terms.html          (Create this for terms of service)
├── blog.html           (Optional: for blog section)
└── assets/             (Optional folder for images/files)
    └── images/
```

**Key Point**: All these files should be in the same folder for links to work properly.

---

## Updating Text Content

### Understanding the Structure

Your landing page has distinct sections. Each section contains text you can customize. Here's how to find and update them:

### Hero Section (The Main Banner)

**Location in Code**: Lines 145-187

This is the first thing visitors see. Here's what you can change:

#### 1. Main Headline

**Current text:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900">
    The Soul of the Blues: John Lee Hooker's Enduring Spirit
</h1>
```

**How to change it:**
- Find the text between `<h1>` and `</h1>` tags
- Replace it with your own headline
- Keep the tags themselves unchanged

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900">
    Discover the Legacy of American Blues Music
</h1>
```

#### 2. Subheading Paragraph

**Current text:**
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-lg">
    Discover the profound impact and continuing influence of a legendary blues pioneer...
</p>
```

**How to change it:**
- Find the text between `<p>` and `</p>` tags
- Replace with your new text
- Keep the class attributes (the long text after `class=`)

**Example:**
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-lg">
    Explore the rich history and cultural significance of blues music through our 
    comprehensive collection of documentaries, academic resources, and community forums.
</p>
```

### Features Section

**Location in Code**: Lines 229-330

This section has three feature cards. Each card contains:

#### Feature Title

**Current example (Feature 1):**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Documentary Previews</h3>
```

**How to change it:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Your New Title Here</h3>
```

#### Feature Description

**Current example:**
```html
<p class="text-gray-600 leading-relaxed mb-4">
    Immerse yourself in expertly crafted documentary content featuring rare archival footage...
</p>
```

**How to change it:**
```html
<p class="text-gray-600 leading-relaxed mb-4">
    Your description text goes here. You can write as much or as little as you want.
</p>
```

#### Feature Bullet Points

**Current example:**
```html
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-center gap-2">
        <svg class="w-4 h-4 text-gray-800" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
        </svg>
        Rare archival footage
    </li>
</ul>
```

**How to change bullet points:**
- Find each `<li>` tag
- Replace the text after the `</svg>` tag with your new bullet point

**Example:**
```html
<li class="flex items-center gap-2">
    <svg class="w-4 h-4 text-gray-800" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
    </svg>
    Your new bullet point text
</li>
```

**Important**: Don't delete or modify the `<svg>` code (the checkmark icon). Only change the text.

### Benefits Section

**Location in Code**: Lines 346-475

Similar structure to Features. Update titles and descriptions the same way.

### Testimonials Section

**Location in Code**: Lines 507-650

Each testimonial has:

#### Quote Text
```html
<p class="text-gray-700 mb-4 leading-relaxed">
    "The documentary previews are absolutely phenomenal..."
</p>
```

#### Author Name
```html
<p class="font-bold text-gray-900">Marcus Thompson</p>
```

#### Author Title
```html
<p class="text-sm text-gray-600">Music Historian & Educator</p>
```

**How to update testimonials:**
```html
<p class="text-gray-700 mb-4 leading-relaxed">
    "Your customer's quote goes here. Keep the quotation marks!"
</p>
<div class="border-t border-gray-300 pt-4">
    <p class="font-bold text-gray-900">Customer Name</p>
    <p class="text-sm text-gray-600">Their Title or Role</p>
</div>
```

### FAQ Section

**Location in Code**: Lines 779-870

Each FAQ item has a question and answer:

#### Question
```html
<span class="text-lg md:text-xl font-bold text-gray-900">
    What types of content are available on the platform?
</span>
```

#### Answer
```html
<div class="faq-answer hidden px-6 md:px-8 pb-6 text-gray-700 leading-relaxed">
    <p>Our platform offers a comprehensive collection of resources...</p>
</div>
```

**How to update FAQ:**
```html
<!-- Change the question -->
<span class="text-lg md:text-xl font-bold text-gray-900">
    Your new FAQ question?
</span>

<!-- Change the answer -->
<div class="faq-answer hidden px-6 md:px-8 pb-6 text-gray-700 leading-relaxed">
    <p>Your answer to the question goes here.</p>
</div>
```

### Footer Text

**Location in Code**: Lines 953-1000

#### Company Description
```html
<p class="text-sm text-gray-400">
    Preserving and celebrating the enduring legacy of John Lee Hooker and the blues tradition.
</p>
```

Change to:
```html
<p class="text-sm text-gray-400">
    Your company description here.
</p>
```

#### Copyright Year
```html
<p class="text-sm text-gray-400 text-center md:text-left mb-4 md:mb-0">
    &copy; 2025 Blues Heritage Project. All rights reserved.
</p>
```

Change to:
```html
<p class="text-sm text-gray-400 text-center md:text-left mb-4 md:mb-0">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

---

## Modifying Colors and Styling

### Understanding Tailwind CSS Classes

Tailwind CSS uses short codes to style elements. Here are the main ones used in your page:

#### Text Colors

| Class | Color | Usage |
|-------|-------|-------|
| `text-gray-900` | Dark gray/black | Main text |
| `text-gray-700` | Medium gray | Body text |
| `text-gray-600` | Light gray | Secondary text |
| `text-white` | White | Text on dark backgrounds |
| `text-yellow-400` | Yellow | Star ratings |

#### Background Colors

| Class | Color | Usage |
|-------|-------|-------|
| `bg-white` | White | Card backgrounds |
| `bg-gray-50` | Very light gray | Section backgrounds |
| `bg-gray-900` | Dark gray/black | Buttons, headers |
| `bg-gradient-to-br` | Gradient | Hero section |

### Changing Button Colors

**Current Primary Button:**
```html
<a href="https://seelbachs.com/..." class="btn-primary inline-flex items-center justify-center gap-2 bg-gray-900 text-white px-8 py-4 rounded-full font-bold text-lg hover:bg-gray-800 transition-colors duration-300 shadow-lg">
    Explore the Legacy
</a>
```

**To change from dark gray to blue:**
```html
<a href="https://seelbachs.com/..." class="btn-primary inline-flex items-center justify-center gap-2 bg-blue-600 text-white px-8 py-4 rounded-full font-bold text-lg hover:bg-blue-700 transition-colors duration-300 shadow-lg">
    Explore the Legacy
</a>
```

**Explanation:**
- `bg-gray-900` = background color (dark gray)
- `text-white` = text color (white)
- `hover:bg-gray-800` = what color it becomes when you hover over it
- Change all three to match your color scheme

### Available Tailwind Colors

```
gray, blue, red, green, yellow, purple, pink, indigo, teal, cyan, orange
```

Add a number to specify shade:
- `100` = very light
- `500` = medium
- `900` = very dark

**Examples:**
- `bg-blue-600` = medium blue background
- `text-green-700` = dark green text
- `hover:bg-red-500` = turns red on hover

### Changing Section Background Colors

**Current:**
```html
<section id="features" class="py-20 md:py-28 lg:py-32 px-4 sm:px-6 lg:px-8 bg-white">
```

**To change to light gray:**
```html
<section id="features" class="py-20 md:py-28 lg:py-32 px-4 sm:px-6 lg:px-8 bg-gray-50">
```

**To change to light blue:**
```html
<section id="features" class="py-20 md:py-28 lg:py-32 px-4 sm:px-6 lg:px-8 bg-blue-50">
```

### Changing Text Size

Tailwind uses these size classes:

| Class | Size | Usage |
|-------|------|-------|
| `text-sm` | Small | Labels, captions |
| `text-lg` | Large | Body text |
| `text-xl` | Extra large | Subheadings |
| `text-2xl` | 2x large | Section titles |
| `text-3xl` | 3x large | Main headings |
| `text-4xl` | 4x large | Hero headings |

**Current:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
    Comprehensive Resources & Features
</h2>
```

**To make smaller:**
```html
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4">
    Comprehensive Resources & Features
</h2>
```

### Changing Font Weight (Boldness)

| Class | Weight |
|-------|--------|
| `font-normal` | Regular |
| `font-semibold` | Semi-bold |
| `font-bold` | Bold |

**Current:**
```html
<p class="font-bold text-gray-900">Marcus Thompson</p>
```

**To make regular weight:**
```html
<p class="font-normal text-gray-900">Marcus Thompson</p>
```

### Changing Spacing (Padding/Margins)

- `p-` = padding (space inside)
- `m-` = margin (space outside)
- `px-` = horizontal padding
- `py-` = vertical padding

Numbers represent spacing amount (4, 6, 8, 12, 16, 20, etc.)

**Current:**
```html
<div class="p-8">Content here</div>
```

**To increase padding:**
```html
<div class="p-12">Content here</div>
```

---

## Fixing and Managing Links

### Understanding Link Types

Your page has three types of links:

1. **Internal Links** - Point to sections on the same page (start with `#`)
2. **External Links** - Point to other websites (start with `http://` or `https://`)
3. **Page Links** - Point to other HTML files in your folder

### Current Links in Your Page

#### Navigation Menu Links

**Location in Code**: Lines 35-48 (Desktop) and Lines 51-60 (Mobile)

**Current:**
```html
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Contact</a>
```

**These are correct** - they point to sections with matching IDs on the same page:
- `#features` points to `<section id="features">`
- `#benefits` points to `<section id="benefits">`
- etc.

#### External Links (Currently Broken)

**Location in Code**: Lines 169-172 and 1047-1050

**Current:**
```html
<a href="https://seelbachs.com/products/john-lee-hooker-legacy-spirits-boogie-chillen-bourbon-kentucky-straight-bourbon-collection" target="_blank" rel="noopener noreferrer" class="btn-primary...">
    Explore the Legacy
</a>
```

**These are external links** (they go to another website). They work as-is, but you can change them:

**To change the destination:**
```html
<a href="https://your-website.com/your-page" target="_blank" rel="noopener noreferrer" class="btn-primary...">
    Explore the Legacy
</a>
```

**Explanation of attributes:**
- `href="..."` = where the link goes
- `target="_blank"` = opens in a new tab
- `rel="noopener noreferrer"` = security feature (keep it)

#### Footer Links (Broken - Need to Fix)

**Location in Code**: Lines 960-965

**Current:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
```

**Problem**: These files don't exist yet. You'll create them in the next section.

#### Social Media Links

**Location in Code**: Lines 973-989 and 1001-1017

**Current:**
```html
<a href="#" class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-gray-100 text-gray-900 hover:bg-gray-900 hover:text-white transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To fix these:**

Replace `href="#"` with your actual social media URLs:

```html
<!-- Facebook -->
<a href="https://facebook.com/your-page-name" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-gray-100 text-gray-900 hover:bg-gray-900 hover:text-white transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/your-handle" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-gray-100 text-gray-900 hover:bg-gray-900 hover:text-white transition-colors duration-300" aria-label="Twitter">
    <i class="fab fa-twitter"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/your-handle" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-gray-100 text-gray-900 hover:bg-gray-900 hover:text-white transition-colors duration-300" aria-label="Instagram">
    <i class="fab fa-instagram"></i>
</a>

<!-- YouTube -->
<a href="https://youtube.com/your-channel" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-gray-100 text-gray-900 hover:bg-gray-900 hover:text-white transition-colors duration-300" aria-label="YouTube">
    <i class="fab fa-youtube"></i>
</a>
```

#### Email Link

**Location in Code**: Line 920

**Current:**
```html
<a href="mailto:technoeg2723@gmail.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">technoeg2723@gmail.com</a>
```

**To change:**
```html
<a href="mailto:your-email@example.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">your-email@example.com</a>
```

Also change the second instance at line 953:
```html
<p class="text-gray-600">
    Or email us directly at <a href="mailto:hello@example.com" class="text-blue-600 hover:text-blue-700 font-semibold">hello@example.com</a>
</p>
```

### Quick Reference: All Links to Update

| Link Type | Current Value | Location | Status |
|-----------|---------------|----------|--------|
| Primary CTA | seelbachs.com | Lines 169, 1047 | External - works |
| Privacy | privacy.html | Line 960 | Needs file |
| Terms | terms.html | Line 961 | Needs file |
| Blog | blog.html | Line 962 | Needs file |
| Facebook | # | Line 974 | Broken |
| Twitter | # | Line 979 | Broken |
| Instagram | # | Line 984 | Broken |
| YouTube | # | Line 989 | Broken |
| Email | technoeg2723@gmail.com | Line 920 | Update |

---

## Creating Privacy and Terms Pages

### Step 1: Create the Privacy Policy File

**What you're doing**: Creating a new HTML file called `privacy.html`

**Step-by-step:**

1. Open your text editor (VS Code, Notepad++, or even Notepad)
2. Create a new file
3. Copy and paste this code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Blues Heritage Project">
    <title>Privacy Policy - Blues Heritage</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-full bg-gradient-to-br from-gray-800 to-gray-600 flex items-center justify-center">
                    <i class="fas fa-music text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">Blues Heritage</span>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 lg:py-32 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="bg-white rounded-2xl p-8 md:p-12 shadow-md border border-gray-200 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Introduction</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The Blues Heritage Project ("we," "our," or "us") is committed to protecting your privacy. 
                        This Privacy Policy explains how we collect, use, disclose, and safeguard your information 
                        when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Information We Collect</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We may collect information about you in a variety of ways. The information we may collect on 
                        the Site includes:
                    </p>
                    <ul class="space-y-2 text-gray-700">
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span><strong>Personal Data:</strong> Name, email address, phone number, and other information 
                            you voluntarily provide through contact forms.</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span><strong>Usage Data:</strong> Information about how you interact with our website, including 
                            pages visited and time spent on pages.</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span><strong>Device Information:</strong> Browser type, IP address, and operating system.</span>
                        </li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">How We Use Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We use the information we collect in various ways, including to:
                    </p>
                    <ul class="space-y-2 text-gray-700">
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Provide, operate, and maintain our website</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Improve, personalize, and expand our website</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Understand and analyze how you use our website</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Develop new products, services, features, and functionality</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Communicate with you, either directly or through one of our partners</span>
                        </li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Security of Your Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We use administrative, technical, and physical security measures to help protect your personal 
                        information. While we have taken reasonable steps to secure the personal information you provide to us, 
                        please be aware that no security measures are perfect or impenetrable.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:technoeg2723@gmail.com" class="text-blue-600 hover:text-blue-700">technoeg2723@gmail.com</a>
                    </p>
                </div>

                <div class="pt-4 border-t border-gray-200">
                    <p class="text-sm text-gray-600">
                        Last updated: <span id="last-updated"></span>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-sm text-gray-400 mb-4">
                    &copy; 2025 Blues Heritage Project. All rights reserved.
                </p>
                <div class="flex gap-6 justify-center text-sm">
                    <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Auto-update the "Last updated" date
        document.getElementById('last-updated').textContent = new Date().toLocaleDateString('en-US', { 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });
    </script>
</body>
</html>
```

4. Save the file as `privacy.html` in the same folder as your `index.html`

**To customize the privacy policy:**
- Replace the content in the `<p>` and `<li>` tags with your actual privacy policy
- Keep the HTML structure (tags) the same
- Update the contact email to your actual email

### Step 2: Create the Terms of Service File

**What you're doing**: Creating a new HTML file called `terms.html`

**Step-by-step:**

1. Create another new file in your text editor
2. Copy and paste this code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Blues Heritage Project">
    <title>Terms of Service - Blues Heritage</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-full bg-gradient-to-br from-gray-800 to-gray-600 flex items-center justify-center">
                    <i class="fas fa-music text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">Blues Heritage</span>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium transition-colors duration-300">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 lg:py-32 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="bg-white rounded-2xl p-8 md:p-12 shadow-md border border-gray-200 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Agreement to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These Terms of Service constitute a legally binding agreement made between you, whether personally 
                        or on behalf of an entity ("you") and the Blues Heritage Project ("we," "us," or "our"), concerning 
                        your access to and use of the website and all related applications, tools, and services.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Intellectual Property Rights</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Unless otherwise indicated, the Site is our proprietary property and all source code, databases, 
                        functionality, software, website designs, audio, video, text, photographs, and graphics on the Site 
                        (collectively, the "Content") and the trademarks, service marks, and logos contained therein (the "Marks") 
                        are owned or controlled by us or licensed to us.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">User Responsibilities</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        By using our website, you agree to:
                    </p>
                    <ul class="space-y-2 text-gray-700">
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Not use the site in any way that violates any applicable law or regulation</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Not engage in any conduct that restricts or inhibits anyone's use or enjoyment of the website</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Not post content that is abusive, harassing, defamatory, or obscene</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <span class="text-blue-600 font-bold">•</span>
                            <span>Not attempt to gain unauthorized access to any portion of the website</span>
                        </li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Limitation of Liability</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall the Blues Heritage Project, its directors, employees, or agents be liable to you or 
                        any third party for any direct, indirect, consequential, exemplary, incidental, special, or punitive 
                        damages resulting from your use of the website or any related services.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Modifications to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We may revise these Terms of Service for the Site at any time without notice. By using this Site, you 
                        are agreeing to be bound by the then current version of these Terms of Service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:technoeg2723@gmail.com" class="text-blue-600 hover:text-blue-700">technoeg2723@gmail.com</a>
                    </p>
                </div>

                <div class="pt-4 border-t border-gray-200">
                    <p class="text-sm text-gray-600">
                        Last updated: <span id="last-updated"></span>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-sm text-gray-400 mb-4">
                    &copy; 2025 Blues Heritage Project. All rights reserved.
                </p>
                <div class="flex gap-6 justify-center text-sm">
                    <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Auto-update the "Last updated" date
        document.getElementById('last-updated').textContent = new Date().toLocaleDateString('en-US', { 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });
    </script>
</body>
</html>
```

3. Save the file as `terms.html` in the same folder as your `index.html`

### Step 3: Verify Your Files Are Set Up Correctly

Your folder should now look like this:

```
your-project-folder/
├── index.html
├── privacy.html
├── terms.html
└── (any other files)
```

**Important**: All three files must be in the SAME folder for the links to work.

### Step 4: Test the Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should take you to `privacy.html`
4. Click on "Terms of Service" - it should take you to `terms.html`
5. Click "Home" links to return to `index.html`

**If links don't work**, make sure:
- File names match exactly (case-sensitive)
- All files are in the same folder
- You're using the correct file names: `privacy.html` and `terms.html`

### Step 5: Customize Your Policy Pages

**For Privacy Policy:**
1. Open `privacy.html`
2. Find the sections like "Information We Collect" and "How We Use Your Information"
3. Replace the bullet points and descriptions with your actual privacy practices
4. Update the email address from `technoeg2723@gmail.com` to your email

**For Terms of Service:**
1. Open `terms.html`
2. Find the sections like "User Responsibilities" and "Limitation of Liability"
3. Replace with your actual terms
4. Update the email address to your email

**What NOT to change:**
- Don't remove or modify the HTML tags (like `<div>`, `<p>`, `<h2>`)
- Don't delete the navigation or footer
- Keep the Tailwind CSS classes the same

---

## Responsive Design Basics

### Understanding Responsive Design

Your page automatically adjusts for different screen sizes using Tailwind CSS breakpoints:

| Breakpoint | Screen Size | Device |
|------------|------------|--------|
| (none) | < 768px | Mobile phones |
| `md:` | 768px - 1024px | Tablets |
| `lg:` | > 1024px | Desktops |

### How It Works in Your Code

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    The Soul of the Blues
</h1>
```

**Breakdown:**
- `text-4xl` = size on mobile phones
- `md:text-5xl` = larger size on tablets
- `lg:text-6xl` = largest size on desktops

### Common Responsive Classes

#### Display/Hiding

```html
<!-- Hidden on mobile, visible on desktop -->
<div class="hidden md:flex">Desktop only content</div>

<!-- Visible on mobile, hidden on desktop -->
<div class="md:hidden">Mobile only content</div>
```

#### Padding/Margins

```html
<!-- Small padding on mobile, larger on desktop -->
<div class="px-4 md:px-6 lg:px-8 py-20 md:py-28 lg:py-32">
    Content
</div>
```

#### Grid Layouts

```html
<!-- 1 column on mobile, 2 on tablets, 3 on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Cards here -->
</div>
```

### Testing Responsive Design

**In your browser:**
1. Open your website
2. Press `F12` to open Developer Tools
3. Press `Ctrl+Shift+M` (or `Cmd+Shift+M` on Mac) to toggle device mode
4. Select different devices to test

**Common issues:**
- Text too small on mobile? Increase `text-lg` to `text-xl`
- Too much padding? Reduce `p-8` to `p-4`
- Cards overlapping? Make sure grid has `gap-8`

---

## Common Issues & Troubleshooting

### Issue 1: Links Not Working

**Problem**: You click a link and nothing happens

**Solutions:**

1. **Check the file name:**
   ```html
   <!-- WRONG - file is named "Privacy.html" but link says "privacy.html" -->
   <a href="privacy.html">Privacy</a>
   
   <!-- CORRECT - names match exactly -->
   <a href="privacy.html">Privacy</a>
   ```

2. **Check the file location:**
   - Make sure `privacy.html` and `index.html` are in the SAME folder
   - Don't put them in subfolders unless you update the path

3. **For external links, use full URL:**
   ```html
   <!-- WRONG - missing https:// -->
   <a href="facebook.com/mypage">Facebook</a>
   
   <!-- CORRECT -->
   <a href="https://facebook.com/mypage">Facebook</a>
   ```

### Issue 2: Styling Looks Wrong

**Problem**: Colors don't match, text is too big/small, or spacing is off

**Solutions:**

1. **Check Tailwind classes:**
   ```html
   <!-- WRONG - space in class name -->
   <div class="text-gray 900">Text</div>
   
   <!-- CORRECT - no spaces -->
   <div class="text-gray-900">Text</div>
   ```

2. **Verify color exists:**
   - Valid: `gray`, `blue`, `red`, `green`, `yellow`, `purple`, `pink`, `indigo`, `teal`, `cyan`, `orange`
   - Invalid: `darkblue`, `lightgray` (use `gray-900` or `gray-100` instead)

3. **Check for typos:**
   ```html
   <!-- WRONG -->
   <div class="bg-grey-50">Content</div>
   
   <!-- CORRECT -->
   <div class="bg-gray-50">Content</div>
   ```

### Issue 3: Mobile Menu Not Working

**Problem**: The hamburger menu doesn't appear or doesn't toggle

**Solution**: The JavaScript at the bottom handles this. Make sure you didn't accidentally delete it.

Check that this code is still at the bottom of your `index.html`:

```javascript
<script>
    document.addEventListener('DOMContentLoaded', function() {
        // Mobile Menu Toggle
        const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
        const mobileMenu = document.querySelector('header nav .mobile-menu');
        
        if (mobileMenuButton && mobileMenu) {
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
                // ... rest of code
            });
        }
    });
</script>
```

### Issue 4: FAQ Accordion Not Working

**Problem**: Clicking FAQ questions doesn't expand/collapse answers

**Solution**: The JavaScript at the bottom handles this. Make sure the code is still there and not deleted.

### Issue 5: Images Not Loading

**Problem**: You see broken image icons instead of pictures

**Solutions:**

1. **Check the image URL:**
   ```html
   <!-- WRONG - URL doesn't exist -->
   <img src="https://invalid-url.com/image.jpg" alt="Description">
   
   <!-- CORRECT - valid Unsplash image -->
   <img src="https://images.unsplash.com/photo-1511379938547-c1f69b13d835?w=600&h=600&fit=crop" alt="John Lee Hooker">
   ```

2. **For local images, use correct path:**
   ```html
   <!-- If image is in assets/images folder -->
   <img src="assets/images/my-image.jpg" alt="Description">
   ```

### Issue 6: Form Not Submitting

**Problem**: Contact form doesn't send messages

**Solution**: You need to set up Web3Forms. Follow these steps:

1. Go to https://web3forms.com
2. Sign up for a free account
3. Create an access key
4. Find this line in your `index.html`:
   ```html
   <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
   ```
5. Replace `YOUR_WEB3FORMS_ACCESS_KEY` with your actual key from Web3Forms
6. Save and test the form

---

## File Structure Best Practices

### Recommended Folder Organization

```
blues-heritage-website/
├── index.html                    (Main landing page)
├── privacy.html                  (Privacy policy)
├── terms.html                    (Terms of service)
├── blog.html                     (Optional: blog page)
│
├── assets/                       (All media files)
│   ├── images/
│   │   ├── logo.png
│   │   ├── hero-image.jpg
│   │   └── testimonial-1.jpg
│   ├── videos/
│   │   └── documentary-preview.mp4
│   └── documents/
│       ├── research-paper.pdf
│       └── discography.pdf
│
├── css/                          (Optional: custom styles)
│   └── custom.css
│
├── js/                           (Optional: custom scripts)
│   └── custom.js
│
└── README.md                     (Documentation)
```

### File Naming Conventions

**Use lowercase with hyphens:**
```
✓ CORRECT:
- privacy-policy.html
- terms-of-service.html
- hero-image.jpg
- my-custom-style.css

✗ WRONG:
- Privacy Policy.html (spaces)
- TermsOfService.html (uppercase)
- My Image.jpg (spaces)
- myCustomStyle.css (camelCase)
```

### Linking Files from Subfolders

**If your image is in `assets/images/`:**
```html
<img src="assets/images/logo.png" alt="Logo">
```

**If your CSS is in `css/`:**
```html
<link rel="stylesheet" href="css/custom.css">
```

**If your JavaScript is in `js/`:**
```html
<script src="js/custom.js"></script>
```

### Updating Links When Files Move

If you move `privacy.html` into a `pages/` folder:

**Before:**
```html
<a href="privacy.html">Privacy</a>
```

**After:**
```html
<a href="pages/privacy.html">Privacy</a>
```

---

## Advanced Customization Tips

### Adding Custom Colors

If you want to use a color not in Tailwind's standard palette:

**Option 1: Use inline styles (quick fix)**
```html
<div style="background-color: #FF6B6B; color: white;">
    Custom colored content
</div>
```

**Option 2: Add to Tailwind config (better)**

Find this in your `<head>`:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

Add this right after:
```html
<script>
    tailwind.config = {
        theme: {
            extend: {
                colors: {
                    'brand-blue': '#1E40AF',
                    'brand-gold': '#D97706',
                }
            }
        }
    }
</script>
```

Then use in your HTML:
```html
<button class="bg-brand-blue text-white">Click me</button>
```

### Adding Animations

Add this to your `<style>` section:

```css
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

.animate-fade-in {
    animation: fadeIn 0.5s ease-in;
}
```

Then use it:
```html
<div class="animate-fade-in">This fades in</div>
```

### Custom Fonts

Add to your `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
<style>
    .font-playfair {
        font-family: 'Playfair Display', serif;
    }
</style>
```

Use it:
```html
<h1 class="font-playfair">Beautiful Heading</h1>
```

---

## Maintenance Checklist

### Weekly Tasks
- [ ] Check for broken links
- [ ] Review contact form submissions
- [ ] Monitor website performance

### Monthly Tasks
- [ ] Update testimonials or content
- [ ] Check for browser compatibility
- [ ] Review analytics (if you have them)
- [ ] Test all forms and contact methods

### Quarterly Tasks
- [ ] Update copyright year in footer
- [ ] Review and update privacy policy if needed
- [ ] Check for outdated information
- [ ] Test on mobile devices

### Annual Tasks
- [ ] Full security audit
- [ ] Update SSL certificate (if applicable)
- [ ] Review and refresh design
- [ ] Update all links and resources

---

## Getting Help

### Resources

- **Tailwind CSS Documentation**: https://tailwindcss.com/docs
- **HTML Learning**: https://www.w3schools.com/html/
- **CSS Learning**: https://www.w3schools.com/css/
- **Font Awesome Icons**: https://fontawesome.com/icons

### Common Questions

**Q: How do I change the site title that appears in the browser tab?**
A: Find this line in `<head>`:
```html
<title>The Soul of the Blues: John Lee Hooker's Enduring Spirit</title>
```
Change the text between `<title>` tags.

**Q: How do I add a new section to the page?**
A: Copy an existing section (like Features or Benefits) and modify the content. Keep the same HTML structure.

**Q: Can I use this on a domain I own?**
A: Yes! Upload all your HTML files to your web hosting and point your domain to them.

---

## Summary

You now have a complete guide to:

✅ Update all text content on your landing page  
✅ Modify colors and styling with Tailwind CSS  
✅ Fix broken links and manage navigation  
✅ Create and link Privacy and Terms pages  
✅ Understand responsive design  
✅ Troubleshoot common issues  
✅ Organize your files properly  

**Remember**: Always save your changes and test your website in a browser before publishing. Start with small changes and gradually build your confidence!

Happy maintaining! 🎵