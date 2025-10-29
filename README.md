# ColdPlunge Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your ColdPlunge landing page. This document provides step-by-step instructions for developers of all skill levels.

---

## Table of Contents

1. [Overview](#overview)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Customizing Colors and Styling](#customizing-colors-and-styling)
8. [Best Practices](#best-practices)
9. [Troubleshooting](#troubleshooting)

---

## Overview

The ColdPlunge landing page is a modern, responsive website built with:

- **HTML5** - Semantic markup and structure
- **Tailwind CSS** - Utility-first CSS framework (via CDN)
- **Font Awesome Icons** - Professional icon library
- **Vanilla JavaScript** - Mobile menu, FAQ accordion, and smooth scrolling

### Key Features

- Fully responsive design (mobile, tablet, desktop)
- Sticky navigation header
- Smooth scrolling between sections
- Interactive FAQ accordion
- Mobile-friendly hamburger menu
- Professional footer with social links
- Contact form section

---

## File Structure

### Current File Organization

```
your-project-folder/
├── index.html                 (Main landing page)
├── privacy.html              (To be created)
├── terms.html                (To be created)
└── blog.html                 (To be created)
```

### Key Sections in index.html

| Section | ID | Purpose |
|---------|----|----|
| Announcement Bar | N/A | Shipping/guarantee message |
| Header/Navigation | N/A | Logo, menu links, sticky nav |
| Hero | `#home` | Main headline and CTA |
| Features | `#features` | Three product features |
| Benefits | `#benefits` | Three detailed benefit sections |
| About | `#about` | Company story and mission |
| Testimonials | `#testimonials` | Customer reviews (4 cards) |
| FAQ | `#faq` | Expandable questions (4 items) |
| CTA Section | N/A | Final call-to-action |
| Contact | `#contact` | Contact form and info |
| Footer | N/A | Links, social, copyright |

---

## Updating Text Content

### Understanding the HTML Structure

Before making changes, understand this basic structure:

```html
<h1>This is a heading</h1>
<p>This is a paragraph of text</p>
<a href="link-here">Click me</a>
```

- **`<h1>`, `<h2>`, `<h3>`, etc.** - Headings (h1 is largest)
- **`<p>`** - Paragraph text
- **`<a href="">`** - Links
- **`<button>`** - Clickable buttons

### Updating the Announcement Bar

**Location:** Top of the page, dark background

**Current text:**
```html
<p>🚚 Fast Worldwide Shipping - 5 days delivery | 100% Satisfaction Guarantee</p>
```

**How to change it:**

1. Open `index.html` in your text editor
2. Find the line starting with `<p>🚚 Fast Worldwide Shipping`
3. Replace the text between `<p>` and `</p>` with your message
4. Keep the emoji if desired, or replace it with another

**Example:**
```html
<!-- BEFORE -->
<p>🚚 Fast Worldwide Shipping - 5 days delivery | 100% Satisfaction Guarantee</p>

<!-- AFTER -->
<p>⭐ Limited Time Offer - Free Shipping on Orders Over $500</p>
```

### Updating the Logo Text

**Location:** Navigation header, left side

**Current text:**
```html
<span class="text-xl font-bold text-slate-900">ColdPlunge</span>
```

**How to change it:**

1. Find this line in the header section
2. Replace `ColdPlunge` with your brand name

**Example:**
```html
<!-- BEFORE -->
<span class="text-xl font-bold text-slate-900">ColdPlunge</span>

<!-- AFTER -->
<span class="text-xl font-bold text-slate-900">IceLab Pro</span>
```

### Updating the Hero Section Headline

**Location:** Large text in the middle of the page (first large section)

**Current text:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Refresh. Recover. Repeat.
</h1>
```

**How to change it:**

1. Find the `<h1>` tag with "Refresh. Recover. Repeat."
2. Replace only the text between the opening `>` and closing `</h1>`
3. Keep all the `class` attributes exactly as they are

**Example:**
```html
<!-- BEFORE -->
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Refresh. Recover. Repeat.
</h1>

<!-- AFTER -->
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Transform Your Recovery Today
</h1>
```

### Updating the Hero Subtitle

**Location:** Below the main headline

**Current text:**
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-2xl mx-auto">
    Transform your wellness routine with cold therapy recovery
</p>
```

**How to change it:**

1. Find the `<p>` tag with "Transform your wellness routine"
2. Replace the text, keeping the class attributes

**Example:**
```html
<!-- BEFORE -->
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-2xl mx-auto">
    Transform your wellness routine with cold therapy recovery
</p>

<!-- AFTER -->
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-2xl mx-auto">
    Elite athletes and fitness enthusiasts choose ColdPlunge for faster recovery
</p>
```

### Updating Feature Cards

**Location:** Three cards below the "Premium Features" heading

Each feature card has three parts to update:

**1. Feature Title**
```html
<h3 class="text-xl font-bold text-slate-900 mb-3">Digital Temperature Control</h3>
```

**2. Feature Description**
```html
<p class="text-gray-600 leading-relaxed">
    Precise temperature management from 39°F to 68°F. Customize your cold plunge experience...
</p>
```

**3. Feature Icon** (more advanced - see [Customizing Colors](#customizing-colors-and-styling))

**How to update Feature 1 (Digital Temperature Control):**

```html
<!-- BEFORE -->
<h3 class="text-xl font-bold text-slate-900 mb-3">Digital Temperature Control</h3>
<p class="text-gray-600 leading-relaxed">
    Precise temperature management from 39°F to 68°F. Customize your cold plunge experience with our advanced digital control system for optimal therapeutic benefits.
</p>

<!-- AFTER -->
<h3 class="text-xl font-bold text-slate-900 mb-3">Smart Temperature Management</h3>
<p class="text-gray-600 leading-relaxed">
    Control water temperature with precision down to one degree. Our AI-powered system learns your preferences and maintains perfect conditions automatically.
</p>
```

### Updating the About Section

**Location:** "About ColdPlunge" section with company history

**Two main paragraphs to update:**

**Paragraph 1: "Our Journey"**
```html
<p class="text-gray-700 leading-relaxed text-lg">
    Founded in 2018 by a team of sports scientists and engineers...
</p>
```

**Paragraph 2: "Our Mission & Values"**
```html
<p class="text-gray-700 leading-relaxed text-lg">
    We believe that peak performance and optimal wellness...
</p>
```

**How to change them:**

1. Find each paragraph in the About section
2. Replace the entire text while keeping the `<p>` tags and class attributes
3. You can keep the headings ("Our Journey", "Our Mission & Values") or change them

**Example:**
```html
<!-- BEFORE -->
<h3 class="text-2xl font-bold text-slate-900 mb-4">Our Journey</h3>
<p class="text-gray-700 leading-relaxed text-lg">
    Founded in 2018 by a team of sports scientists and engineers, ColdPlunge emerged from a simple mission...
</p>

<!-- AFTER -->
<h3 class="text-2xl font-bold text-slate-900 mb-4">Our Story</h3>
<p class="text-gray-700 leading-relaxed text-lg">
    Since 2015, we've been dedicated to bringing professional-grade recovery equipment to every athlete. What started as a small startup is now trusted by over 100,000 users worldwide...
</p>
```

### Updating Testimonials

**Location:** "What Our Customers Say" section with customer reviews

Each testimonial has:
- A 5-star rating (don't change this)
- Customer quote text
- Customer name
- Customer title/role

**How to update a testimonial:**

```html
<!-- BEFORE -->
<p class="text-gray-700 leading-relaxed mb-6">
    "The ColdPlunge has completely transformed my recovery routine. As a competitive runner..."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-slate-900">Marcus Chen</p>
    <p class="text-sm text-gray-600">Professional Marathon Runner</p>
</div>

<!-- AFTER -->
<p class="text-gray-700 leading-relaxed mb-6">
    "I've tried every recovery method available, and nothing compares to ColdPlunge. My performance improved dramatically..."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-slate-900">Alex Thompson</p>
    <p class="text-sm text-gray-600">Triathlon Champion</p>
</div>
```

### Updating FAQ Answers

**Location:** "Frequently Asked Questions" section

Each FAQ item has:
- A question (button text)
- An answer (hidden content that expands)

**How to update FAQ content:**

```html
<!-- BEFORE -->
<button class="faq-button w-full flex items-center justify-between p-6..." onclick="toggleFAQ(this)">
    <span class="text-lg font-semibold text-slate-900 text-left">How long should I stay in the cold plunge?</span>
    <i class="fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
</button>
<div class="faq-content">
    <div class="px-6 pb-6 text-gray-700 leading-relaxed border-t border-gray-200">
        <p class="mb-3">For beginners, we recommend starting with 1-2 minutes...</p>
    </div>
</div>

<!-- AFTER -->
<button class="faq-button w-full flex items-center justify-between p-6..." onclick="toggleFAQ(this)">
    <span class="text-lg font-semibold text-slate-900 text-left">What's the ideal water temperature?</span>
    <i class="fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
</button>
<div class="faq-content">
    <div class="px-6 pb-6 text-gray-700 leading-relaxed border-t border-gray-200">
        <p class="mb-3">Most users prefer temperatures between 45-55°F for optimal recovery...</p>
    </div>
</div>
```

**Important:** Keep the `onclick="toggleFAQ(this)"` attribute - this makes the accordion work!

### Updating Contact Information

**Location:** "Get In Touch" section and footer

**Email address:**
```html
<a href="mailto:coldplunge@yourbrand.com" class="hover:text-blue-600 transition-colors duration-300">
    coldplunge@yourbrand.com
</a>
```

**How to change it:**

1. Find `coldplunge@yourbrand.com` in the contact section
2. Replace it with your actual email address
3. Update it in THREE places:
   - Contact section (main content)
   - Contact section (footer area)
   - Footer contact info

```html
<!-- BEFORE -->
<a href="mailto:coldplunge@yourbrand.com">coldplunge@yourbrand.com</a>

<!-- AFTER -->
<a href="mailto:support@yourcompany.com">support@yourcompany.com</a>
```

**Support hours:**
```html
<p class="text-gray-600">Available Monday - Friday, 9AM - 5PM EST</p>
```

**How to change it:**

```html
<!-- BEFORE -->
<p class="text-gray-600">Available Monday - Friday, 9AM - 5PM EST</p>

<!-- AFTER -->
<p class="text-gray-600">Available 24/7 via email and chat support</p>
```

### Updating Footer Copyright Year

**Location:** Bottom of the page

The year automatically updates with this code:
```html
<span id="year"></span>
```

This is controlled by JavaScript at the bottom of the file:
```javascript
document.getElementById('year').textContent = new Date().getFullYear();
```

**You don't need to change this** - it updates automatically every year!

### Updating Footer Company Description

**Location:** Footer, left column

```html
<p class="text-sm text-gray-400 leading-relaxed mb-4">
    Premium cold therapy recovery systems designed for athletes and wellness enthusiasts worldwide.
</p>
```

**How to change it:**

```html
<!-- BEFORE -->
<p class="text-sm text-gray-400 leading-relaxed mb-4">
    Premium cold therapy recovery systems designed for athletes and wellness enthusiasts worldwide.
</p>

<!-- AFTER -->
<p class="text-sm text-gray-400 leading-relaxed mb-4">
    The #1 trusted cold plunge provider for professional athletes, fitness coaches, and health-conscious individuals globally.
</p>
```

---

## Modifying Tailwind CSS Classes

### What are Tailwind CSS Classes?

Tailwind CSS is a "utility-first" CSS framework. Instead of writing custom CSS, you use pre-made classes. For example:

```html
<!-- Instead of writing CSS, you use classes like: -->
<div class="bg-blue-600 text-white px-8 py-4 rounded-lg">
    This is a button
</div>
```

Each class does one specific thing:
- `bg-blue-600` = blue background
- `text-white` = white text
- `px-8` = horizontal padding
- `py-4` = vertical padding
- `rounded-lg` = rounded corners

### Common Tailwind Classes Used in This Landing Page

#### Text and Font Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Large text | Headings |
| `text-lg` | Medium text | Subheadings |
| `text-sm` | Small text | Captions |
| `font-bold` | Bold text | Titles |
| `font-semibold` | Semi-bold text | Emphasis |
| `text-white` | White text | On dark backgrounds |
| `text-gray-600` | Gray text | Body copy |
| `text-slate-900` | Dark gray text | Main headings |

#### Color Classes

| Class | Color | Used For |
|-------|-------|----------|
| `bg-white` | White background | Main sections |
| `bg-gray-50` | Light gray background | Alternating sections |
| `bg-blue-600` | Blue background | Buttons, accents |
| `bg-slate-900` | Dark background | Header, footer |
| `text-blue-600` | Blue text | Links, highlights |
| `text-gray-700` | Dark gray text | Body text |

#### Spacing Classes

| Class | What It Does | Size |
|-------|-------------|------|
| `px-4` | Horizontal padding | Small |
| `px-6` | Horizontal padding | Medium |
| `px-8` | Horizontal padding | Large |
| `py-2` | Vertical padding | Small |
| `py-4` | Vertical padding | Medium |
| `py-8` | Vertical padding | Large |
| `mb-4` | Margin bottom | Space below element |
| `mb-6` | Margin bottom | More space below |
| `gap-4` | Space between items | In grids/flexbox |

#### Layout Classes

| Class | What It Does |
|-------|-------------|
| `flex` | Makes items line up horizontally |
| `flex-col` | Makes items stack vertically |
| `grid` | Creates a grid layout |
| `grid-cols-1` | 1 column on mobile |
| `md:grid-cols-2` | 2 columns on medium screens |
| `lg:grid-cols-3` | 3 columns on large screens |
| `items-center` | Center items vertically |
| `justify-between` | Space items apart |
| `rounded-lg` | Rounded corners |
| `shadow-md` | Subtle shadow |
| `shadow-lg` | Larger shadow |

#### Responsive Classes

Tailwind uses prefixes for different screen sizes:

| Prefix | Screen Size | Example |
|--------|------------|---------|
| (none) | Mobile (default) | `text-4xl` |
| `sm:` | Small (640px+) | `sm:text-5xl` |
| `md:` | Medium (768px+) | `md:text-6xl` |
| `lg:` | Large (1024px+) | `lg:grid-cols-3` |
| `xl:` | Extra large (1280px+) | `xl:px-8` |

**Example:** This means "4xl text on mobile, 6xl on medium screens and up"
```html
<h1 class="text-4xl md:text-6xl">Headline</h1>
```

### Practical Examples: Modifying Tailwind Classes

#### Example 1: Making Text Larger

**Current:**
```html
<h2 class="text-3xl md:text-4xl font-bold text-slate-900 mb-4">Premium Features</h2>
```

**To make it even larger:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-slate-900 mb-4">Premium Features</h2>
```

Changed:
- `text-3xl` → `text-4xl` (larger on mobile)
- `md:text-4xl` → `md:text-5xl` (larger on medium screens)

#### Example 2: Changing Button Color

**Current (Blue):**
```html
<button class="bg-blue-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-blue-700">
    Explore Now
</button>
```

**To make it green:**
```html
<button class="bg-green-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-green-700">
    Explore Now
</button>
```

Changed:
- `bg-blue-600` → `bg-green-600` (main button color)
- `hover:bg-blue-700` → `hover:bg-green-700` (color when hovering)

#### Example 3: Changing Text Color

**Current (Dark text):**
```html
<p class="text-gray-600 leading-relaxed">
    Your paragraph text here
</p>
```

**To make it lighter:**
```html
<p class="text-gray-500 leading-relaxed">
    Your paragraph text here
</p>
```

Changed:
- `text-gray-600` → `text-gray-500` (lighter gray)

#### Example 4: Adjusting Spacing

**Current (Less space):**
```html
<div class="py-16 md:py-24 bg-white">
```

**To add more space:**
```html
<div class="py-20 md:py-32 bg-white">
```

Changed:
- `py-16` → `py-20` (more vertical padding on mobile)
- `md:py-24` → `md:py-32` (more vertical padding on medium screens)

#### Example 5: Changing Card Styling

**Current (With border and shadow):**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl">
```

**To add more shadow and remove border:**
```html
<div class="feature-card bg-white shadow-lg rounded-xl p-8 hover:shadow-2xl">
```

Changed:
- Removed `border border-gray-200`
- Changed `hover:shadow-xl` → `hover:shadow-2xl` (bigger shadow on hover)
- Added `shadow-lg` (shadow visible all the time)

### Complete Tailwind Color Palette Reference

#### Background Colors
- `bg-white` - Pure white
- `bg-gray-50` - Very light gray
- `bg-gray-100` - Light gray
- `bg-gray-200` - Medium-light gray
- `bg-blue-50` - Very light blue
- `bg-blue-100` - Light blue
- `bg-blue-600` - Medium blue
- `bg-slate-900` - Very dark gray/blue

#### Text Colors
- `text-white` - White
- `text-gray-400` - Light gray
- `text-gray-500` - Medium gray
- `text-gray-600` - Medium-dark gray
- `text-gray-700` - Dark gray
- `text-slate-900` - Very dark
- `text-blue-600` - Blue

#### Hover States
- `hover:bg-blue-700` - Darker blue on hover
- `hover:text-blue-600` - Blue text on hover
- `hover:shadow-xl` - Larger shadow on hover

### Best Practices for Modifying Classes

✅ **DO:**
- Keep all classes together in one `class=""` attribute
- Maintain responsive prefixes (`md:`, `lg:`, etc.)
- Test on mobile and desktop after changes
- Use consistent color schemes

❌ **DON'T:**
- Delete or modify the `onclick="toggleFAQ(this)"` attributes
- Change `id` attributes (used for navigation)
- Break responsive design by removing `md:` or `lg:` classes
- Use classes that don't exist in Tailwind

---

## Fixing and Managing Links

### Understanding Links in HTML

Links are created with the `<a>` tag:

```html
<a href="where-to-go">Click me</a>
```

- `href` = the destination (where the link goes)
- The text between `<a>` and `</a>` = what users see and click

### Types of Links in This Landing Page

#### 1. Internal Links (Within Your Website)

These link to sections on the same page using `#` and an ID.

**Example:**
```html
<a href="#features">Features</a>
```

This links to:
```html
<section id="features">
```

#### 2. External Links (Outside Your Website)

These use full URLs like `https://example.com`

**Example:**
```html
<a href="https://www.facebook.com/yourpage">Facebook</a>
```

#### 3. Email Links

These use `mailto:` to open the user's email client.

**Example:**
```html
<a href="mailto:support@company.com">Email Us</a>
```

#### 4. Page Links (To Other HTML Files)

These link to other pages in your folder.

**Example:**
```html
<a href="privacy.html">Privacy Policy</a>
```

### All Navigation Links in This Landing Page

**Location:** Navigation menu (appears in header and mobile menu)

**Current links:**
```html
<a href="#home">Home</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#about">About</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

**These are all internal links** - they point to sections on the same page.

#### How to Add a New Navigation Link

Let's say you want to add a "Blog" link:

1. **Find the desktop navigation** (around line 80):
```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="nav-link text-gray-700 hover:text-blue-600 font-medium text-sm">Home</a>
    <a href="#features" class="nav-link text-gray-700 hover:text-blue-600 font-medium text-sm">Features</a>
    <!-- ... other links ... -->
    <a href="#contact" class="nav-link text-gray-700 hover:text-blue-600 font-medium text-sm">Contact</a>
</nav>
```

2. **Add the new link before the closing `</nav>` tag:**
```html
<a href="blog.html" class="nav-link text-gray-700 hover:text-blue-600 font-medium text-sm">Blog</a>
```

3. **Also add it to the mobile menu** (around line 120):
```html
<nav class="flex flex-col gap-3 pt-4">
    <a href="#home" class="text-gray-700 hover:text-blue-600 font-medium text-sm py-2 px-2 rounded-lg hover:bg-gray-50 transition-colors duration-300">Home</a>
    <!-- ... other links ... -->
    <a href="#contact" class="text-gray-700 hover:text-blue-600 font-medium text-sm py-2 px-2 rounded-lg hover:bg-gray-50 transition-colors duration-300">Contact</a>
</nav>
```

4. **Add the new link before the closing `</nav>` tag:**
```html
<a href="blog.html" class="text-gray-700 hover:text-blue-600 font-medium text-sm py-2 px-2 rounded-lg hover:bg-gray-50 transition-colors duration-300">Blog</a>
```

**Result:** "Blog" now appears in both desktop and mobile menus

### All Footer Links

The footer has several link sections:

#### Quick Links Section
```html
<li><a href="#home" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Home</a></li>
<li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Features</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Benefits</a></li>
<li><a href="#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">About Us</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Testimonials</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">FAQ</a></li>
```

#### Support Section
```html
<li><a href="#contact" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Contact Us</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Blog</a></li>
<li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Shipping Info</a></li>
<li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Returns</a></li>
```

#### Social Media Links
```html
<a href="#" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

### Fixing Broken Links

**A broken link is one that:**
- Points to a file that doesn't exist
- Has a typo in the URL
- Points to `#` (nowhere)

#### Example 1: Fixing a Link to a Non-Existent File

**Current (broken):**
```html
<a href="shipping.html">Shipping Info</a>
```

**Problem:** There's no `shipping.html` file in your folder

**Fix:** Either create the file, or link to an external URL:

```html
<!-- Option 1: Link to external shipping page -->
<a href="https://www.yourcompany.com/shipping">Shipping Info</a>

<!-- Option 2: Link to a section on current page -->
<a href="#contact">Shipping Info</a>
```

#### Example 2: Fixing Social Media Links

**Current (not working):**
```html
<a href="#" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Problem:** `href="#"` doesn't go anywhere

**Fix:** Add your actual social media URLs:

```html
<a href="https://www.facebook.com/yourcompany" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
<a href="https://www.instagram.com/yourcompany" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-instagram text-white"></i>
</a>
<a href="https://www.twitter.com/yourcompany" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-twitter text-white"></i>
</a>
<a href="https://www.youtube.com/yourcompany" class="w-10 h-10 bg-slate-800 hover:bg-blue-600 rounded-lg flex items-center justify-center transition-colors duration-300">
    <i class="fab fa-youtube text-white"></i>
</a>
```

### Fixing Email Links

**Current:**
```html
<a href="mailto:coldplunge@yourbrand.com" class="hover:text-blue-600 transition-colors duration-300">
    coldplunge@yourbrand.com
</a>
```

**To update with your email:**

```html
<a href="mailto:support@yourcompany.com" class="hover:text-blue-600 transition-colors duration-300">
    support@yourcompany.com
</a>
```

**Update both:**
1. The `href="mailto:..."` part
2. The visible text (should match for clarity)

### Testing Links

After updating links, test them by:

1. **Right-click the link** → "Open link in new tab"
2. **Verify the destination** is correct
3. **Check on mobile** - use your phone or browser's mobile view
4. **Test all navigation** - make sure no links are broken

---

## Linking Privacy and Terms Pages

### Overview

Currently, the landing page has links to `privacy.html` and `terms.html`, but these files don't exist yet. This section shows you how to:

1. Create these files
2. Link them properly
3. Ensure consistent styling

### Step 1: Identify All Links to Privacy and Terms

**These links currently exist in your HTML:**

**In the Footer - Support Section:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a></li>
```

**In the Footer - Bottom Links:**
```html
<a href="privacy.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
<a href="terms.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
```

**These links are ready to go!** You just need to create the actual files.

### Step 2: Create the Privacy Policy Page

**Create a new file called `privacy.html` in the same folder as `index.html`**

Here's a complete template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for ColdPlunge">
    <meta name="author" content="Cold Plunge Brand">
    <title>Privacy Policy – ColdPlunge</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header / Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex items-center gap-2">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-400 rounded-lg flex items-center justify-center">
                        <i class="fas fa-snowflake text-white text-lg"></i>
                    </div>
                    <span class="text-xl font-bold text-slate-900">ColdPlunge</span>
                </div>

                <!-- Navigation -->
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Features</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Contact</a>
                </nav>

                <!-- Right Section -->
                <div class="flex items-center gap-4">
                    <button class="hidden sm:block bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold text-sm hover:bg-blue-700">
                        Buy Now
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-slate-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700">
                <p class="text-lg mb-6 text-gray-600">
                    <strong>Last Updated: January 2024</strong>
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">1. Introduction</h2>
                <p class="mb-6">
                    ColdPlunge ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">2. Information We Collect</h2>
                <p class="mb-4">We may collect information about you in a variety of ways. The information we may collect on the site includes:</p>
                <ul class="list-disc list-inside mb-6 space-y-2">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, shipping address</li>
                    <li><strong>Payment Information:</strong> Credit card details (processed securely)</li>
                    <li><strong>Usage Data:</strong> Browser type, IP address, pages visited</li>
                    <li><strong>Device Information:</strong> Device type, operating system</li>
                </ul>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">3. How We Use Your Information</h2>
                <p class="mb-4">We use the information we collect in the following ways:</p>
                <ul class="list-disc list-inside mb-6 space-y-2">
                    <li>To process your orders and deliver products</li>
                    <li>To send transactional and promotional emails</li>
                    <li>To improve our website and services</li>
                    <li>To respond to your inquiries</li>
                    <li>To comply with legal obligations</li>
                </ul>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">4. Data Security</h2>
                <p class="mb-6">
                    We implement appropriate technical and organizational measures to protect your personal data against unauthorized access, alteration, disclosure, or destruction. All payment information is encrypted and processed securely.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">5. Third-Party Services</h2>
                <p class="mb-6">
                    We may use third-party service providers to assist us in operating our website and conducting our business. These third parties are contractually obligated to maintain the confidentiality of your information.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">6. Cookies</h2>
                <p class="mb-6">
                    Our website uses cookies to enhance your browsing experience. You can control cookie settings in your browser preferences.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">7. Your Rights</h2>
                <p class="mb-4">You have the right to:</p>
                <ul class="list-disc list-inside mb-6 space-y-2">
                    <li>Access your personal data</li>
                    <li>Request correction of inaccurate data</li>
                    <li>Request deletion of your data</li>
                    <li>Opt-out of marketing communications</li>
                </ul>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">8. Contact Us</h2>
                <p class="mb-6">
                    If you have questions about this Privacy Policy, please contact us at:
                    <br><br>
                    <strong>Email:</strong> <a href="mailto:privacy@coldplunge.com" class="text-blue-600 hover:text-blue-700">privacy@coldplunge.com</a>
                    <br>
                    <strong>Address:</strong> [Your Company Address]
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-slate-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-slate-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                    <p class="text-sm text-gray-400 text-center md:text-left">
                        &copy; <span id="year"></span> ColdPlunge. All rights reserved.
                    </p>
                    <div class="flex gap-6">
                        <a href="privacy.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
                        <a href="terms.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 3: Create the Terms of Service Page

**Create a new file called `terms.html` in the same folder as `index.html`**

Here's a complete template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for ColdPlunge">
    <meta name="author" content="Cold Plunge Brand">
    <title>Terms of Service – ColdPlunge</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header / Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex items-center gap-2">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-400 rounded-lg flex items-center justify-center">
                        <i class="fas fa-snowflake text-white text-lg"></i>
                    </div>
                    <span class="text-xl font-bold text-slate-900">ColdPlunge</span>
                </div>

                <!-- Navigation -->
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Features</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-blue-600 font-medium text-sm">Contact</a>
                </nav>

                <!-- Right Section -->
                <div class="flex items-center gap-4">
                    <button class="hidden sm:block bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold text-sm hover:bg-blue-700">
                        Buy Now
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-slate-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700">
                <p class="text-lg mb-6 text-gray-600">
                    <strong>Last Updated: January 2024</strong>
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="mb-6">
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">2. Use License</h2>
                <p class="mb-4">Permission is granted to temporarily download one copy of the materials (information or software) on ColdPlunge's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside mb-6 space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">3. Disclaimer</h2>
                <p class="mb-6">
                    The materials on ColdPlunge's website are provided on an 'as is' basis. ColdPlunge makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">4. Limitations</h2>
                <p class="mb-6">
                    In no event shall ColdPlunge or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on ColdPlunge's website.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="mb-6">
                    The materials appearing on ColdPlunge's website could include technical, typographical, or photographic errors. ColdPlunge does not warrant that any of the materials on its website are accurate, complete, or current. ColdPlunge may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">6. Links</h2>
                <p class="mb-6">
                    ColdPlunge has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by ColdPlunge of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">7. Modifications</h2>
                <p class="mb-6">
                    ColdPlunge may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">8. Governing Law</h2>
                <p class="mb-6">
                    These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction], and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <h2 class="text-2xl font-bold text-slate-900 mt-8 mb-4">9. Contact Information</h2>
                <p class="mb-6">
                    If you have any questions about these Terms of Service, please contact us at:
                    <br><br>
                    <strong>Email:</strong> <a href="mailto:legal@coldplunge.com" class="text-blue-600 hover:text-blue-700">legal@coldplunge.com</a>
                    <br>
                    <strong>Address:</strong> [Your Company Address]
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-slate-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-slate-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                    <p class="text-sm text-gray-400 text-center md:text-left">
                        &copy; <span id="year"></span> ColdPlunge. All rights reserved.
                    </p>
                    <div class="flex gap-6">
                        <a href="privacy.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
                        <a href="terms.html" class="text-sm text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 4: Verify Your File Structure

After creating these files, your folder should look like:

```
your-project-folder/
├── index.html           ✓ (Already exists)
├── privacy.html         ✓ (Just created)
├── terms.html           ✓ (Just created)
└── blog.html            (Optional - create if needed)
```

### Step 5: Test the Links

1. **Open `index.html` in your browser**
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - should open `privacy.html`
4. **Click on "Terms of Service"** - should open `terms.html`
5. **From the policy pages, click the logo** - should return to `index.html`

### Step 6: Customize the Policy Pages

Both policy pages have placeholder text that you should customize:

**In both files, update:**

1. **Company Address:**
```html
<!-- BEFORE -->
<strong>Address:</strong> [Your Company Address]

<!-- AFTER -->
<strong>Address:</strong> 123 Main Street, New York, NY 10001
```

2. **Email Addresses:**
```html
<!-- In privacy.html -->
<a href="mailto:privacy@coldplunge.com">privacy@coldplunge.com</a>

<!-- In terms.html -->
<a href="mailto:legal@coldplunge.com">legal@coldplunge.com</a>
```

3. **Jurisdiction:**
```html
<!-- BEFORE -->
These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction]

<!-- AFTER -->
These terms and conditions are governed by and construed in accordance with the laws of the State of California
```

4. **Last Updated Date:**
```html
<!-- BEFORE -->
<strong>Last Updated: January 2024</strong>

<!-- AFTER -->
<strong>Last Updated: March 15, 2024</strong>
```

### Step 7: Add Links to Other Pages

If you want to add links to privacy/terms from other pages (like a blog), use the same format:

```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
```

### Troubleshooting Policy Page Links

**Problem: Link doesn't work**
- Solution: Make sure `privacy.html` and `terms.html` are in the same folder as `index.html`
- Check spelling - filenames are case-sensitive on some servers

**Problem: Page looks different from landing page**
- Solution: Both pages use the same header and footer code - this is intentional for consistency

**Problem: Links in navigation don't work**
- Solution: Check that the `href` attribute matches the filename exactly

---

## Customizing Colors and Styling

### Color System Overview

This landing page uses a consistent color scheme:

| Element | Color | Tailwind Class |
|---------|-------|-----------------|
| Primary Accent | Blue | `bg-blue-600`, `text-blue-600` |
| Hover State | Darker Blue | `hover:bg-blue-700`, `hover:text-blue-600` |
| Backgrounds | White/Gray | `bg-white`, `bg-gray-50` |
| Text (Main) | Dark Gray | `text-slate-900` |
| Text (Secondary) | Medium Gray | `text-gray-600` |
| Text (Light) | Light Gray | `text-gray-400` |
| Dark Sections | Slate | `bg-slate-900` |

### Changing the Primary Color (Blue to Green)

**Step 1: Find all blue color classes**

Search your HTML for:
- `bg-blue-600`
- `bg-blue-700`
- `text-blue-600`
- `hover:bg-blue-600`
- `hover:text-blue-600`
- `border-blue-100`
- `from-blue-600`
- `to-blue-400`

**Step 2: Replace with green equivalents**

| Blue | Green |
|------|-------|
| `bg-blue-600` | `bg-green-600` |
| `bg-blue-700` | `bg-green-700` |
| `bg-blue-400` | `bg-green-400` |
| `text-blue-600` | `text-green-600` |
| `hover:bg-blue-600` | `hover:bg-green-600` |
| `border-blue-100` | `border-green-100` |
| `from-blue-600` | `from-green-600` |
| `to-blue-400` | `to-green-400` |

**Example: Changing the button color**

```html
<!-- BEFORE (Blue) -->
<button class="bg-blue-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-blue-700">
    Explore Now
</button>

<!-- AFTER (Green) -->
<button class="bg-green-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-green-700">
    Explore Now
</button>
```

### Changing the Primary Color (Blue to Purple)

Replace blue with purple equivalents:

| Blue | Purple |
|------|--------|
| `bg-blue-600` | `bg-purple-600` |
| `bg-blue-700` | `bg-purple-700` |
| `text-blue-600` | `text-purple-600` |

### Changing the Primary Color (Blue to Red)

Replace blue with red equivalents:

| Blue | Red |
|------|-----|
| `bg-blue-600` | `bg-red-600` |
| `bg-blue-700` | `bg-red-700` |
| `text-blue-600` | `text-red-600` |

### Changing Background Colors

**Current light section backgrounds:**
```html
<section class="py-16 md:py-24 bg-white">
```

**To make it light gray:**
```html
<section class="py-16 md:py-24 bg-gray-50">
```

**Color options:**
- `bg-white` - Pure white
- `bg-gray-50` - Very light gray
- `bg-gray-100` - Light gray
- `bg-blue-50` - Light blue tint
- `bg-slate-50` - Light slate tint

### Changing Text Colors

**For main headings (currently dark):**
```html
<!-- BEFORE -->
<h1 class="text-4xl md:text-6xl font-bold text-slate-900">Headline</h1>

<!-- AFTER (Lighter) -->
<h1 class="text-4xl md:text-6xl font-bold text-gray-800">Headline</h1>
```

**For body text (currently medium gray):**
```html
<!-- BEFORE -->
<p class="text-gray-600">Your text here</p>

<!-- AFTER (Darker) -->
<p class="text-gray-700">Your text here</p>

<!-- AFTER (Lighter) -->
<p class="text-gray-500">Your text here</p>
```

### Changing the Gradient Overlay

**Current hero overlay (semi-transparent dark):**
```html
<div class="hero-overlay absolute inset-0"></div>
```

**In the CSS section, find:**
```css
.hero-overlay {
    background: linear-gradient(135deg, rgba(0, 0, 0, 0.4) 0%, rgba(0, 0, 0, 0.2) 100%);
}
```

**To make it lighter:**
```css
.hero-overlay {
    background: linear-gradient(135deg, rgba(0, 0, 0, 0.2) 0%, rgba(0, 0, 0, 0.1) 100%);
}
```

**To make it darker:**
```css
.hero-overlay {
    background: linear-gradient(135deg, rgba(0, 0, 0, 0.6) 0%, rgba(0, 0, 0, 0.4) 100%);
}
```

**To make it blue-tinted:**
```css
.hero-overlay {
    background: linear-gradient(135deg, rgba(0, 0, 100, 0.4) 0%, rgba(0, 0, 100, 0.2) 100%);
}
```

### Changing the Logo Icon Background

**Current (Blue gradient):**
```html
<div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-400 rounded-lg flex items-center justify-center">
    <i class="fas fa-snowflake text-white text-lg"></i>
</div>
```

**To make it solid green:**
```html
<div class="w-10 h-10 bg-green-600 rounded-lg flex items-center justify-center">
    <i class="fas fa-snowflake text-white text-lg"></i>
</div>
```

**To make it purple gradient:**
```html
<div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-purple-400 rounded-lg flex items-center justify-center">
    <i class="fas fa-snowflake text-white text-lg"></i>
</div>
```

### Changing Feature Card Styling

**Current (White background with border):**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl">
```

**To add colored background:**
```html
<div class="feature-card bg-blue-50 border border-blue-200 rounded-xl p-8 hover:shadow-xl">
```

**To remove border and add shadow:**
```html
<div class="feature-card bg-white shadow-md rounded-xl p-8 hover:shadow-xl">
```

### Complete Color Replacement Example

**Scenario: Change entire site from blue to teal**

1. **Find all blue classes:**
```
bg-blue-600
bg-blue-700
bg-blue-400
text-blue-600
hover:bg-blue-600
hover:text-blue-600
border-blue-100
from-blue-600
to-blue-400
```

2. **Replace with teal equivalents:**
```
bg-teal-600
bg-teal-700
bg-teal-400
text-teal-600
hover:bg-teal-600
hover:text-teal-600
border-teal-100
from-teal-600
to-teal-400
```

3. **Use Find & Replace** in your editor (Ctrl+H or Cmd+H):
   - Find: `blue-600`
   - Replace with: `teal-600`
   - Click "Replace All"

4. **Repeat for:** `blue-700`, `blue-400`, `blue-100`

---

## Best Practices

### 1. Always Back Up Before Making Changes

**Create a backup:**
```
your-project-folder/
├── index.html
├── index.html.backup          ← Copy of original
├── privacy.html
└── terms.html
```

### 2. Test Changes on Multiple Devices

- Desktop (1920px wide)
- Tablet (768px wide)
- Mobile (375px wide)

Use your browser's developer tools (F12 or Cmd+Option+I) to test responsive design.

### 3. Keep Consistent Naming

When adding new sections or pages:
- Use lowercase filenames: `blog.html`, not `Blog.html`
- Use hyphens for multi-word names: `about-us.html`, not `aboutus.html`
- Keep filenames short and descriptive

### 4. Maintain Consistent Spacing

Use Tailwind's spacing scale consistently:
- `py-16` for section padding (mobile)
- `md:py-24` for section padding (desktop)
- `gap-8` for grid gaps
- `mb-6` for bottom margins

### 5. Test All Links Regularly

Create a checklist:
- [ ] All navigation links work
- [ ] All footer links work
- [ ] Email links open email client
- [ ] Social media links go to correct profiles
- [ ] Policy pages are accessible

### 6. Use Semantic HTML

- Use `<header>` for header
- Use `<nav>` for navigation
- Use `<section>` for major sections
- Use `<footer>` for footer
- Use `<button>` for clickable elements
- Use `<a>` for links

### 7. Keep Accessibility in Mind

- Always include `alt` text for images
- Use proper heading hierarchy (h1, h2, h3)
- Ensure sufficient color contrast
- Make buttons keyboard accessible

### 8. Document Your Changes

Keep a changelog:

```
## Version History

### v1.1 (March 2024)
- Changed primary color from blue to green
- Updated hero image
- Added blog link to navigation
- Fixed broken social media links

### v1.0 (January 2024)
- Initial launch
```

---

## Troubleshooting

### Common Issues and Solutions

#### Issue 1: Links Not Working

**Symptoms:** Clicking a link does nothing or shows 404 error

**Solutions:**
1. Check the filename matches exactly (case-sensitive)
2. Verify file is in the same folder as `index.html`
3. Check `href` attribute for typos
4. Use browser console (F12) to see error messages

**Example fix:**
```html
<!-- WRONG -->
<a href="Privacy.html">Privacy</a>

<!-- RIGHT -->
<a href="privacy.html">Privacy</a>
```

#### Issue 2: Styling Looks Wrong

**Symptoms:** Colors are wrong, spacing is off, layout is broken

**Solutions:**
1. Clear browser cache (Ctrl+Shift+Delete)
2. Check that Tailwind CSS is loading from CDN
3. Verify class names are spelled correctly
4. Use browser developer tools to inspect elements (F12)

**Check CDN is loading:**
```html
<!-- Make sure this line is present -->
<script src="https://cdn.tailwindcss.com"></script>
```

#### Issue 3: Mobile Menu Not Working

**Symptoms:** Hamburger menu doesn't open on mobile

**Solutions:**
1. Check JavaScript is not disabled
2. Verify the `mobile-menu-button` class exists
3. Check browser console for errors (F12)
4. Test in different browser

**Verify JavaScript section exists:**
```html
<script>
    document.querySelector('.mobile-menu-button').addEventListener('click', function() {
        const menu = document.querySelector('.mobile-menu');
        menu.classList.toggle('active');
    });
</script>
```

#### Issue 4: FAQ Accordion Not Expanding

**Symptoms:** FAQ items don't expand when clicked

**Solutions:**
1. Check `onclick="toggleFAQ(this)"` attribute exists
2. Verify JavaScript function is present
3. Check browser console for errors (F12)

**Verify FAQ function exists:**
```javascript
function toggleFAQ(button) {
    const content = button.nextElementSibling;
    const icon = button.querySelector('i');
    
    document.querySelectorAll('.faq-content.active').forEach(item => {
        if (item !== content) {
            item.classList.remove('active');
            item.previousElementSibling.querySelector('i').style.transform = 'rotate(0deg)';
        }
    });
    
    content.classList.toggle('active');
    icon.style.transform = content.classList.contains('active') ? 'rotate(180deg)' : 'rotate(0deg)';
}
```

#### Issue 5: Images Not Displaying

**Symptoms:** Broken image icons appear instead of images

**Solutions:**
1. Check image URL is correct
2. Verify external URLs are still valid
3. Check image file exists if using local images
4. Check image path is correct

**Example fix:**
```html
<!-- WRONG (URL might be broken) -->
<img src="https://images.unsplash.com/photo-1234567890?w=1600&h=900&fit=crop&q=80" alt="Image">

<!-- RIGHT (Use valid URL) -->
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" alt="Cold Plunge">
```

#### Issue 6: Sticky Header Not Sticking

**Symptoms:** Header scrolls away with page

**Solutions:**
1. Check `sticky top-0 z-50` classes are present
2. Check `z-50` isn't being overridden
3. Test in different browser

**Verify header has correct classes:**
```html
<header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
```

#### Issue 7: Smooth Scrolling Not Working

**Symptoms:** Clicking nav links jumps instantly instead of smooth scroll

**Solutions:**
1. Check CSS `scroll-behavior: smooth;` is present
2. Check browser supports smooth scroll (most modern browsers do)
3. Test in different browser

**Verify CSS is present:**
```css
html {
    scroll-behavior: smooth;
}
```

#### Issue 8: Contact Form Not Submitting

**Symptoms:** Clicking "Send Message" does nothing

**Solutions:**
1. Currently, the form has no backend - it won't actually send
2. To make it work, you need a backend service or email service
3. Popular options: Formspree, EmailJS, or your own backend

**To use Formspree (easiest):**

1. Go to https://formspree.io
2. Sign up and create a new form
3. Get your form ID
4. Update the form in your HTML:

```html
<!-- BEFORE (doesn't send) -->
<form class="space-y-4">

<!-- AFTER (uses Formspree) -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-4">
```

#### Issue 9: Colors Not Changing

**Symptoms:** Changed color class but color didn't change

**Solutions:**
1. Clear browser cache (Ctrl+Shift+Delete)
2. Make sure you saved the file
3. Refresh page (F5 or Cmd+R)
4. Check you changed the right element
5. Verify Tailwind class name is correct

**Verify Tailwind class syntax:**
```html
<!-- WRONG -->
<button class="bg-blue600">  <!-- Missing hyphen -->

<!-- RIGHT -->
<button class="bg-blue-600">  <!-- Has hyphen -->
```

#### Issue 10: Website Looks Different on Different Browsers

**Symptoms:** Layout or styling looks different in Chrome vs Firefox vs Safari

**Solutions:**
1. Use browser developer tools to debug
2. Test in multiple browsers
3. Use Tailwind classes (they're cross-browser compatible)
4. Avoid custom CSS that might not be supported

**Test in:**
- Chrome
- Firefox
- Safari
- Edge

### Getting Help

If you encounter issues:

1. **Check the browser console** (F12 → Console tab)
2. **Look for error messages** - they often tell you what's wrong
3. **Search the error message** on Google or Stack Overflow
4. **Check Tailwind documentation** - https://tailwindcss.com/docs
5. **Validate your HTML** - https://validator.w3.org/

---

## Frequently Asked Questions

### Q: Can I change the fonts?

**A:** Yes! The current font stack is system fonts. To use a custom font like Google Fonts:

1. Add this to the `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
```

2. Add this to the CSS:
```css
body {
    font-family: 'Poppins', sans-serif;
}
```

### Q: How do I add more testimonials?

**A:** Copy an existing testimonial card and paste it in the testimonials section:

```html
<!-- Copy this entire div -->
<div class="testimonial-card bg-white rounded-xl p-8 border border-gray-200 hover:shadow-xl">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Your testimonial text here"
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-slate-900">Customer Name</p>
        <p class="text-sm text-gray-600">Job Title</p>
    </div>
</div>
```

### Q: How do I add more features?

**A:** Copy an existing feature card:

```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl">
    <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-50 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-icon-name text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-slate-900 mb-3">Feature Title</h3>
    <p class="text-gray-600 leading-relaxed">
        Feature description here
    </p>
</div>
```

### Q: How do I add more FAQ items?

**A:** Copy an existing FAQ item:

```html
<div class="faq-item bg-gray-50 rounded-lg border border-gray-200 overflow-hidden">
    <button class="faq-button w-full flex items-center justify-between p-6 hover:bg-gray-100 transition-colors duration-300" onclick="toggleFAQ(this)">
        <span class="text-lg font-semibold text-slate-900 text-left">Your question here?</span>
        <i class="fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-content">
        <div class="px-6 pb-6 text-gray-700 leading-relaxed border-t border-gray-200">
            <p class="mb-3">Your answer here</p>
        </div>
    </div>
</div>
```

### Q: Can I change the hero image?

**A:** Yes! Find this line and replace the URL:

```html
<!-- BEFORE -->
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" alt="Cold Plunge Experience">

<!-- AFTER -->
<img src="your-new-image-url.jpg" alt="Your alt text">
```

### Q: How do I add a new section?

**A:** Follow this template:

```html
<section id="your-section-id" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12 md:mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-slate-900 mb-4">Section Title</h2>
            <p class="text-lg text-gray-600 max-w-2xl mx-auto">Section description</p>
        </div>
        
        <!-- Your content here -->
    </div>
</section>
```

Then add a link to it in the navigation:
```html
<a href="#your-section-id">Your Section</a>
```

### Q: Can I remove a section?

**A:** Yes! Find the entire `<section>` and delete it. Also remove the navigation link to it.

### Q: How do I deploy this to the internet?

**A:** You need web hosting. Popular options:
- Netlify (free tier available)
- Vercel (free tier available)
- GitHub Pages (free)
- Traditional hosting (GoDaddy, Bluehost, etc.)

All of these accept HTML files.

---

## Summary

You now have a comprehensive guide for maintaining and customizing your ColdPlunge landing page. Here's what you learned:

✅ **Updating Text** - How to change headings, descriptions, and content
✅ **Modifying Tailwind CSS** - How to adjust colors, spacing, and styling
✅ **Fixing Links** - How to update navigation and external links
✅ **Creating Policy Pages** - How to add privacy and terms pages
✅ **Customizing Colors** - How to change the entire color scheme
✅ **Best Practices** - How to maintain quality and consistency
✅ **Troubleshooting** - How to fix common issues

**Next Steps:**
1. Back up your files
2. Make one small change and test it
3. Gradually customize to your brand
4. Test on mobile and desktop
5. Deploy to the internet

Good luck with your ColdPlunge landing page!