# Paper Chef Landing Page - Maintenance & Customization Guide

Welcome to the Paper Chef landing page documentation! This guide will help you maintain, customize, and update your website with confidence, even if you're new to web development.

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Updating Text Content](#updating-text-content)
3. [Customizing Tailwind CSS Classes](#customizing-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Issues & Troubleshooting](#common-issues--troubleshooting)
7. [File Structure Best Practices](#file-structure-best-practices)

---

## Quick Start Overview

### What You're Working With

Your `index.html` file is a **single-page landing website** for Paper Chef. It contains:

- **Sticky Header/Navigation** - stays at top when scrolling
- **Hero Section** - large banner with main message
- **Features Section** - three key features with icons
- **Benefits Section** - detailed benefits with images
- **About Section** - company information
- **Testimonials Section** - customer reviews
- **FAQ Section** - expandable questions and answers
- **Contact Section** - contact form and information
- **Footer** - links and company info

### Key Technologies Used

| Technology | Purpose | What You Need to Know |
|-----------|---------|----------------------|
| **HTML** | Structure/Content | The words, headings, and text |
| **Tailwind CSS** | Styling/Design | Classes that control colors, spacing, layout |
| **Font Awesome** | Icons | The little symbols (like shopping cart, star, etc.) |
| **JavaScript** | Interactivity | Makes things clickable, animations, menu toggle |

---

## Updating Text Content

### How to Find and Edit Text

Text content is the easiest thing to update. Follow these steps:

#### Step 1: Open Your File
- Open `index.html` in any text editor (VS Code, Notepad, Sublime Text, etc.)
- Use **Ctrl+F** (Windows) or **Cmd+F** (Mac) to search for text

#### Step 2: Locate the Section You Want to Change

**Example: Changing the Main Hero Headline**

Search for: `"Paper Chef receipt-to-menu meal planning"`

You'll find it here (around line 150):

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Paper Chef receipt-to-menu meal planning
</h1>
```

**To change it:**
1. Select the text: `Paper Chef receipt-to-menu meal planning`
2. Delete it
3. Type your new headline
4. Save the file

**Result:** The new text will appear on your website!

---

### Key Text Sections to Update

#### 1. **Navigation Menu Text** (Header)
**Location:** Lines 65-72

```html
<a href="#home" class="nav-link text-gray-700 font-medium hover:text-blue-600">Home</a>
<a href="#features" class="nav-link text-gray-700 font-medium hover:text-blue-600">Features</a>
<a href="#benefits" class="nav-link text-gray-700 font-medium hover:text-blue-600">Benefits</a>
```

**How to change:** Replace the text between `>` and `</a>` with new menu items.

**Example:**
```html
<!-- OLD -->
<a href="#features" class="nav-link text-gray-700 font-medium hover:text-blue-600">Features</a>

<!-- NEW -->
<a href="#features" class="nav-link text-gray-700 font-medium hover:text-blue-600">Our Features</a>
```

#### 2. **Announcement Bar** (Top Blue Banner)
**Location:** Line 51

```html
<div class="bg-blue-600 text-white py-3 px-4 text-center text-sm md:text-base">
    <i class="fas fa-shipping-fast mr-2"></i>Fast Worldwide Shipping (5 days delivery) • 100% Satisfaction Guarantee
</div>
```

**How to change:** Replace the text after the icon.

**Example:**
```html
<!-- OLD -->
Fast Worldwide Shipping (5 days delivery) • 100% Satisfaction Guarantee

<!-- NEW -->
Limited Time Offer: 50% Off Your First Month • Free Shipping Worldwide
```

#### 3. **Hero Section Subheading**
**Location:** Lines 157-159

```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed">
    Grocery receipt + your pantry = ready-to-cook 7-day plan
</p>
```

**How to change:** Replace the text between the `<p>` tags.

#### 4. **Feature Cards** (Three boxes with icons)
**Location:** Lines 197-234

```html
<!-- Feature 1 -->
<h3 class="text-xl font-bold text-gray-900 mb-3">Receipt-to-Menu OCR</h3>
<p class="text-gray-600 leading-relaxed">
    Simply snap a photo of your grocery receipt...
</p>
```

**How to change:** Update the `<h3>` for the title and the `<p>` for the description.

#### 5. **Testimonials** (Customer Reviews)
**Location:** Lines 565-640

```html
<p class="text-gray-700 leading-relaxed mb-6 text-lg">
    "Paper Chef has completely transformed how I approach meal planning..."
</p>
<p class="font-bold text-gray-900">Sarah Mitchell</p>
<p class="text-gray-600 text-sm">Busy Mom & Food Blogger</p>
```

**How to change:** Replace the quote, name, and title with new testimonials.

#### 6. **Footer Text** (Bottom of Page)
**Location:** Lines 870-876

```html
<p class="text-gray-400 leading-relaxed mb-4">
    Transform your grocery receipts into ready-to-cook meal plans...
</p>
```

**How to change:** Replace the company description.

---

### Pro Tips for Editing Text

✅ **DO:**
- Keep text concise and clear
- Maintain the same general length (very long text might break layouts)
- Use quotation marks carefully (if you use them, make sure they match)
- Save your file after each change

❌ **DON'T:**
- Delete any HTML tags like `<h1>`, `<p>`, `</h1>`, `</p>`
- Change text inside `class=""` attributes
- Remove the `id=` attributes (they're used for navigation links)

---

## Customizing Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses **classes** (like `text-white`, `bg-blue-600`) to control how things look. Instead of writing custom CSS, you apply pre-made classes.

### Common Tailwind Classes in This Landing Page

#### **Text & Colors**

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | Makes text white | `<p class="text-white">` |
| `text-gray-900` | Makes text dark gray | `<p class="text-gray-900">` |
| `text-blue-600` | Makes text blue | `<a class="text-blue-600">` |
| `bg-blue-600` | Makes background blue | `<div class="bg-blue-600">` |
| `bg-white` | Makes background white | `<div class="bg-white">` |
| `bg-gray-50` | Makes background light gray | `<section class="bg-gray-50">` |

#### **Spacing (Padding & Margins)**

| Class | What It Does | Spacing Amount |
|-------|-------------|-----------------|
| `p-4` | Padding (space inside) | Small (16px) |
| `p-8` | Padding | Medium (32px) |
| `px-4` | Padding left & right | 16px |
| `py-4` | Padding top & bottom | 16px |
| `mb-6` | Margin bottom (space below) | 24px |
| `gap-4` | Space between items | 16px |

#### **Sizing & Display**

| Class | What It Does |
|-------|-------------|
| `w-full` | Width 100% (takes full width) |
| `h-screen` | Height full screen |
| `rounded-lg` | Slightly rounded corners |
| `rounded-xl` | More rounded corners |
| `shadow-md` | Medium shadow effect |
| `hidden` | Hides the element |
| `flex` | Displays items in a row |

#### **Responsive Design (Mobile, Tablet, Desktop)**

| Class | Applies To |
|-------|-----------|
| `md:text-5xl` | Medium screens and up (tablets) |
| `lg:text-6xl` | Large screens and up (desktops) |
| `hidden md:flex` | Hidden on mobile, visible on tablets/desktop |

---

### How to Change Colors

#### Example 1: Change Button Color from Blue to Green

**Find this code (line 164):**
```html
<a href="https://stripe.com/checkout" class="btn-primary bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-lg font-bold text-lg transform transition-all duration-300 shadow-lg">
    Get Started Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**Change:**
- `bg-blue-600` → `bg-green-600` (main button color)
- `hover:bg-blue-700` → `hover:bg-green-700` (color when you hover over button)

**Result:**
```html
<a href="https://stripe.com/checkout" class="btn-primary bg-green-600 hover:bg-green-700 text-white px-8 py-4 rounded-lg font-bold text-lg transform transition-all duration-300 shadow-lg">
    Get Started Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

#### Available Colors in Tailwind

```
blue-600, green-600, red-600, purple-600, yellow-600, pink-600, orange-600
```

You can also use numbers: `600`, `700`, `500`, `400`, `300`, etc.

---

### How to Change Spacing

#### Example 2: Add More Space Below a Section

**Find this code (line 182):**
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

**Understanding the current spacing:**
- `py-16` = Medium padding top and bottom (64px)
- `md:py-24` = Larger padding on tablets and up (96px)

**To add MORE space:**
- Change `py-16` to `py-20` (80px)
- Change `md:py-24` to `md:py-32` (128px)

**Result:**
```html
<section id="features" class="py-20 md:py-32 bg-white">
```

---

### How to Change Corner Roundness

#### Example 3: Make Feature Cards More Rounded

**Find this code (line 200):**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 shadow-md hover:shadow-xl">
```

**Current:** `rounded-xl` (extra rounded)

**Options:**
- `rounded-none` - No rounding (square corners)
- `rounded-sm` - Slightly rounded
- `rounded-md` - Medium rounded
- `rounded-lg` - More rounded
- `rounded-xl` - Extra rounded (current)
- `rounded-2xl` - Very extra rounded
- `rounded-full` - Completely circular

**To make them slightly more rounded:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-2xl p-8 shadow-md hover:shadow-xl">
```

---

### How to Change Shadow Effects

#### Example 4: Make Cards Have Stronger Shadows

**Find this code (line 200):**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 shadow-md hover:shadow-xl">
```

**Current shadows:**
- `shadow-md` = Medium shadow (normal state)
- `hover:shadow-xl` = Extra large shadow (when you hover)

**Options (from light to heavy):**
- `shadow-sm` - Very light shadow
- `shadow-md` - Medium shadow
- `shadow-lg` - Large shadow
- `shadow-xl` - Extra large shadow
- `shadow-2xl` - Very extra large shadow

**To make shadows stronger:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 shadow-lg hover:shadow-2xl">
```

---

### How to Change Text Size

#### Example 5: Make Headings Larger

**Find this code (line 187):**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Powerful Features Built for You
</h2>
```

**Current sizes:**
- `text-3xl` = 30px (mobile)
- `md:text-4xl` = 36px (tablets)
- `lg:text-5xl` = 48px (desktop)

**Options:** `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`

**To make larger:**
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-4 tracking-tight">
    Powerful Features Built for You
</h2>
```

---

### Responsive Design Tips

The landing page uses **mobile-first responsive design**. This means:

1. **Classes without prefixes** = Mobile (phones)
2. **`md:` prefix** = Tablets and up
3. **`lg:` prefix** = Desktop and up

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white">
```

This means:
- On phones: 36px text
- On tablets: 48px text
- On desktop: 60px text

**Why?** Smaller text is better on small screens, larger text on big screens.

---

## Fixing and Managing Links

### Understanding Links in This Landing Page

Links are used for:
1. **Navigation menu** - Jump to different sections
2. **Call-to-action buttons** - Go to checkout or external sites
3. **Footer links** - Go to policies and other pages
4. **Internal anchors** - Jump to sections on the same page

---

### Types of Links and How They Work

#### Type 1: Internal Links (Jump to Sections on Same Page)

**Example (line 70):**
```html
<a href="#features" class="nav-link text-gray-700 font-medium hover:text-blue-600">Features</a>
```

**How it works:**
- `href="#features"` = Go to the element with `id="features"`
- When clicked, page scrolls to that section

**To create a new internal link:**
1. Find the section you want to link to
2. Note its `id=` attribute
3. Create a link with `href="#thatid"`

**Example:**
```html
<!-- This is the section you want to link to -->
<section id="myspecialsection" class="py-16">
    <h2>My Special Section</h2>
</section>

<!-- This link will jump to that section -->
<a href="#myspecialsection">Go to My Special Section</a>
```

---

#### Type 2: External Links (Go to Other Websites)

**Example (line 162):**
```html
<a href="https://stripe.com/checkout" class="btn-primary bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-lg font-bold text-lg transform transition-all duration-300 shadow-lg">
    Get Started Now
</a>
```

**How it works:**
- `href="https://stripe.com/checkout"` = Full web address
- When clicked, opens that website in the browser

**To create a new external link:**
```html
<a href="https://www.google.com">Go to Google</a>
```

**Important:** Always include `https://` at the beginning!

---

#### Type 3: Email Links

**Example (line 903):**
```html
<a href="mailto:hello@thepaperchef.com" class="text-blue-500 hover:text-blue-400 transition-colors duration-300">
    hello@thepaperchef.com
</a>
```

**How it works:**
- `href="mailto:email@example.com"` = Opens email client
- When clicked, opens user's default email app

**To create an email link:**
```html
<a href="mailto:yourname@yourdomain.com">Email Us</a>
```

---

### Finding All Links in This Landing Page

**Search for:** `href=`

This will show you every link on the page. Here's a complete list:

| Location | Current Link | Purpose |
|----------|--------------|---------|
| Line 70 | `#home` | Nav: Home |
| Line 71 | `#features` | Nav: Features |
| Line 72 | `#benefits` | Nav: Benefits |
| Line 73 | `#about` | Nav: About |
| Line 74 | `#testimonials` | Nav: Testimonials |
| Line 75 | `#faq` | Nav: FAQ |
| Line 76 | `#contact` | Nav: Contact |
| Line 82 | `https://stripe.com/checkout` | Buy Now Button |
| Line 162 | `https://stripe.com/checkout` | Hero CTA Button |
| Line 167 | (Demo button - no link) | Watch Demo |
| Line 903 | `mailto:hello@thepaperchef.com` | Email |
| Line 912 | `https://blog.html` | Blog (BROKEN) |
| Line 915 | `privacy.html` | Privacy Policy |
| Line 917 | `terms.html` | Terms of Service |

---

### Fixing Broken Links

#### Issue: Links That Don't Work

**Broken Link Example (line 912):**
```html
<a href="https://blog.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Blog</a>
```

**Problem:** `https://blog.html` is not a real website!

**Solution 1: Link to Your Real Blog**
```html
<!-- If you have a blog at your domain -->
<a href="https://www.yourdomain.com/blog" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Blog</a>
```

**Solution 2: Link to External Blog Platform**
```html
<!-- If you use Medium or another platform -->
<a href="https://medium.com/yourprofile" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Blog</a>
```

**Solution 3: Remove the Link (Temporary)**
```html
<span class="text-gray-400">Blog (Coming Soon)</span>
```

---

### Updating All "Buy Now" Links

You have multiple "Buy Now" buttons that point to Stripe checkout. To update them all:

**Search for:** `https://stripe.com/checkout`

**Replace with your actual checkout URL:**

**Step-by-step:**
1. Use **Ctrl+H** (Windows) or **Cmd+H** (Mac) to open Find & Replace
2. Find: `https://stripe.com/checkout`
3. Replace with: `https://your-actual-checkout-url.com`
4. Click "Replace All"

**Example:**
```html
<!-- OLD -->
<a href="https://stripe.com/checkout" class="btn-primary...">Buy Now</a>

<!-- NEW -->
<a href="https://buy.yourdomain.com" class="btn-primary...">Buy Now</a>
```

---

### Updating Social Media Links

**Location:** Lines 879-889 (Footer)

**Current code:**
```html
<a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">
    <i class="fab fa-facebook text-xl"></i>
</a>
```

**Problem:** `href="#"` doesn't go anywhere!

**Solution: Add Your Social Media URLs**

```html
<!-- Facebook -->
<a href="https://www.facebook.com/yourpage" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">
    <i class="fab fa-facebook text-xl"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/yourprofile" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">
    <i class="fab fa-twitter text-xl"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/yourprofile" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">
    <i class="fab fa-instagram text-xl"></i>
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/company/yourcompany" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">
    <i class="fab fa-linkedin text-xl"></i>
</a>
```

---

### Testing Your Links

After updating links, test them:

1. **Open your HTML file in a web browser**
2. **Click each link** to make sure it works
3. **Check that:**
   - Internal links scroll to the right section
   - External links open in a new tab (or same tab)
   - Email links open your email client
   - Buttons navigate to checkout

**If a link doesn't work:**
- Double-check the URL spelling
- Make sure external URLs start with `https://`
- Verify the page/file actually exists

---

## Adding Privacy and Terms Pages

### Current Status

Your landing page has **links to privacy and terms pages**, but the pages don't exist yet:

**In Footer (line 915-917):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Terms of Service</a>
```

**Also in Navigation (line 912-913):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Terms of Service</a>
```

---

### Step-by-Step: Create Privacy Page

#### Step 1: Create a New File

1. Open your text editor
2. Click **File → New File**
3. Save it as `privacy.html` in the same folder as `index.html`

#### Step 2: Add Basic HTML Structure

Copy and paste this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Paper Chef Privacy Policy">
    <title>Privacy Policy - Paper Chef</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i class="fas fa-receipt text-2xl text-blue-600"></i>
                <span class="text-xl font-bold text-gray-900">Paper Chef</span>
            </div>
            <a href="index.html" class="text-gray-700 font-medium hover:text-blue-600">← Back to Home</a>
        </nav>
    </header>
    
    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    Paper Chef ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase products or services from the Site.</li>
                    <li>Data From Receipts: Information from grocery receipts you upload, including items purchased, quantities, and prices.</li>
                    <li>Mobile Device Data: Device information, such as your mobile device ID, model, and manufacturer, and information about your location.</li>
                </ul>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Create and manage your account</li>
                    <li>Process your transactions and send related information</li>
                    <li>Generate meal plans based on your grocery receipts</li>
                    <li>Provide customer service and support</li>
                    <li>Send promotional communications (with your consent)</li>
                    <li>Improve our services and website functionality</li>
                </ul>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>By Law or to Protect Rights: If we believe the release of information is necessary to comply with the law.</li>
                    <li>Third-Party Service Providers: We may share your information with parties who perform services for us, including payment processors, hosting providers, and customer service platforms.</li>
                    <li>Your Consent: We may disclose your information with your consent for any purpose.</li>
                </ul>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to help protect your personal information. While we have taken reasonable steps to secure the personal information you provide to us, please be aware that no security measures are perfect or impenetrable.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p class="font-semibold">
                    Email: <a href="mailto:hello@thepaperchef.com" class="text-blue-600 hover:text-blue-700">hello@thepaperchef.com</a>
                </p>
            </section>
        </div>
    </main>
    
    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; <span id="year">2024</span> Paper Chef. All rights reserved.
            </p>
        </div>
    </footer>
    
    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

#### Step 3: Customize the Content

Replace the placeholder sections with your actual privacy policy. Key sections to customize:

- **1. Introduction** - Add your company details
- **2. Information We Collect** - List what you actually collect
- **3. Use of Your Information** - Explain how you use it
- **4. Disclosure** - Explain who you share data with
- **5. Security** - Describe your security measures
- **6. Contact** - Update with your email

---

### Step-by-Step: Create Terms Page

#### Step 1: Create a New File

1. Open your text editor
2. Click **File → New File**
3. Save it as `terms.html` in the same folder as `index.html`

#### Step 2: Add Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Paper Chef Terms of Service">
    <title>Terms of Service - Paper Chef</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i class="fas fa-receipt text-2xl text-blue-600"></i>
                <span class="text-xl font-bold text-gray-900">Paper Chef</span>
            </div>
            <a href="index.html" class="text-gray-700 font-medium hover:text-blue-600">← Back to Home</a>
        </nav>
    </header>
    
    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Paper Chef's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>
                    The materials on Paper Chef's website are provided on an 'as is' basis. Paper Chef makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall Paper Chef or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Paper Chef's website.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Paper Chef's website could include technical, typographical, or photographic errors. Paper Chef does not warrant that any of the materials on its website are accurate, complete, or current. Paper Chef may make changes to the materials contained on its website at any time without notice.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    Paper Chef has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Paper Chef of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    Paper Chef may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>
            </section>
            
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="font-semibold">
                    Email: <a href="mailto:hello@thepaperchef.com" class="text-blue-600 hover:text-blue-700">hello@thepaperchef.com</a>
                </p>
            </section>
        </div>
    </main>
    
    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; <span id="year">2024</span> Paper Chef. All rights reserved.
            </p>
        </div>
    </footer>
    
    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

#### Step 3: Customize the Content

Replace the placeholder sections with your actual terms. Key sections to customize:

- **1. Agreement to Terms** - Your terms acceptance
- **2. Use License** - What users can/cannot do
- **3. Disclaimer** - Your legal disclaimers
- **4. Limitations** - Liability limitations
- **5. Accuracy** - Content accuracy statement
- **6. Links** - Third-party link policy
- **7. Modifications** - How you can change terms
- **8. Governing Law** - Your jurisdiction
- **9. Contact** - Your contact information

---

### Verifying Your Links Work

After creating both files, test the links:

1. **Open `index.html` in your browser**
2. **Scroll to footer**
3. **Click "Privacy Policy"** - Should open `privacy.html`
4. **Click "Terms of Service"** - Should open `terms.html`
5. **Click "← Back to Home"** - Should return to `index.html`

**If links don't work:**
- Make sure all three files are in the **same folder**
- Make sure filenames are spelled exactly: `index.html`, `privacy.html`, `terms.html`
- Check that you saved the new files

---

### File Structure

Your folder should look like this:

```
your-project-folder/
├── index.html
├── privacy.html
├── terms.html
└── (any other files)
```

---

### Adding Links to Navigation Menu

If you want Privacy/Terms links in the **desktop navigation menu** (not just footer):

**Find line 76 (after Contact link):**
```html
<a href="#contact" class="nav-link text-gray-700 font-medium hover:text-blue-600">Contact</a>
```

**Add these lines after it:**
```html
<a href="privacy.html" class="nav-link text-gray-700 font-medium hover:text-blue-600">Privacy</a>
<a href="terms.html" class="nav-link text-gray-700 font-medium hover:text-blue-600">Terms</a>
```

**Result:**
```html
<a href="#contact" class="nav-link text-gray-700 font-medium hover:text-blue-600">Contact</a>
<a href="privacy.html" class="nav-link text-gray-700 font-medium hover:text-blue-600">Privacy</a>
<a href="terms.html" class="nav-link text-gray-700 font-medium hover:text-blue-600">Terms</a>
```

---

### Adding Links to Mobile Menu

**Find line 105 (in mobile menu, after Contact link):**
```html
<a href="#contact" class="nav-link text-gray-700 font-medium py-2 hover:text-blue-600">Contact</a>
```

**Add these lines after it:**
```html
<a href="privacy.html" class="nav-link text-gray-700 font-medium py-2 hover:text-blue-600">Privacy</a>
<a href="terms.html" class="nav-link text-gray-700 font-medium py-2 hover:text-blue-600">Terms</a>
```

---

## Common Issues & Troubleshooting

### Issue 1: Changes Don't Appear on Website

**Symptoms:** You edited the HTML but the website looks the same.

**Solutions:**

1. **Save the file**
   - After making changes, press **Ctrl+S** (Windows) or **Cmd+S** (Mac)
   - Check that the file was saved (usually shows in the title bar)

2. **Refresh the browser**
   - Press **Ctrl+R** (Windows) or **Cmd+R** (Mac)
   - Or press **Ctrl+Shift+R** (Windows) or **Cmd+Shift+R** (Mac) for hard refresh

3. **Clear browser cache**
   - Sometimes browsers cache old versions
   - Try opening in a different browser
   - Or use Incognito/Private mode

4. **Check you edited the right file**
   - Make sure you're editing `index.html`, not a copy
   - Check the file path in your text editor

---

### Issue 2: Styling Looks Broken

**Symptoms:** Text is huge, colors are wrong, spacing is off.

**Causes:**
- Accidentally deleted or modified a class name
- Removed HTML tags like `<div>` or `</div>`
- Broke the CSS by editing inside `<style>` tags

**Solution:**
- Use **Ctrl+Z** (Windows) or **Cmd+Z** (Mac) to undo recent changes
- Carefully review what you changed
- If stuck, revert to the original file

---

### Issue 3: Links Don't Work

**Symptoms:** Clicking a button or link does nothing.

**Causes:**
- Wrong URL format (missing `https://`)
- File doesn't exist (for internal links)
- Typo in the link address
- Removed `href=` attribute

**Solution:**

1. **For external links:**
   ```html
   <!-- WRONG -->
   <a href="google.com">Google</a>
   
   <!-- RIGHT -->
   <a href="https://google.com">Google</a>
   ```

2. **For internal links:**
   ```html
   <!-- Make sure the section exists -->
   <section id="features">...</section>
   
   <!-- Then link to it -->
   <a href="#features">Go to Features</a>
   ```

3. **For file links:**
   ```html
   <!-- File must exist in same folder -->
   <a href="privacy.html">Privacy</a>
   ```

---

### Issue 4: Mobile Menu Button Doesn't Work

**Symptoms:** On mobile, the hamburger menu button doesn't toggle the menu.

**Causes:**
- JavaScript code was accidentally deleted
- HTML structure was changed
- Classes were renamed

**Solution:**
- Check that the `<script>` section at the bottom is intact
- Make sure classes are exactly: `mobile-menu-button` and `mobile-menu`
- Don't modify the JavaScript unless you know what you're doing

---

### Issue 5: Colors Don't Change

**Symptoms:** You changed a color class but it doesn't look different.

**Causes:**
- Changed the wrong class
- Tailwind class doesn't exist (typo)
- Another class is overriding it

**Solution:**

1. **Double-check the class name**
   ```html
   <!-- WRONG (typo) -->
   <div class="bg-blu-600">Wrong</div>
   
   <!-- RIGHT -->
   <div class="bg-blue-600">Right</div>
   ```

2. **Try a more obvious color**
   ```html
   <!-- Test with red to see if it works -->
   <div class="bg-red-600">Test</div>
   ```

3. **Check for conflicting classes**
   - Remove all classes except the color one
   - Add them back one by one to find the culprit

---

### Issue 6: Text Overflows or Looks Bad

**Symptoms:** Text is too large, wraps weirdly, or goes off the screen.

**Causes:**
- Added too much text
- Changed responsive classes (like `md:` or `lg:`)
- Modified width or padding

**Solution:**

1. **Make text shorter** (if possible)
   ```html
   <!-- Too long -->
   <h1>This is a very long headline that takes up too much space</h1>
   
   <!-- Better -->
   <h1>Short, Powerful Headline</h1>
   ```

2. **Adjust text size classes**
   ```html
   <!-- Too large on mobile -->
   <h1 class="text-6xl">Heading</h1>
   
   <!-- Better -->
   <h1 class="text-3xl md:text-5xl lg:text-6xl">Heading</h1>
   ```

3. **Test on different screen sizes**
   - Open browser developer tools (F12)
   - Click the mobile device icon
   - Try different screen sizes

---

### Issue 7: Images Don't Load

**Symptoms:** You see broken image icons instead of pictures.

**Causes:**
- Image URL is broken
- Image file doesn't exist
- Wrong image path

**Solution:**

1. **Check the image URL**
   ```html
   <!-- WRONG (broken URL) -->
   <img src="https://invalid-url.com/image.jpg" alt="...">
   
   <!-- RIGHT (working URL) -->
   <img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600" alt="...">
   ```

2. **For local images (in your folder)**
   ```html
   <!-- If image is in same folder -->
   <img src="myimage.jpg" alt="Description">
   
   <!-- If image is in subfolder -->
   <img src="images/myimage.jpg" alt="Description">
   ```

3. **Always include alt text**
   ```html
   <img src="photo.jpg" alt="Fresh groceries and meal planning">
   ```

---

### Issue 8: FAQ Accordion Doesn't Expand

**Symptoms:** Clicking FAQ questions doesn't expand them.

**Causes:**
- JavaScript code was deleted
- HTML structure changed
- Class names were modified

**Solution:**
- Check that the `<script>` section is complete
- Make sure the class `faq-toggle` exists on buttons
- Make sure the class `faq-item` exists on containers

---

### Quick Debugging Checklist

Before asking for help, check:

- ✅ Did you save the file? (Ctrl+S / Cmd+S)
- ✅ Did you refresh the browser? (Ctrl+R / Cmd+R)
- ✅ Did you hard refresh? (Ctrl+Shift+R / Cmd+Shift+R)
- ✅ Is the file in the right location?
- ✅ Did you accidentally delete HTML tags?
- ✅ Did you accidentally delete the `<script>` section?
- ✅ Are class names spelled correctly?
- ✅ Do external links start with `https://`?
- ✅ Do internal links match section IDs?

---

## File Structure Best Practices

### Recommended Folder Organization

As your website grows, organize files like this:

```
paper-chef-website/
├── index.html                 (Main landing page)
├── privacy.html               (Privacy policy)
├── terms.html                 (Terms of service)
├── css/
│   └── custom.css            (Optional custom styles)
├── js/
│   └── custom.js             (Optional custom JavaScript)
├── images/
│   ├── logo.png
│   ├── hero-bg.jpg
│   └── feature-icons/
│       ├── icon1.svg
│       ├── icon2.svg
│       └── icon3.svg
├── assets/
│   └── fonts/                (Custom fonts if needed)
└── README.md                 (Documentation)
```

---

### How to Use This Structure

#### Adding External CSS File

1. **Create `css/custom.css`**
2. **Add to `index.html` head (after Tailwind)**
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   <link rel="stylesheet" href="css/custom.css">
   ```

#### Adding External JavaScript File

1. **Create `js/custom.js`**
2. **Add to `index.html` before closing `</body>`**
   ```html
   <script src="js/custom.js"></script>
   </body>
   </html>
   ```

#### Using Local Images

1. **Put images in `images/` folder**
2. **Reference in HTML**
   ```html
   <!-- OLD (external URL) -->
   <img src="https://images.unsplash.com/..." alt="...">
   
   <!-- NEW (local file) -->
   <img src="images/hero-bg.jpg" alt="...">
   ```

---

### Backup Best Practices

**Always keep backups!**

1. **Before making major changes:**
   - Copy entire folder
   - Name it `paper-chef-website-backup-date`
   - Store safely

2. **Use version control (Git)**
   - Create a GitHub repository
   - Commit changes regularly
   - Easy to revert if something breaks

3. **Keep a change log**
   - Document what you changed
   - When you changed it
   - Why you changed it

**Example change log:**
```
2024-01-15: Updated hero headline text
2024-01-14: Changed button colors from blue to green
2024-01-13: Added privacy and terms pages
2024-01-12: Fixed broken social media links
```

---

### Testing Checklist Before Going Live

Before publishing your website:

- ✅ All links work (internal and external)
- ✅ All images load correctly
- ✅ Mobile menu works
- ✅ FAQ accordion works
- ✅ Forms have valid email
- ✅ Contact info is correct
- ✅ Privacy/Terms pages exist and link correctly
- ✅ Social media links are correct
- ✅ Checkout link is correct
- ✅ Website looks good on mobile, tablet, desktop
- ✅ No broken images or missing content
- ✅ Page loads quickly
- ✅ No console errors (open DevTools with F12)

---

## Quick Reference Guide

### Finding Sections to Edit

| Section | Search For | Line # |
|---------|-----------|--------|
| Announcement Bar | "Fast Worldwide Shipping" | 51 |
| Logo/Brand Name | "Paper Chef" (in header) | 56 |
| Navigation Links | `<a href="#home"` | 70-76 |
| Hero Headline | "Paper Chef receipt-to-menu" | 150 |
| Hero Subheading | "Grocery receipt + your pantry" | 157 |
| Features Section | "Powerful Features Built for You" | 187 |
| Benefits Section | "Why Choose Paper Chef?" | 282 |
| About Section | "About Paper Chef" | 419 |
| Testimonials | "Loved by Home Cooks" | 565 |
| FAQ Section | "Frequently Asked Questions" | 659 |
| CTA Section | "Ready to Transform" | 770 |
| Contact Form | "Get in Touch" | 795 |
| Footer | `<footer>` | 865 |

---

### Common Tailwind Classes Reference

**Text Colors:**
```
text-white, text-gray-900, text-gray-700, text-gray-600, text-blue-600, text-green-600, text-red-600
```

**Background Colors:**
```
bg-white, bg-gray-50, bg-gray-100, bg-blue-600, bg-green-600, bg-red-600
```

**Spacing (Padding/Margin):**
```
p-4, p-8, p-12 (padding)
m-4, m-8, m-12 (margin)
px-4, py-4 (padding left/right, top/bottom)
mb-6, mt-6 (margin bottom, top)
gap-4, gap-8 (space between items)
```

**Sizing:**
```
w-full, w-1/2, h-screen, h-96
```

**Rounded Corners:**
```
rounded-lg, rounded-xl, rounded-2xl, rounded-full
```

**Shadows:**
```
shadow-sm, shadow-md, shadow-lg, shadow-xl
```

**Responsive Prefixes:**
```
md: (tablets and up)
lg: (desktops and up)
```

---

### Common HTML Tags Reference

```html
<h1>Largest Heading</h1>
<h2>Section Heading</h2>
<h3>Subsection Heading</h3>
<p>Paragraph of text</p>
<a href="url">Link</a>
<div>Container/Box</div>
<section>Large section</section>
<img src="image.jpg" alt="Description">
<button>Clickable button</button>
<form>Form container</form>
<input type="text" placeholder="...">
<textarea>Text area</textarea>
<i class="fas fa-icon">Icon</i>
```

---

## Final Tips for Success

### 1. Start Small
- Make one small change
- Test it
- Make sure it works
- Then make another change

### 2. Use Comments
Add notes to remember what you changed:
```html
<!-- Updated hero headline 2024-01-15 -->
<h1>New Headline</h1>
```

### 3. Test Everything
- Click every link
- Test on mobile
- Try different browsers
- Make sure forms work

### 4. Keep It Organized
- Use consistent naming
- Keep files in right folders
- Document your changes
- Keep backups

### 5. When Stuck
- Use Ctrl+Z to undo
- Check browser console (F12)
- Search the code for similar examples
- Ask for help with specific error messages

---

## Getting More Help

### Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **Font Awesome Icons:** https://fontawesome.com/icons
- **Color Picker:** https://tailwindcss.com/docs/customizing-colors

### Common Questions

**Q: How do I change the blue color to something else?**
A: Replace `blue-600` with `green-600`, `red-600`, `purple-600`, etc.

**Q: How do I make text bigger?**
A: Change `text-xl` to `text-2xl`, `text-3xl`, `text-4xl`, etc.

**Q: How do I add more space between elements?**
A: Increase the number in `gap-4` to `gap-6`, `gap-8`, etc.

**Q: How do I hide something on mobile?**
A: Add `hidden md:block` class.

**Q: How do I make something full width?**
A: Add `w-full` class.

---

## Conclusion

Congratulations! You now have a comprehensive guide to maintaining and customizing the Paper Chef landing page. Remember:

- **Start small** and test often
- **Use Find & Replace** to update multiple items
- **Keep backups** of working versions
- **Test on mobile** before publishing
- **Ask for help** when needed

Your landing page is built with modern, maintainable code. With this guide, you have everything you need to keep it fresh and up-to-date!

Happy editing! 🍳