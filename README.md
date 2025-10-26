# Cowtown Custom Cabinets Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Cowtown Custom Cabinets landing page. This document is designed for beginners with little to no prior web development experience.

---

## Table of Contents

1. [Overview & File Structure](#overview--file-structure)
2. [Part 1: Updating Text and Tailwind CSS Classes](#part-1-updating-text-and-tailwind-css-classes)
3. [Part 2: Fixing Broken Links](#part-2-fixing-broken-links)
4. [Part 3: Linking Privacy and Terms Pages](#part-3-linking-privacy-and-terms-pages)
5. [Common Issues & Troubleshooting](#common-issues--troubleshooting)
6. [Best Practices](#best-practices)

---

## Overview & File Structure

### What You're Working With

The Cowtown Custom Cabinets landing page is a single-page website built with:

- **HTML**: The structure and content of the page
- **Tailwind CSS**: A utility-first CSS framework that handles styling (colors, spacing, layouts)
- **Font Awesome**: An icon library for visual elements
- **Vanilla JavaScript**: Minimal code for interactive features (mobile menu, FAQ accordion)

### File Organization

Your project should have this basic structure:

```
project-folder/
├── index.html          (Main landing page - what we're editing)
├── privacy.html        (Privacy Policy page - to be created/linked)
├── terms.html          (Terms of Service page - to be created/linked)
├── blog.html           (Blog page - optional)
└── assets/             (Optional: for images, custom CSS, etc.)
    └── images/
```

### How the Page is Organized

The `index.html` file contains these main sections (in order from top to bottom):

1. **Header Navigation** - Menu and logo at the top
2. **Hero Section** - Large welcome banner with call-to-action buttons
3. **Features Section** - Three service cards (Kitchen, Bathroom, Custom Cabinets)
4. **Benefits Section** - Why choose Cowtown with icons and stats
5. **About Section** - Company history and statistics
6. **Testimonials Section** - Customer reviews
7. **CTA Section** - Call-to-action banner
8. **FAQ Section** - Frequently asked questions with accordion
9. **Footer** - Contact info, links, and legal pages

---

## Part 1: Updating Text and Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses **utility classes** - short class names that apply specific styling. Instead of writing custom CSS, you combine multiple classes to style elements.

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white">
```

This means:
- `text-4xl` = Large text size (mobile)
- `md:text-5xl` = Larger text on medium screens
- `lg:text-6xl` = Even larger text on large screens
- `font-bold` = Bold text
- `text-white` = White text color

**Key Concept:** Responsive design classes use prefixes like `md:` and `lg:` to apply styles at different screen sizes.

### Locating Sections to Edit

#### 1. **Header/Navigation Text**

**Location:** Lines 85-110 (approximately)

**What to Update:**
- Company name "Cowtown"
- Navigation menu items
- Get Started button link

**How to Find It:**
Search for `<header class="sticky top-0">` in your text editor (Ctrl+F or Cmd+F)

**Example - Current Code:**
```html
<span class="text-2xl font-bold text-gray-900">Cowtown</span>
```

**To Change:** Replace `Cowtown` with your company name

```html
<span class="text-2xl font-bold text-gray-900">Your Company Name</span>
```

**Navigation Menu Items - Current:**
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Benefits</a>
```

**To Change:** Replace the text between `>` and `</a>` tags

```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Your New Label</a>
```

---

#### 2. **Hero Section (Main Banner)**

**Location:** Lines 139-170 (approximately)

**What to Update:**
- Main headline
- Subtitle/description
- Button text and links

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6 animate-fade-in">
    Cowtown Custom Cabinets
</h1>
```

**To Change the Headline:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6 animate-fade-in">
    Your New Headline Here
</h1>
```

**Current Subtitle:**
```html
<p class="text-xl md:text-2xl text-blue-100 mb-8 max-w-3xl mx-auto leading-relaxed">
    At Cowtown, we specialize in custom cabinets that transform your space...
</p>
```

**To Change:** Replace the paragraph text (keep the opening `<p>` tag and closing `</p>` tag)

```html
<p class="text-xl md:text-2xl text-blue-100 mb-8 max-w-3xl mx-auto leading-relaxed">
    Your new subtitle text goes here. Keep it compelling and customer-focused.
</p>
```

**Tailwind Classes Explained:**
- `text-xl` = Extra large text
- `text-blue-100` = Light blue text color
- `mb-8` = Margin (space) below the element
- `max-w-3xl` = Maximum width of the element
- `mx-auto` = Center the element horizontally
- `leading-relaxed` = Extra space between lines

---

#### 3. **Features Section (Service Cards)**

**Location:** Lines 185-245 (approximately)

**What to Update:**
- Section heading and description
- Individual feature card titles, descriptions, and bullet points
- Feature icons

**Current Code - Section Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Our Premium Services
</h2>
```

**To Change:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Your New Section Title
</h2>
```

**Current Code - Feature Card Example (First Card):**
```html
<div class="feature-card card-hover bg-white rounded-xl shadow-md p-8 border border-gray-100">
    <div class="feature-icon text-blue-600 mb-4">
        <i class="fas fa-kitchen"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">Custom Kitchen Cabinets</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Transform your kitchen with our bespoke cabinet designs...
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i>Custom sizing and layouts</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i>Premium hardware options</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i>Multiple finish choices</li>
    </ul>
</div>
```

**To Update the Card Title:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Your New Service Title</h3>
```

**To Update the Card Description:**
```html
<p class="text-gray-600 leading-relaxed mb-4">
    Your new description text goes here. Describe your service clearly and compellingly.
</p>
```

**To Update Bullet Points:**
Replace each `<li>` item:
```html
<li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i>Your new bullet point text</li>
```

**To Change the Icon:**
Replace the icon class. Find available icons at [Font Awesome Icons](https://fontawesome.com/icons). Common examples:
- `fa-kitchen` → Kitchen icon
- `fa-bath` → Bathroom icon
- `fa-paint-brush` → Design icon
- `fa-star` → Star icon
- `fa-hammer` → Tools icon

**Tailwind Classes in Cards:**
- `bg-white` = White background
- `rounded-xl` = Rounded corners (extra rounded)
- `shadow-md` = Medium drop shadow
- `p-8` = Padding (internal spacing) of 8 units
- `border border-gray-100` = Light gray border
- `text-blue-600` = Blue text
- `mb-3` = Margin bottom (space below)

---

#### 4. **Benefits Section**

**Location:** Lines 250-320 (approximately)

**What to Update:**
- Section heading
- Benefit titles and descriptions
- Commitment box text and bullet points
- Stats (Years, Projects, Satisfaction, Team Members)

**Current Code - Section Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Why Choose Cowtown Custom Cabinets
</h2>
```

**To Change:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Why Choose Your Company Name
</h2>
```

**Current Code - Individual Benefit:**
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-12 w-12 rounded-md bg-blue-600 text-white">
            <i class="fas fa-pencil-ruler text-lg"></i>
        </div>
    </div>
    <div>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Expert Design Consultation</h3>
        <p class="text-gray-600 leading-relaxed">
            Our talented designers work closely with you...
        </p>
    </div>
</div>
```

**To Update the Benefit Title:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-2">Your New Benefit Title</h3>
```

**To Update the Benefit Description:**
```html
<p class="text-gray-600 leading-relaxed">
    Your new benefit description goes here.
</p>
```

**To Change the Icon:**
Replace `fa-pencil-ruler` with another Font Awesome icon, such as:
- `fa-pencil-ruler` → Design/measurement
- `fa-wrench` → Tools/fabrication
- `fa-tools` → Installation
- `fa-lightbulb` → Ideas
- `fa-check` → Checkmark

**Current Code - Commitment Box (Right Side):**
```html
<div class="bg-gradient-to-br from-blue-600 to-purple-600 rounded-2xl shadow-xl p-8 text-white">
    <h3 class="text-3xl font-bold mb-6">Our Commitment to Excellence</h3>
    <ul class="space-y-4 mb-8">
        <li class="flex items-start gap-3">
            <i class="fas fa-star text-yellow-300 mt-1"></i>
            <span>Premium quality materials sourced from trusted suppliers</span>
        </li>
        <!-- More list items -->
    </ul>
</div>
```

**To Update the Box Title:**
```html
<h3 class="text-3xl font-bold mb-6">Your New Commitment Title</h3>
```

**To Update Commitment List Items:**
```html
<li class="flex items-start gap-3">
    <i class="fas fa-star text-yellow-300 mt-1"></i>
    <span>Your new commitment point goes here</span>
</li>
```

---

#### 5. **About Section**

**Location:** Lines 325-390 (approximately)

**What to Update:**
- Section heading
- Company description paragraphs
- Statistics (Years, Projects, Satisfaction, Team)

**Current Code - Section Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Cowtown Custom Cabinets
</h2>
```

**To Change:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Your Company Name
</h2>
```

**Current Code - Description Paragraph:**
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Founded in 2008, Cowtown Custom Cabinets began as a small family-owned business...
</p>
```

**To Change:**
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Your company history and description goes here. Make it engaging and authentic.
</p>
```

**Current Code - Statistics Cards:**
```html
<div class="bg-white rounded-xl shadow-lg p-8 text-center card-hover">
    <div class="text-4xl font-bold text-blue-600 mb-2">15+</div>
    <p class="text-gray-600 font-semibold">Years of Experience</p>
</div>
```

**To Update Statistics:**
```html
<div class="bg-white rounded-xl shadow-lg p-8 text-center card-hover">
    <div class="text-4xl font-bold text-blue-600 mb-2">20+</div>
    <p class="text-gray-600 font-semibold">Your Statistic Label</p>
</div>
```

**Tailwind Classes for Stats:**
- `text-4xl` = Very large number
- `font-bold` = Bold text
- `text-blue-600` = Blue color (change to `text-purple-600`, `text-green-600`, etc.)
- `text-center` = Center alignment

---

#### 6. **Testimonials Section**

**Location:** Lines 395-460 (approximately)

**What to Update:**
- Section heading and description
- Individual testimonial quotes, names, and titles

**Current Code - Section Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    What Our Clients Say
</h2>
```

**To Change:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Your New Testimonial Heading
</h2>
```

**Current Code - Individual Testimonial:**
```html
<div class="card-hover bg-white rounded-xl shadow-md border border-gray-100 p-8">
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed">
        "The team at Cowtown completely transformed our kitchen!..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-sm text-gray-600">Homeowner, Arlington TX</p>
    </div>
</div>
```

**To Update the Quote:**
```html
<p class="text-gray-700 mb-6 leading-relaxed">
    "Your customer testimonial goes here. Include specific details about the project."
</p>
```

**To Update the Customer Name:**
```html
<p class="font-bold text-gray-900">Your Customer Name</p>
```

**To Update the Customer Title:**
```html
<p class="text-sm text-gray-600">Their role or location</p>
```

**To Adjust Star Rating:** Add or remove star icons (`<i class="fas fa-star text-yellow-400"></i>`) to show 1-5 stars.

---

#### 7. **CTA Section (Call-to-Action Banner)**

**Location:** Lines 465-490 (approximately)

**What to Update:**
- Heading
- Description text
- Button text and links

**Current Code:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-6 tracking-tight">
    Ready to Transform Your Space?
</h2>
<p class="text-xl text-blue-100 mb-8 max-w-2xl mx-auto leading-relaxed">
    Let our expert team create custom cabinets that perfectly match your vision...
</p>
```

**To Change the Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-6 tracking-tight">
    Your New CTA Heading
</h2>
```

**To Change the Description:**
```html
<p class="text-xl text-blue-100 mb-8 max-w-2xl mx-auto leading-relaxed">
    Your new call-to-action description.
</p>
```

---

#### 8. **FAQ Section**

**Location:** Lines 495-580 (approximately)

**What to Update:**
- Section heading
- FAQ questions and answers

**Current Code - Section Heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Frequently Asked Questions
</h2>
```

**To Change:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Your New FAQ Heading
</h2>
```

**Current Code - FAQ Item:**
```html
<div class="faq-item bg-white rounded-xl shadow-md border border-gray-100 overflow-hidden">
    <button class="faq-question w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-bold text-gray-900">How long does the custom cabinet design and fabrication process take?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-8 pb-6 text-gray-700 border-t border-gray-100 pt-6 leading-relaxed">
        <p>The timeline for our custom cabinet projects typically ranges from 4 to 8 weeks...</p>
    </div>
</div>
```

**To Update the Question:**
Replace the text in the `<span>` tag:
```html
<span class="text-lg font-bold text-gray-900">Your new FAQ question?</span>
```

**To Update the Answer:**
Replace the text in the `<p>` tag inside the `.faq-answer` div:
```html
<p>Your detailed answer goes here. You can include multiple paragraphs if needed.</p>
```

**Adding Multiple Paragraphs to an Answer:**
```html
<div class="faq-answer hidden px-8 pb-6 text-gray-700 border-t border-gray-100 pt-6 leading-relaxed">
    <p>First paragraph of your answer.</p>
    <p>Second paragraph of your answer.</p>
</div>
```

---

#### 9. **Footer**

**Location:** Lines 585-650 (approximately)

**What to Update:**
- Company description
- Footer links
- Contact information
- Copyright year

**Current Code - Company Info:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Premium custom cabinets and design solutions for homes and businesses throughout North Texas.
</p>
```

**To Change:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Your company description for the footer.
</p>
```

**Current Code - Footer Links:**
```html
<h4 class="text-white font-bold text-lg mb-6">Quick Links</h4>
<ul class="space-y-3">
    <li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Our Services</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Why Choose Us</a></li>
    <li><a href="#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a></li>
    <li><a href="#testimonials" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Testimonials</a></li>
    <li><a href="#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
</ul>
```

**To Update Link Text:**
```html
<li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Your New Link Text</a></li>
```

**Current Code - Contact Info:**
```html
<li class="flex items-start gap-3">
    <i class="fas fa-envelope text-blue-400 mt-1"></i>
    <a href="mailto:Cowtowndfw@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Cowtowndfw@gmail.com</a>
</li>
```

**To Update Email:**
```html
<a href="mailto:youremail@example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">youremail@example.com</a>
```

**Current Code - Copyright:**
```html
<p class="text-gray-400 text-center md:text-left">
    &copy; 2025 Cowtown Custom Cabinets. All rights reserved.
</p>
```

**To Update:**
```html
<p class="text-gray-400 text-center md:text-left">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

---

### Changing Colors with Tailwind CSS

Tailwind uses a consistent color system. Common colors and their usage:

**Text Colors:**
- `text-white` = White
- `text-gray-900` = Dark gray/black
- `text-gray-600` = Medium gray
- `text-blue-600` = Blue (primary)
- `text-purple-600` = Purple
- `text-green-500` = Green

**Background Colors:**
- `bg-white` = White background
- `bg-gray-50` = Very light gray background
- `bg-blue-600` = Blue background
- `bg-gradient-to-r from-blue-600 to-purple-600` = Gradient background

**To Change All Primary Colors:**

1. Find all instances of `text-blue-600` and replace with your color
2. Find all instances of `bg-blue-600` and replace with your color
3. Find all instances of `from-blue-600` and replace with your color

**Example - Changing from Blue to Green:**

**Before:**
```html
<a href="#" class="bg-gradient-to-r from-blue-600 to-purple-600 text-white px-6 py-2 rounded-lg">
    Get Started
</a>
```

**After:**
```html
<a href="#" class="bg-gradient-to-r from-green-600 to-teal-600 text-white px-6 py-2 rounded-lg">
    Get Started
</a>
```

---

## Part 2: Fixing Broken Links

### Understanding Links in HTML

A link is created with an `<a>` tag:
```html
<a href="https://example.com">Click here</a>
```

- `<a>` = Link tag
- `href="..."` = The destination (where the link goes)
- Text between `>` and `</a>` = What users see and click

### Types of Links on This Page

#### A. **Internal Links** (Links to sections within the same page)

These use the `#` symbol followed by a section ID.

**Example:**
```html
<a href="#features">Features</a>
```

This links to:
```html
<section id="features" class="...">
```

**Current Internal Links:**
- `href="#features"` → Links to Features section
- `href="#benefits"` → Links to Benefits section
- `href="#about"` → Links to About section
- `href="#testimonials"` → Links to Testimonials section
- `href="#faq"` → Links to FAQ section

**These are working correctly** and don't need changes unless you rename the section IDs.

#### B. **External Links** (Links to other websites)

These use full URLs starting with `http://` or `https://`

**Current External Links in the Page:**

**1. Main Website Link (Multiple Locations)**

**Locations:**
- Header "Get Started" button (Line ~115)
- Hero section buttons (Lines ~170-175)
- Benefits section button (Line ~310)
- CTA section button (Line ~485)

**Current Code:**
```html
<a href="https://cowtowncustomcabinets.net/" class="...">Get Started</a>
```

**To Fix:** Replace the URL with your actual website

```html
<a href="https://yourwebsite.com/" class="...">Get Started</a>
```

**How to Find All Instances:**
1. Open your HTML file in a text editor
2. Press Ctrl+F (Windows) or Cmd+F (Mac)
3. Search for: `cowtowncustomcabinets.net`
4. Replace each instance with your URL

**2. Email Link (Footer)**

**Location:** Line ~635

**Current Code:**
```html
<a href="mailto:Cowtowndfw@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Cowtowndfw@gmail.com</a>
```

**To Fix:** Replace with your email address

```html
<a href="mailto:youremail@example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">youremail@example.com</a>
```

**3. Social Media Links (Footer)**

**Location:** Lines ~615-625

**Current Code:**
```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**These are currently set to `#`** (placeholder links that don't go anywhere)

**To Fix - Facebook:**
```html
<a href="https://www.facebook.com/yourpage" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To Fix - Instagram:**
```html
<a href="https://www.instagram.com/yourprofile" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-instagram"></i>
</a>
```

**To Fix - Twitter:**
```html
<a href="https://www.twitter.com/yourprofile" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-twitter"></i>
</a>
```

**To Fix - LinkedIn:**
```html
<a href="https://www.linkedin.com/company/yourcompany" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-linkedin-in"></i>
</a>
```

### Step-by-Step: Fixing All Links

**Step 1:** Open `index.html` in your text editor

**Step 2:** Use Find & Replace (Ctrl+H or Cmd+H)

**Step 3:** For each broken link:
- **Find:** The current URL or placeholder
- **Replace with:** Your correct URL
- **Click Replace All** (or replace individually to verify)

**Step 4:** Test by opening the page in a browser and clicking each link

---

### Link Testing Checklist

After updating links, test each one:

- [ ] Header navigation links scroll to correct sections
- [ ] "Get Started" buttons link to your website
- [ ] Email link opens your email client
- [ ] Social media icons link to your profiles
- [ ] Footer links work correctly
- [ ] All links open in correct target (same tab or new tab)

---

## Part 3: Linking Privacy and Terms Pages

### Understanding the Current Setup

The footer currently has links to `privacy.html` and `terms.html`:

**Current Code (Lines ~645-650):**
```html
<div class="flex justify-center md:justify-end space-x-6">
    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
    <a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Blog</a>
</div>
```

These links are already set up, but the pages don't exist yet. Let's create them.

### Step 1: Create the Privacy Policy Page

**File Name:** `privacy.html`

**Location:** Save in the same folder as `index.html`

**Starter Code:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Cowtown Custom Cabinets">
    <title>Privacy Policy - Cowtown Custom Cabinets</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Poppins', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-purple-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-hammer text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold text-gray-900">Cowtown</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
                <a href="https://cowtowncustomcabinets.net/" class="bg-gradient-to-r from-blue-600 to-purple-600 text-white px-6 py-2 rounded-lg hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300">
                <i class="fas fa-bars text-2xl text-gray-900"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-24 lg:py-28 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p>
                    <strong>Last Updated: [Current Date]</strong>
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    Cowtown Custom Cabinets ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you provide when requesting a consultation or submitting inquiries.</li>
                    <li><strong>Device Information:</strong> Information about your device, including browser type, IP address, and pages visited.</li>
                    <li><strong>Usage Data:</strong> How you interact with our website, including pages viewed and time spent on our site.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Respond to your inquiries and provide customer service</li>
                    <li>Process your requests for consultations or quotes</li>
                    <li>Send promotional communications (with your consent)</li>
                    <li>Improve our website and services</li>
                    <li>Monitor website analytics and usage patterns</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Disclosure of Your Information</h2>
                <p>
                    We do not sell, trade, or rent your personal information to third parties. We may disclose your information only in the following circumstances:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>To service providers who assist us in operating our website and conducting our business</li>
                    <li>When required by law or legal process</li>
                    <li>To protect our rights, privacy, safety, or property</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet is 100% secure. While we strive to use commercially acceptable means to protect your personal information, we cannot guarantee its absolute security.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Contact Us</h2>
                <p>
                    If you have questions about this Privacy Policy, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:Cowtowndfw@gmail.com" class="text-blue-600 hover:text-blue-800">Cowtowndfw@gmail.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400">
                    &copy; 2025 Cowtown Custom Cabinets. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**File Name:** `terms.html`

**Location:** Save in the same folder as `index.html`

**Starter Code:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Cowtown Custom Cabinets">
    <title>Terms of Service - Cowtown Custom Cabinets</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Poppins', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-purple-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-hammer text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold text-gray-900">Cowtown</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
                <a href="https://cowtowncustomcabinets.net/" class="bg-gradient-to-r from-blue-600 to-purple-600 text-white px-6 py-2 rounded-lg hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300">
                <i class="fas fa-bars text-2xl text-gray-900"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-24 lg:py-28 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p>
                    <strong>Last Updated: [Current Date]</strong>
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Cowtown Custom Cabinets' website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>
                    The materials on Cowtown Custom Cabinets' website are provided on an 'as is' basis. Cowtown Custom Cabinets makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>
                    In no event shall Cowtown Custom Cabinets or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Cowtown Custom Cabinets' website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Cowtown Custom Cabinets' website could include technical, typographical, or photographic errors. Cowtown Custom Cabinets does not warrant that any of the materials on its website are accurate, complete, or current. Cowtown Custom Cabinets may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Links</h2>
                <p>
                    Cowtown Custom Cabinets has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Cowtown Custom Cabinets of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Modifications</h2>
                <p>
                    Cowtown Custom Cabinets may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of Texas, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">9. Contact Us</h2>
                <p>
                    If you have questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:Cowtowndfw@gmail.com" class="text-blue-600 hover:text-blue-800">Cowtowndfw@gmail.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400">
                    &copy; 2025 Cowtown Custom Cabinets. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Verify Links in index.html

The footer of `index.html` already contains the correct links. Verify they're present:

**Check for (should already exist in index.html):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
```

If these links are missing, add them to the footer section (around line 645).

### Step 4: Test the Links

1. **Save all three files** in the same folder:
   - `index.html`
   - `privacy.html`
   - `terms.html`

2. **Open `index.html`** in your web browser

3. **Scroll to the footer** and click on:
   - "Privacy Policy" → Should open `privacy.html`
   - "Terms of Service" → Should open `terms.html`

4. **From the policy pages**, click the logo or "Home" link to return to `index.html`

### Step 5: Customize the Policy Pages

**In both `privacy.html` and `terms.html`, update:**

1. **Company Name:**
   - Find: `Cowtown Custom Cabinets`
   - Replace with: Your company name

2. **Email Address:**
   - Find: `Cowtowndfw@gmail.com`
   - Replace with: Your email

3. **Jurisdiction/Location:**
   - Find: `Texas`
   - Replace with: Your state/location

4. **Last Updated Date:**
   - Find: `[Current Date]`
   - Replace with: Today's date (e.g., "January 15, 2025")

5. **Content:**
   - Review each section
   - Update any company-specific details
   - Add or remove sections as needed for your business

### Adding Links to Policy Pages from Other Locations

If you want to add links to privacy/terms pages in other locations:

**Example - Adding to Header:**
```html
<a href="privacy.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Privacy</a>
<a href="terms.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Terms</a>
```

**Example - Adding to a CTA Section:**
```html
<div class="text-center text-sm text-gray-600 mt-6">
    <a href="privacy.html" class="hover:text-blue-600 mr-4">Privacy Policy</a>
    <a href="terms.html" class="hover:text-blue-600">Terms of Service</a>
</div>
```

---

## Common Issues & Troubleshooting

### Issue 1: Links Don't Work

**Problem:** Clicking a link does nothing or shows a 404 error

**Solution:**
1. Check that the file exists in the same folder as `index.html`
2. Verify the filename matches exactly (including capitalization)
3. Check for typos in the `href` attribute
4. If linking to an external website, ensure the URL includes `http://` or `https://`

**Example - Correct:**
```html
<a href="privacy.html">Privacy Policy</a>
```

**Example - Incorrect:**
```html
<a href="Privacy.html">Privacy Policy</a>  <!-- Wrong filename -->
<a href="/privacy.html">Privacy Policy</a>  <!-- Wrong path (adds slash) -->
```

---

### Issue 2: Text Changes Don't Appear

**Problem:** You edited text in the HTML, but the website still shows old text

**Solution:**
1. Save the file (Ctrl+S or Cmd+S)
2. Refresh the browser (Ctrl+R or Cmd+R)
3. Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
4. Close and reopen the browser

---

### Issue 3: Styling Looks Broken

**Problem:** Colors, spacing, or layout looks wrong after editing

**Solution:**
1. Don't delete the class names - only change the text between tags
2. If you accidentally deleted a closing tag `</div>`, add it back
3. Check that you didn't accidentally delete an opening tag `<`

**Correct - Change text only:**
```html
<h2 class="text-3xl font-bold text-gray-900">Your New Title</h2>
```

**Incorrect - Don't remove or change classes:**
```html
<h2>Your New Title</h2>  <!-- Lost all styling! -->
```

---

### Issue 4: Mobile Menu Not Working

**Problem:** The hamburger menu doesn't open on mobile devices

**Solution:**
1. Check that JavaScript code is still present at the bottom of the file
2. Verify the `mobile-menu-button` and `mobile-menu` elements exist
3. Clear browser cache and refresh

---

### Issue 5: Colors Not Changing

**Problem:** Changed color classes but colors didn't update

**Solution:**
1. Make sure you're using valid Tailwind color classes:
   - Valid: `text-blue-600`, `bg-purple-600`, `text-green-500`
   - Invalid: `text-blue`, `bg-purple` (missing number)
2. Replace ALL instances of the color, not just one
3. Refresh the browser cache

---

### Issue 6: External Links Open in Same Tab

**Problem:** Links to external websites replace your page instead of opening in new tab

**Solution:** Add `target="_blank"` to the link

**Before:**
```html
<a href="https://example.com">Visit Site</a>
```

**After:**
```html
<a href="https://example.com" target="_blank">Visit Site</a>
```

---

### Issue 7: Email Link Not Working

**Problem:** Clicking email link doesn't open email client

**Solution:**
1. Verify the email link uses `mailto:` prefix
2. Check for typos in the email address
3. Make sure the user has an email client configured on their device

**Correct Format:**
```html
<a href="mailto:youremail@example.com">Send Email</a>
```

---

## Best Practices

### 1. **Always Make Backups**

Before making major changes:
1. Create a copy of the file (e.g., `index_backup.html`)
2. Save it in a separate folder
3. If something breaks, you can restore from backup

---

### 2. **Edit One Section at a Time**

Don't edit multiple sections at once. Instead:
1. Edit one section
2. Save and test in browser
3. If it works, move to next section
4. If it breaks, undo changes and troubleshoot

---

### 3. **Keep Tag Structure Intact**

Always maintain matching opening and closing tags:

**Correct:**
```html
<div class="...">
    <h2 class="...">Title</h2>
    <p class="...">Content</p>
</div>
```

**Incorrect (Missing closing tag):**
```html
<div class="...">
    <h2 class="...">Title</h2>
    <p class="...">Content
</div>
```

---

### 4. **Use a Proper Code Editor**

Recommended free code editors:
- **Visual Studio Code** (most popular)
- **Notepad++** (Windows)
- **Sublime Text** (all platforms)
- **Atom** (all platforms)

Avoid:
- Microsoft Word (adds hidden formatting)
- Notepad (lacks helpful features)
- Google Docs (not designed for code)

---

### 5. **Test Changes Immediately**

After each edit:
1. Save the file
2. Refresh the browser
3. Check that it looks correct
4. Test any links or interactive elements

---

### 6. **Comment Your Changes**

Add HTML comments to mark your edits:

```html
<!-- CUSTOM EDIT: Updated company name -->
<h1 class="text-4xl font-bold">Your Company Name</h1>

<!-- CUSTOM EDIT: Added new feature card -->
<div class="feature-card">
    ...
</div>
```

---

### 7. **Maintain Consistent Formatting**

Keep indentation consistent for readability:

```html
<!-- Good indentation -->
<div class="container">
    <h2 class="title">Heading</h2>
    <p class="content">Content</p>
</div>

<!-- Poor indentation (harder to read) -->
<div class="container">
<h2 class="title">Heading</h2>
<p class="content">Content</p>
</div>
```

---

### 8. **Update All Instances**

When changing something that appears multiple times (like company name or email):
1. Use Find & Replace (Ctrl+H or Cmd+H)
2. Search for the old value
3. Replace with new value
4. Click "Replace All"
5. Verify the changes

---

### 9. **Responsive Design Considerations**

When editing text, keep responsive design in mind:
- Short text works better on mobile
- Long text may break layouts
- Test on different screen sizes

**Test your page at different sizes:**
1. Full desktop (1920px)
2. Tablet (768px)
3. Mobile (375px)

In most browsers, press F12 to open Developer Tools and test responsive design.

---

### 10. **SEO Best Practices**

When updating content, remember SEO:

**Update Meta Tags:**
```html
<meta name="description" content="Your new page description - 150 characters max">
<meta name="keywords" content="keyword1, keyword2, keyword3">
<title>Your Page Title - 50-60 characters max</title>
```

**Use Descriptive Headings:**
- Use `<h1>` for main page title (only once)
- Use `<h2>` for section headings
- Use `<h3>` for subsections

---

## Advanced: Custom CSS

If you need to add custom styling beyond Tailwind classes:

**Location:** Add custom CSS in the `<style>` tag (around line 18-40)

**Example - Adding a custom hover effect:**
```css
.custom-button:hover {
    background-color: #ff6b6b;
    transform: scale(1.1);
    transition: all 0.3s ease;
}
```

**Then use it in HTML:**
```html
<button class="custom-button px-6 py-2 rounded-lg">Click Me</button>
```

---

## Summary

### Quick Reference - Key Locations to Edit

| Section | Line Range | What to Edit |
|---------|-----------|--------------|
| Header Logo | ~90 | Company name |
| Hero Title | ~145 | Main headline |
| Hero Description | ~149 | Subtitle |
| Features Heading | ~189 | Section title |
| Feature Cards | ~200-245 | Service titles, descriptions, icons |
| Benefits Section | ~265-310 | Benefit titles, descriptions, stats |
| About Section | ~350-380 | Company history, statistics |
| Testimonials | ~410-455 | Customer quotes, names, titles |
| FAQ | ~510-575 | Questions and answers |
| Footer | ~600-650 | Contact info, links, copyright |

### Quick Reference - Common Tailwind Classes

| Purpose | Class | Example |
|---------|-------|---------|
| Text Size | `text-lg`, `text-xl`, `text-2xl` | `<h2 class="text-2xl">` |
| Text Color | `text-blue-600`, `text-gray-900` | `<p class="text-gray-900">` |
| Background | `bg-white`, `bg-gray-50` | `<div class="bg-white">` |
| Spacing | `mb-4`, `p-8`, `px-6` | `<div class="mb-4 p-8">` |
| Responsive | `md:text-4xl`, `lg:text-5xl` | `<h1 class="text-2xl md:text-4xl">` |
| Hover | `hover:text-blue-600` | `<a class="hover:text-blue-600">` |

---

## Getting Help

If you get stuck:

1. **Check the browser console** (F12) for error messages
2. **Validate HTML** at [W3C Validator](https://validator.w3.org/)
3. **Review Tailwind documentation** at [tailwindcss.com](https://tailwindcss.com/docs)
4. **Check Font Awesome icons** at [fontawesome.com/icons](https://fontawesome.com/icons)
5. **Search for specific issues** on Stack Overflow or Google

---

## Conclusion

You now have a comprehensive understanding of how to maintain and customize the Cowtown Custom Cabinets landing page. Remember to:

- Make backups before major changes
- Test changes immediately
- Keep tag structure intact
- Update all instances of repeated content
- Maintain responsive design principles

Happy editing! 🎉