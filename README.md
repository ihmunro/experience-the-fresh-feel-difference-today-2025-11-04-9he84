# Fresh Feel Painting & Cleaning Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Colors & Styling](#modifying-colors--styling)
5. [Fixing & Managing Links](#fixing--managing-links)
6. [Adding Privacy & Terms Pages](#adding-privacy--terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting](#troubleshooting)

---

## Overview

This landing page is built with **HTML**, **Tailwind CSS**, and **Font Awesome icons**. It uses a single `index.html` file with embedded CSS and JavaScript. The page is fully responsive and includes:

- Sticky navigation header
- Hero section with call-to-action buttons
- Features showcase (3 columns)
- Benefits section
- Client testimonials (4 cards)
- About section
- FAQ accordion
- Call-to-action banner
- Footer with links and contact info

**Key Technologies:**
- **HTML5**: Page structure
- **Tailwind CSS 2.2.19**: Styling and responsive design (via CDN)
- **Font Awesome 6.4.0**: Icons (via CDN)
- **Vanilla JavaScript**: Interactive features (mobile menu, FAQ accordion)

---

## File Structure

```
project-root/
├── index.html (main landing page)
├── privacy.html (to be created)
├── terms.html (to be created)
└── blog.html (referenced but optional)
```

All files should be in the same directory for links to work correctly.

---

## Updating Text Content

### 1. Page Title & Meta Description

**Location:** Lines 5-7 in the `<head>` section

```html
<title>Fresh Feel Painting & Cleaning - Professional Painting and Cleaning Services</title>
<meta name="description" content="Transform your space with Fresh Feel Painting & Cleaning. Expert painting and meticulous cleaning services for a fresher, healthier environment.">
```

**How to Update:**
1. Open `index.html` in any text editor (Notepad, VS Code, etc.)
2. Find the `<title>` tag at the top
3. Replace the text between `<title>` and `</title>` with your new title
4. Find the `<meta name="description"` tag
5. Replace the `content="..."` text with your new description (keep it under 160 characters)

**Example:**
```html
<title>Your Company Name - Your Service Description</title>
<meta name="description" content="Your new description here.">
```

---

### 2. Company Name in Header

**Location:** Line 33 (Header section)

```html
<a href="#" class="text-2xl font-bold text-blue-600">Fresh Feel</a>
```

**How to Update:**
1. Find the line with `<a href="#" class="text-2xl font-bold text-blue-600">Fresh Feel</a>`
2. Replace `Fresh Feel` with your company name
3. The `text-2xl` class makes it large, `font-bold` makes it bold, and `text-blue-600` makes it blue

**Example:**
```html
<a href="#" class="text-2xl font-bold text-blue-600">Your Company Name</a>
```

---

### 3. Hero Section (Main Headline & Subtitle)

**Location:** Lines 54-56

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 tracking-tight">
  Experience the Fresh Feel Difference Today!
</h1>
<p class="text-xl md:text-2xl max-w-3xl mx-auto mb-8 leading-relaxed">
  Transform your space with our expert painting and meticulous cleaning services...
</p>
```

**How to Update:**
1. Find the `<h1>` tag (the largest heading)
2. Replace the text between `<h1>` and `</h1>` with your headline
3. Find the `<p>` tag below it
4. Replace the subtitle text

**Understanding the Classes:**
- `text-4xl md:text-5xl lg:text-6xl`: Makes text responsive (smaller on mobile, larger on desktop)
- `font-bold`: Makes text bold
- `mb-6`: Adds margin (space) below the element
- `max-w-3xl`: Limits the width so text doesn't stretch too far

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 tracking-tight">
  Your New Headline Here!
</h1>
<p class="text-xl md:text-2xl max-w-3xl mx-auto mb-8 leading-relaxed">
  Your new subtitle describing your services.
</p>
```

---

### 4. Feature Cards (What Sets Us Apart)

**Location:** Lines 70-96

Each feature card has three parts: icon, title, and description.

```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:scale-102 fade-in">
    <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-leaf"></i></div>
    <h3 class="text-2xl font-semibold mb-4">Eco-Friendly Excellence</h3>
    <p class="text-gray-600 leading-relaxed">We prioritize your health...</p>
</div>
```

**How to Update a Feature Card:**

1. **Change the Icon:**
   - Find `<i class="fas fa-leaf"></i>`
   - Visit [Font Awesome Icons](https://fontawesome.com/icons) to find a different icon
   - Replace `fa-leaf` with the new icon name (e.g., `fa-hammer` for tools)
   - Example: `<i class="fas fa-hammer"></i>`

2. **Change the Title:**
   - Find `<h3 class="text-2xl font-semibold mb-4">Eco-Friendly Excellence</h3>`
   - Replace `Eco-Friendly Excellence` with your new title

3. **Change the Description:**
   - Find the `<p class="text-gray-600 leading-relaxed">` paragraph
   - Replace the text with your new description

**Complete Example:**
```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:scale-102 fade-in">
    <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-hammer"></i></div>
    <h3 class="text-2xl font-semibold mb-4">Professional Tools</h3>
    <p class="text-gray-600 leading-relaxed">We use only the best equipment and tools...</p>
</div>
```

---

### 5. Benefits Section

**Location:** Lines 105-135

Similar to features, but with different styling (blue background: `bg-blue-50`).

```html
<div class="bg-blue-50 p-8 rounded-xl hover:shadow-md transition-all duration-300 fade-in">
    <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-wind"></i></div>
    <h3 class="text-2xl font-semibold mb-4">Fresher, Healthier Environment</h3>
    <p class="text-gray-600 leading-relaxed">Breathe easier...</p>
</div>
```

**How to Update:**
Follow the same process as feature cards:
1. Change icon (find `fas fa-wind`, replace with new icon)
2. Change title (h3 text)
3. Change description (p text)

---

### 6. Testimonials Section

**Location:** Lines 155-195

Each testimonial card contains: star rating, quote, customer name, and title.

```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 fade-in">
    <div class="flex items-center mb-4">
        <div class="text-yellow-400 mr-1">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-600 mb-4 italic">"Fresh Feel transformed our office..."</p>
    <div class="font-semibold">Sarah Johnson</div>
    <div class="text-gray-500 text-sm">Office Manager, TechCorp Solutions</div>
</div>
```

**How to Update a Testimonial:**

1. **Change the Quote:**
   - Find the `<p class="text-gray-600 mb-4 italic">` paragraph
   - Replace the quoted text with the new testimonial
   - Keep the quotation marks

2. **Change the Customer Name:**
   - Find `<div class="font-semibold">Sarah Johnson</div>`
   - Replace `Sarah Johnson` with the real customer name

3. **Change the Customer Title:**
   - Find `<div class="text-gray-500 text-sm">Office Manager, TechCorp Solutions</div>`
   - Replace with the customer's actual title and company

3. **Adjust Star Rating (if needed):**
   - To show 4 stars instead of 5, remove one `<i class="fas fa-star"></i>` line
   - To show a half star, change one to: `<i class="fas fa-star-half-alt"></i>`

**Example (4-star testimonial):**
```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 fade-in">
    <div class="flex items-center mb-4">
        <div class="text-yellow-400 mr-1">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-600 mb-4 italic">"Their service was excellent and professional."</p>
    <div class="font-semibold">John Smith</div>
    <div class="text-gray-500 text-sm">Homeowner</div>
</div>
```

---

### 7. FAQ Section

**Location:** Lines 240-310

Each FAQ item has a question and answer that expands/collapses.

```html
<div class="faq-item mb-4">
    <div class="faq-question bg-white p-6 rounded-lg shadow-md cursor-pointer hover:bg-gray-50 transition-colors duration-300">
        <div class="flex justify-between items-center">
            <h3 class="text-xl font-semibold">How long does a typical painting project take?</h3>
            <i class="fas fa-chevron-down faq-icon transition-transform duration-300"></i>
        </div>
    </div>
    <div class="faq-answer hidden bg-white p-6 rounded-b-lg shadow-md">
        <p class="text-gray-600">The duration of a painting project varies...</p>
    </div>
</div>
```

**How to Update an FAQ:**

1. **Change the Question:**
   - Find `<h3 class="text-xl font-semibold">How long does a typical painting project take?</h3>`
   - Replace the question text

2. **Change the Answer:**
   - Find `<p class="text-gray-600">The duration of a painting project varies...</p>`
   - Replace with your answer

**Example:**
```html
<div class="faq-item mb-4">
    <div class="faq-question bg-white p-6 rounded-lg shadow-md cursor-pointer hover:bg-gray-50 transition-colors duration-300">
        <div class="flex justify-between items-center">
            <h3 class="text-xl font-semibold">Do you offer emergency services?</h3>
            <i class="fas fa-chevron-down faq-icon transition-transform duration-300"></i>
        </div>
    </div>
    <div class="faq-answer hidden bg-white p-6 rounded-b-lg shadow-md">
        <p class="text-gray-600">Yes, we offer 24/7 emergency services for urgent cleaning needs. Contact us immediately for availability.</p>
    </div>
</div>
```

---

### 8. Footer Contact Information

**Location:** Lines 350-365

```html
<li class="text-gray-400"><i class="fas fa-envelope mr-2"></i> iainhmunro@gmail.com</li>
<li class="text-gray-400"><i class="fas fa-phone mr-2"></i> (555) 123-4567</li>
<li class="text-gray-400"><i class="fas fa-map-marker-alt mr-2"></i> 123 Main St, Toronto, ON</li>
```

**How to Update:**

1. **Change Email:**
   - Find `iainhmunro@gmail.com`
   - Replace with your email address

2. **Change Phone Number:**
   - Find `(555) 123-4567`
   - Replace with your phone number

3. **Change Address:**
   - Find `123 Main St, Toronto, ON`
   - Replace with your business address

**Example:**
```html
<li class="text-gray-400"><i class="fas fa-envelope mr-2"></i> contact@yourcompany.com</li>
<li class="text-gray-400"><i class="fas fa-phone mr-2"></i> (416) 555-0123</li>
<li class="text-gray-400"><i class="fas fa-map-marker-alt mr-2"></i> 456 Queen St, Toronto, ON M5H 2N2</li>
```

---

### 9. Copyright Year

**Location:** Line 378

```html
<p>&copy; 2025 Fresh Feel Painting & Cleaning. All rights reserved.</p>
```

**How to Update:**
- Replace `2025` with the current year
- Replace `Fresh Feel Painting & Cleaning` with your company name

**Example:**
```html
<p>&copy; 2024 Your Company Name. All rights reserved.</p>
```

---

## Modifying Colors & Styling

### Understanding Tailwind CSS Color Classes

Tailwind uses a naming convention for colors. Common ones used on this page:

- `text-blue-600`: Blue text (used for headings)
- `bg-white`: White background
- `bg-gray-50`: Light gray background
- `bg-gray-800`: Dark gray background (footer)
- `text-gray-600`: Gray text
- `text-yellow-400`: Yellow text (star ratings)

### Changing the Primary Color (Blue to Another Color)

The page currently uses `blue-600` as the primary color. To change it throughout:

**Step 1: Find All Blue Color Classes**

Search for these in your editor (Ctrl+F or Cmd+F):
- `text-blue-600`
- `bg-blue-600`
- `bg-blue-50`
- `hover:text-blue-600`
- `hover:bg-blue-600`

**Step 2: Choose Your New Color**

Tailwind color options: `red`, `orange`, `yellow`, `green`, `blue`, `indigo`, `purple`, `pink`

Each has shades: `-50`, `-100`, `-200`, `-300`, `-400`, `-500`, `-600`, `-700`, `-800`, `-900`

**Step 3: Replace the Color**

For example, to change from blue to green:
- Replace `text-blue-600` with `text-green-600`
- Replace `bg-blue-50` with `bg-green-50`
- Replace `bg-blue-600` with `bg-green-600`

**Example - Changing to Green:**

Original:
```html
<section class="hero-gradient text-white py-24 md:py-32">
```

The hero gradient is defined in the `<style>` section (line 16):
```css
.hero-gradient {
    background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 100%);
}
```

To change to green, you'd need to use green hex codes:
```css
.hero-gradient {
    background: linear-gradient(135deg, #1b4332 0%, #40916c 100%);
}
```

---

### Changing Section Backgrounds

**Hero Section Background:**
Located at line 50, the gradient is defined in the `<style>` section (lines 14-17).

To change the hero gradient color:
1. Find the `.hero-gradient` CSS rule
2. Replace the hex colors with new ones

**Feature Cards Background:**
- Currently: `bg-white` (white background)
- To change: Replace `bg-white` with another background color

**Benefits Section Background:**
- Currently: `bg-blue-50` (light blue)
- To change: Replace `bg-blue-50` with another color

---

### Changing Font Sizes

Font size classes in Tailwind follow this pattern: `text-{size}`

- `text-sm`: Small
- `text-base`: Normal
- `text-lg`: Large
- `text-xl`: Extra Large
- `text-2xl`: 2X Large
- `text-3xl`: 3X Large
- `text-4xl`: 4X Large
- `text-5xl`: 5X Large
- `text-6xl`: 6X Large

**Example - Make Hero Headline Smaller:**

Original:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 tracking-tight">
```

Changed:
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-6 tracking-tight">
```

---

### Changing Spacing (Padding & Margins)

Tailwind spacing classes: `p-{number}` (padding), `m-{number}` (margin)

- `p-4`: Small padding
- `p-6`: Medium padding
- `p-8`: Large padding
- `mb-4`: Margin bottom (small)
- `mb-6`: Margin bottom (medium)
- `mb-12`: Margin bottom (large)

**Example - Add more space between sections:**

Original:
```html
<section class="py-16 md:py-24 bg-gray-50">
```

Changed (more space):
```html
<section class="py-24 md:py-32 bg-gray-50">
```

---

## Fixing & Managing Links

### Current Links in the Navigation

**Location:** Lines 34-39 and 43-48 (desktop and mobile navigation)

```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
<a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
```

**Understanding Links:**
- `href="#features"`: Links to a section with `id="features"` on the same page
- `href="https://example.com"`: Links to an external website
- `href="page.html"`: Links to another HTML file in the same folder

---

### Fixing the "Get Started" Button Links

**Location:** Lines 57-58 and 331 (multiple places)

```html
<a href="https://www.freshfeelpaintingandcleaning.ca/" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-50 transition-all duration-300 transform hover:scale-105 shadow-md hover:shadow-lg">Get Started</a>
```

**How to Update:**

1. Find all instances of `href="https://www.freshfeelpaintingandcleaning.ca/"`
2. Replace with your website URL or contact page

**Options:**
- Link to external website: `href="https://yourwebsite.com"`
- Link to a contact form: `href="contact.html"`
- Link to email: `href="mailto:email@example.com"`
- Link to phone: `href="tel:+14165550123"`

**Examples:**
```html
<!-- Link to website -->
<a href="https://www.yourcompany.com/">Get Started</a>

<!-- Link to contact page -->
<a href="contact.html">Get Started</a>

<!-- Link to email -->
<a href="mailto:contact@yourcompany.com">Get Started</a>

<!-- Link to phone -->
<a href="tel:+14165550123">Get Started</a>
```

---

### Fixing the Header Logo Link

**Location:** Line 33

```html
<a href="#" class="text-2xl font-bold text-blue-600">Fresh Feel</a>
```

**How to Update:**

The `href="#"` currently doesn't go anywhere. Change it to:
- `href="index.html"` (links to home page)
- `href="/"` (links to root/home)
- `href="https://yourwebsite.com"` (links to external site)

**Example:**
```html
<a href="index.html" class="text-2xl font-bold text-blue-600">Fresh Feel</a>
```

---

### Fixing Social Media Links

**Location:** Lines 340-344 (Footer)

```html
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-facebook text-xl"></i></a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-twitter text-xl"></i></a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-instagram text-xl"></i></a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-linkedin text-xl"></i></a>
```

**How to Update:**

1. Find your social media profile URL
2. Replace `href="#"` with your actual URL

**Examples:**
```html
<!-- Facebook -->
<a href="https://www.facebook.com/yourpage" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-facebook text-xl"></i></a>

<!-- Twitter/X -->
<a href="https://twitter.com/yourhandle" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-twitter text-xl"></i></a>

<!-- Instagram -->
<a href="https://www.instagram.com/yourhandle" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-instagram text-xl"></i></a>

<!-- LinkedIn -->
<a href="https://www.linkedin.com/company/yourcompany" class="text-gray-400 hover:text-white transition-colors duration-300"><i class="fab fa-linkedin text-xl"></i></a>
```

---

### Fixing Footer Quick Links

**Location:** Lines 347-351

```html
<li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
<li><a href="#contact" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
```

These links use anchor tags (`#features`, `#benefits`, etc.) that jump to sections on the page. They should work automatically if the corresponding `id` attributes exist in the HTML.

**Verify these section IDs exist:**
- `id="features"` - Line 63
- `id="benefits"` - Line 103
- `id="testimonials"` - Line 143
- `id="faq"` - Line 237
- `id="about"` - Line 205

If you remove a section, remove its link from the navigation and footer.

---

## Adding Privacy & Terms Pages

### Step 1: Create the Privacy Policy Page

1. **Create a new file:**
   - Right-click in your project folder
   - Select "New File"
   - Name it `privacy.html`

2. **Add basic HTML structure:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Fresh Feel Painting & Cleaning</title>
    <meta name="description" content="Privacy Policy for Fresh Feel Painting & Cleaning">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-800 font-sans">
    <!-- Header (same as index.html) -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="index.html" class="text-2xl font-bold text-blue-600">Fresh Feel</a>
            <nav class="hidden md:flex space-x-6">
                <a href="index.html#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
                <a href="index.html#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="container mx-auto px-4 max-w-3xl">
            <h1 class="text-4xl md:text-5xl font-bold mb-8">Privacy Policy</h1>
            
            <h2 class="text-2xl font-bold mt-8 mb-4">1. Introduction</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                Fresh Feel Painting & Cleaning ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">2. Information We Collect</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                We may collect information about you in a variety of ways. The information we may collect on the site includes:
            </p>
            <ul class="text-gray-600 mb-4 leading-relaxed list-disc list-inside">
                <li>Personal identification information (name, email address, phone number, etc.)</li>
                <li>Payment information</li>
                <li>Browsing data and cookies</li>
                <li>Device information</li>
            </ul>

            <h2 class="text-2xl font-bold mt-8 mb-4">3. Use of Your Information</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. 
                Specifically, we may use information collected about you via the site to:
            </p>
            <ul class="text-gray-600 mb-4 leading-relaxed list-disc list-inside">
                <li>Generate invoices and send billing information</li>
                <li>Fulfill and manage purchases, orders, payments, and other transactions</li>
                <li>Email regarding your account or order</li>
                <li>Improve our website and services</li>
                <li>Respond to your inquiries, questions, and requests</li>
            </ul>

            <h2 class="text-2xl font-bold mt-8 mb-4">4. Disclosure of Your Information</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                We do not sell, trade, or otherwise transfer to outside parties your Personally Identifiable Information unless we provide 
                users with advance notice. This does not include website hosting partners and other parties who assist us in operating our website, 
                conducting our business, or serving our users, so long as those parties agree to keep this information confidential.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">5. Security of Your Information</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                We use administrative, technical, and physical security measures to protect your personal information. 
                However, perfect security cannot be guaranteed on the Internet.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">6. Contact Us</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                If you have questions or comments about this Privacy Policy, please contact us at:
            </p>
            <p class="text-gray-600">
                Email: <a href="mailto:contact@yourcompany.com" class="text-blue-600 hover:text-blue-800">contact@yourcompany.com</a><br>
                Phone: <a href="tel:+14165550123" class="text-blue-600 hover:text-blue-800">(416) 555-0123</a>
            </p>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-800 text-white py-16 md:py-24">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-2xl font-bold mb-4">Fresh Feel</h3>
                    <p class="text-gray-400 mb-4">Transform your space with expert painting and meticulous cleaning services.</p>
                </div>
                <div>
                    <h3 class="text-xl font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-xl font-semibold mb-4">Legal</h3>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
                <p>&copy; 2024 Fresh Feel Painting & Cleaning. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

1. **Create a new file:**
   - Right-click in your project folder
   - Select "New File"
   - Name it `terms.html`

2. **Add basic HTML structure:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Terms of Service - Fresh Feel Painting & Cleaning</title>
    <meta name="description" content="Terms of Service for Fresh Feel Painting & Cleaning">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-800 font-sans">
    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="index.html" class="text-2xl font-bold text-blue-600">Fresh Feel</a>
            <nav class="hidden md:flex space-x-6">
                <a href="index.html#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
                <a href="index.html#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="container mx-auto px-4 max-w-3xl">
            <h1 class="text-4xl md:text-5xl font-bold mb-8">Terms of Service</h1>
            
            <h2 class="text-2xl font-bold mt-8 mb-4">1. Acceptance of Terms</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. 
                If you do not agree to abide by the above, please do not use this service.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">2. Use License</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                Permission is granted to temporarily download one copy of the materials (information or software) on Fresh Feel's website 
                for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under 
                this license you may not:
            </p>
            <ul class="text-gray-600 mb-4 leading-relaxed list-disc list-inside">
                <li>Modify or copy the materials</li>
                <li>Use the materials for any commercial purpose or for any public display</li>
                <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                <li>Remove any copyright or other proprietary notations from the materials</li>
                <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
            </ul>

            <h2 class="text-2xl font-bold mt-8 mb-4">3. Disclaimer</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                The materials on Fresh Feel's website are provided on an 'as is' basis. Fresh Feel makes no warranties, 
                expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, 
                implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property 
                or other violation of rights.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">4. Limitations</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                In no event shall Fresh Feel or its suppliers be liable for any damages (including, without limitation, damages for loss of 
                data or profit, or due to business interruption) arising out of the use or inability to use the materials on Fresh Feel's website, 
                even if Fresh Feel or an authorized representative has been notified orally or in writing of the possibility of such damage.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">5. Accuracy of Materials</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                The materials appearing on Fresh Feel's website could include technical, typographical, or photographic errors. 
                Fresh Feel does not warrant that any of the materials on its website are accurate, complete, or current. 
                Fresh Feel may make changes to the materials contained on its website at any time without notice.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">6. Links</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                Fresh Feel has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. 
                The inclusion of any link does not imply endorsement by Fresh Feel of the site. Use of any such linked website is at the user's own risk.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">7. Modifications</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                Fresh Feel may revise these terms of service for its website at any time without notice. 
                By using this website, you are agreeing to be bound by the then current version of these terms of service.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">8. Governing Law</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                These terms and conditions are governed by and construed in accordance with the laws of Ontario, Canada, 
                and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
            </p>

            <h2 class="text-2xl font-bold mt-8 mb-4">9. Contact Us</h2>
            <p class="text-gray-600 mb-4 leading-relaxed">
                If you have any questions about these Terms of Service, please contact us at:
            </p>
            <p class="text-gray-600">
                Email: <a href="mailto:contact@yourcompany.com" class="text-blue-600 hover:text-blue-800">contact@yourcompany.com</a><br>
                Phone: <a href="tel:+14165550123" class="text-blue-600 hover:text-blue-800">(416) 555-0123</a>
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-16 md:py-24">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-2xl font-bold mb-4">Fresh Feel</h3>
                    <p class="text-gray-400 mb-4">Transform your space with expert painting and meticulous cleaning services.</p>
                </div>
                <div>
                    <h3 class="text-xl font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-xl font-semibold mb-4">Legal</h3>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
                <p>&copy; 2024 Fresh Feel Painting & Cleaning. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Update Links in index.html

Now update the footer in `index.html` to link to these new pages.

**Location:** Lines 363-364

**Original:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

These are already correct! They already link to the right files. Just make sure your files are named exactly `privacy.html` and `terms.html`.

---

### Step 4: Verify File Structure

After creating the files, your project folder should look like:

```
project-folder/
├── index.html
├── privacy.html
├── terms.html
└── blog.html (optional)
```

All files should be in the **same directory** for the links to work correctly.

---

## Common Customizations

### Adding a New Section

**Example: Adding a "Our Team" Section**

1. **Choose where to add it** (e.g., after the About section)

2. **Create the HTML structure:**

```html
<!-- Our Team Section -->
<section id="team" class="py-16 md:py-24 bg-gray-50">
    <div class="container mx-auto px-4">
        <div class="text-center mb-12 fade-in">
            <h2 class="text-3xl md:text-4xl font-bold mb-4">Meet Our Team</h2>
            <p class="text-xl text-gray-600 max-w-3xl mx-auto">Our experienced professionals are dedicated to delivering exceptional results.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Team Member 1 -->
            <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 fade-in">
                <div class="text-center">
                    <h3 class="text-2xl font-semibold mb-2">John Smith</h3>
                    <p class="text-blue-600 font-semibold mb-4">Founder & Lead Painter</p>
                    <p class="text-gray-600">With 15+ years of experience in professional painting services.</p>
                </div>
            </div>
            <!-- Team Member 2 -->
            <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 fade-in">
                <div class="text-center">
                    <h3 class="text-2xl font-semibold mb-2">Sarah Johnson</h3>
                    <p class="text-blue-600 font-semibold mb-4">Cleaning Specialist</p>
                    <p class="text-gray-600">Expert in eco-friendly cleaning solutions and customer satisfaction.</p>
                </div>
            </div>
            <!-- Team Member 3 -->
            <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 fade-in">
                <div class="text-center">
                    <h3 class="text-2xl font-semibold mb-2">Mike Davis</h3>
                    <p class="text-blue-600 font-semibold mb-4">Project Manager</p>
                    <p class="text-gray-600">Ensures every project is completed on time and to perfection.</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

3. **Add the link to navigation:**

Find the navigation section (lines 34-39) and add:
```html
<a href="#team" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Team</a>
```

---

### Changing the Hero Background Image

**Location:** Lines 330-331

```html
<section class="relative py-16 md:py-24 bg-cover bg-center" style="background-image: url('https://images.unsplash.com/photo-1581578731548-c64695cc6952?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');">
```

**How to Change:**

1. Find a new image URL from:
   - [Unsplash](https://unsplash.com) (free)
   - [Pexels](https://www.pexels.com) (free)
   - [Pixabay](https://pixabay.com) (free)

2. Replace the URL in `background-image: url('YOUR_NEW_URL_HERE')`

**Example:**
```html
<section class="relative py-16 md:py-24 bg-cover bg-center" style="background-image: url('https://images.unsplash.com/photo-1552321554-5fefe8c9ef14?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');">
```

---

### Adding a Contact Form Section

**Add before the CTA Section (around line 328):**

```html
<!-- Contact Form Section -->
<section id="contact" class="py-16 md:py-24">
    <div class="container mx-auto px-4 max-w-2xl">
        <div class="text-center mb-12 fade-in">
            <h2 class="text-3xl md:text-4xl font-bold mb-4">Get in Touch</h2>
            <p class="text-xl text-gray-600">Have questions? We'd love to hear from you. Send us a message!</p>
        </div>
        <form class="bg-gray-50 p-8 rounded-xl shadow-md">
            <div class="mb-6">
                <label for="name" class="block text-gray-700 font-semibold mb-2">Name</label>
                <input type="text" id="name" name="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600" required>
            </div>
            <div class="mb-6">
                <label for="email" class="block text-gray-700 font-semibold mb-2">Email</label>
                <input type="email" id="email" name="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600" required>
            </div>
            <div class="mb-6">
                <label for="phone" class="block text-gray-700 font-semibold mb-2">Phone</label>
                <input type="tel" id="phone" name="phone" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600">
            </div>
            <div class="mb-6">
                <label for="message" class="block text-gray-700 font-semibold mb-2">Message</label>
                <textarea id="message" name="message" rows="5" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600" required></textarea>
            </div>
            <button type="submit" class="w-full bg-blue-600 text-white px-8 py-3 rounded-full font-semibold hover:bg-blue-700 transition-all duration-300">Send Message</button>
        </form>
    </div>
</section>
```

---

## Troubleshooting

### Problem: Links Not Working

**Possible Causes & Solutions:**

1. **Wrong file path:**
   - ✓ Make sure all HTML files are in the same folder
   - ✓ Check spelling: `privacy.html` (not `Privacy.html` or `privacy.HTML`)

2. **External links not working:**
   - ✓ Make sure URL starts with `https://` or `http://`
   - ✓ Check for typos in the URL
   - ✓ Test the URL in your browser first

3. **Anchor links (jump to sections) not working:**
   - ✓ Make sure the `id` attribute exists on the target element
   - ✓ Check that the `href="#features"` matches `id="features"`
   - ✓ IDs are case-sensitive: `#Features` ≠ `#features`

**Example of correct anchor link:**
```html
<!-- In navigation -->
<a href="#features">Features</a>

<!-- In page -->
<section id="features">...</section>
```

---

### Problem: Styling Not Appearing

**Possible Causes & Solutions:**

1. **Tailwind CSS not loading:**
   - ✓ Check that the CDN link is correct (line 10)
   - ✓ Make sure you have an internet connection (Tailwind loads from CDN)
   - ✓ Wait a few seconds for the page to fully load

2. **Class name typo:**
   - ✓ Common typos: `text-blue-600` vs `text-blue600` (missing hyphen)
   - ✓ Check that spacing classes use hyphens: `mb-4`, not `mb4`

3. **Mobile responsive not working:**
   - ✓ Make sure meta viewport tag is present (line 4)
   - ✓ Test in different browser sizes
   - ✓ Use browser developer tools (F12) to test responsiveness

---

### Problem: Mobile Menu Not Working

**Possible Causes & Solutions:**

1. **JavaScript not running:**
   - ✓ Check browser console for errors (F12 → Console tab)
   - ✓ Make sure JavaScript code is at the end of the file (before `</body>`)

2. **Mobile menu button not visible:**
   - ✓ Check that the button has the class `mobile-menu-button`
   - ✓ Verify the button is inside the header

3. **Menu not toggling:**
   - ✓ Check that the menu has the class `mobile-menu`
   - ✓ Verify the JavaScript code is not modified

---

### Problem: Images Not Showing

**Possible Causes & Solutions:**

1. **External image URL broken:**
   - ✓ Test the image URL in your browser
   - ✓ Make sure URL starts with `https://`
   - ✓ Try a different image URL

2. **Local image file not found:**
   - ✓ Make sure image file is in the same folder as HTML
   - ✓ Check file name spelling and extension (`.jpg`, `.png`, etc.)
   - ✓ Use correct file path: `image.jpg` (if in same folder)

---

### Problem: Page Not Displaying Correctly

**Possible Causes & Solutions:**

1. **File not saved:**
   - ✓ Save your changes (Ctrl+S or Cmd+S)
   - ✓ Refresh the browser (F5 or Cmd+R)

2. **HTML syntax error:**
   - ✓ Check that all opening tags have closing tags
   - ✓ Verify quotes are matched: `"..."` not `"...'`
   - ✓ Use browser developer tools to find errors

3. **CDN links down:**
   - ✓ Check internet connection
   - ✓ Try opening the CDN links directly in browser
   - ✓ Wait a moment and refresh

---

### Problem: Colors Look Different

**Possible Causes:**

1. **Browser cache:**
   - ✓ Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
   - ✓ Clear browser cache

2. **Color class typo:**
   - ✓ Check color shade: `text-blue-600` vs `text-blue-500`
   - ✓ Verify color name: `red`, `green`, `blue`, etc.

3. **CSS specificity issue:**
   - ✓ Make sure newer class comes after old one
   - ✓ Use browser inspector to check which style is applied

---

## Quick Reference: Common Tailwind Classes

### Text Sizes
```
text-sm     = Small
text-base   = Normal
text-lg     = Large
text-xl     = Extra Large
text-2xl    = 2X Large
text-3xl    = 3X Large
text-4xl    = 4X Large
text-5xl    = 5X Large
text-6xl    = 6X Large
```

### Text Colors
```
text-white      = White text
text-gray-600   = Gray text
text-blue-600   = Blue text
text-yellow-400 = Yellow text
text-red-600    = Red text
```

### Background Colors
```
bg-white      = White background
bg-gray-50    = Light gray
bg-gray-800   = Dark gray
bg-blue-50    = Light blue
bg-blue-600   = Blue
```

### Spacing
```
p-4   = Padding (small)
p-6   = Padding (medium)
p-8   = Padding (large)
mb-4  = Margin bottom (small)
mb-6  = Margin bottom (medium)
mb-12 = Margin bottom (large)
```

### Responsive
```
md: = Medium screens and up (tablets)
lg: = Large screens and up (desktops)
```

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
  <!-- Small: 4xl, Medium: 5xl, Large: 6xl -->
</h1>
```

---

## Support & Resources

### Learning Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools - CSS](https://www.w3schools.com/css/)

### Tools
- [Color Picker](https://www.colorpicker.com/)
- [Responsive Design Checker](https://responsivedesignchecker.com/)
- [Browser Developer Tools](https://developer.chrome.com/docs/devtools/) (F12)

### Getting Help
- Check the **Troubleshooting** section above
- Review the specific section for your change
- Use browser developer tools (F12) to inspect elements
- Test changes in multiple browsers

---

## Maintenance Checklist

- [ ] Update company name and contact info
- [ ] Change hero headline and subtitle
- [ ] Update feature cards with your services
- [ ] Add real customer testimonials
- [ ] Update FAQ with your questions
- [ ] Fix all external links (website, social media)
- [ ] Update footer contact information
- [ ] Create and link Privacy Policy page
- [ ] Create and link Terms of Service page
- [ ] Test all links work correctly
- [ ] Test on mobile devices
- [ ] Test on multiple browsers
- [ ] Verify images load correctly
- [ ] Check spelling and grammar

---

## Final Tips

1. **Always backup** your files before making major changes
2. **Test changes** in multiple browsers (Chrome, Firefox, Safari, Edge)
3. **Use browser developer tools** (F12) to debug issues
4. **Keep the structure** of the HTML to avoid breaking functionality
5. **Update consistently** - keep company info the same across all pages
6. **Mobile-first** - always test on mobile devices
7. **Performance** - optimize images for faster loading
8. **Security** - never share sensitive information in the code

---

**Last Updated:** 2024

For questions or issues, refer to the troubleshooting section or consult the resource links provided above.