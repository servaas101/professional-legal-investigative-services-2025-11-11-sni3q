# SOMDA Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the SOMDA Professional Legal & Investigative Services landing page.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Working with Tailwind CSS Classes](#working-with-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Color Customization](#color-customization)
8. [Responsive Design Tips](#responsive-design-tips)
9. [Troubleshooting](#troubleshooting)
10. [Best Practices](#best-practices)

---

## Getting Started

### What You Need

Before making changes to this landing page, you should have:

- **A text editor** such as:
  - Visual Studio Code (recommended for beginners)
  - Notepad++
  - Sublime Text
  - Or any basic text editor (even Notepad works)

- **A web browser** to preview your changes:
  - Chrome, Firefox, Safari, or Edge

- **Basic file management** skills to save and organize HTML files

### How to Edit the File

1. **Open the HTML file** in your text editor
2. **Make your changes** following the guides below
3. **Save the file** (Ctrl+S on Windows, Cmd+S on Mac)
4. **Preview in browser** by opening the HTML file directly or using a local server
5. **Check responsiveness** by resizing your browser window or testing on different devices

### File Organization

Your project folder should look like this:

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy - you'll create this)
├── terms.html (terms of service - you'll create this)
└── blog.html (blog page - already referenced)
```

---

## Understanding the Page Structure

The landing page is organized into distinct sections. Understanding these sections will help you know where to make changes.

### Main Sections (in order from top to bottom)

| Section | Purpose | Key Content |
|---------|---------|-------------|
| **Header/Navigation** | Site navigation and branding | Logo, menu links, "Get Started" button |
| **Hero Section** | Main introduction | Large headline, subheading, call-to-action buttons |
| **Features Section** | Service offerings | Three main services with descriptions |
| **Benefits Section** | Why choose SOMDA | Three key benefits with icons |
| **About Us Section** | Company information | Company background and values |
| **Testimonials Section** | Client reviews | Four client testimonials with ratings |
| **FAQ Section** | Common questions | Five expandable Q&A items |
| **CTA Section** | Final call-to-action | Secondary promotion before footer |
| **Contact Form Section** | Lead capture | Email contact form |
| **Footer** | Site information | Links, contact info, social media |

---

## Updating Text Content

This section shows you exactly where to find and update text throughout the page.

### Header/Navigation Area

**Location:** Lines 103-135 in the HTML

The header contains your company name, navigation menu, and call-to-action button.

#### Updating the Company Name

**Current code:**
```html
<span class="text-2xl font-semibold text-white">SOMDA</span>
```

**How to change it:**
1. Find the text `SOMDA` in the header section
2. Replace `SOMDA` with your company name
3. The text automatically resizes on mobile devices (you don't need to change anything else)

**Example:**
```html
<!-- Before -->
<span class="text-2xl font-semibold text-white">SOMDA</span>

<!-- After -->
<span class="text-2xl font-semibold text-white">Your Law Firm Name</span>
```

#### Updating Navigation Menu Links

**Current code:**
```html
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>
<a href="#benefits" class="text-gray-300 hover:text-primary smooth-transition">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-primary smooth-transition">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-primary smooth-transition">FAQ</a>
```

**How to change menu text:**
1. Find each `<a>` tag in the navigation
2. Change the text between the opening and closing tags
3. Keep the `href="#"` part the same (it jumps to sections)

**Example:**
```html
<!-- Before -->
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>

<!-- After - Change the visible text -->
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition">Our Services</a>
```

**Important:** Don't change the `href="#features"` part unless you also change the section ID below.

#### Updating the "Get Started" Button Text

**Current code:**
```html
<a href="https://somda.co.za/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
    Get Started
</a>
```

**How to change it:**
1. Find the text `Get Started` in the header
2. Replace it with your preferred text
3. To change where the button links to, modify the `href="https://somda.co.za/contact/"` URL

**Example:**
```html
<!-- Before -->
<a href="https://somda.co.za/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
    Get Started
</a>

<!-- After -->
<a href="https://yourwebsite.com/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
    Book a Consultation
</a>
```

---

### Hero Section (Main Introduction)

**Location:** Lines 139-200

This is the large introductory section at the top of the page with the big headline.

#### Updating the Main Headline

**Current code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold leading-tight text-white">
    Professional Legal & Investigative <span class="text-primary">Services</span>
</h1>
```

**How to change it:**
1. Replace the text `Professional Legal & Investigative`
2. The word in the `<span class="text-primary">Services</span>` appears in the accent color (orange/gold)
3. Keep or change this colored word as needed

**Example:**
```html
<!-- Before -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold leading-tight text-white">
    Professional Legal & Investigative <span class="text-primary">Services</span>
</h1>

<!-- After -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold leading-tight text-white">
    Expert Legal Solutions & <span class="text-primary">Investigations</span>
</h1>
```

#### Updating the Tagline

**Current code:**
```html
<p class="text-lg md:text-xl text-gray-300 leading-relaxed font-light">
    Investigations & Legal Counsel — Clear Results
</p>
```

**How to change it:**
1. Replace the entire text with your tagline
2. This text is smaller than the main headline

**Example:**
```html
<!-- Before -->
<p class="text-lg md:text-xl text-gray-300 leading-relaxed font-light">
    Investigations & Legal Counsel — Clear Results
</p>

<!-- After -->
<p class="text-lg md:text-xl text-gray-300 leading-relaxed font-light">
    Strategic Legal Representation & Thorough Investigation
</p>
```

#### Updating the Main Description

**Current code:**
```html
<p class="text-base md:text-lg text-gray-400 leading-relaxed font-light max-w-xl">
    Navigate complex legal challenges with confidence. Our expert team combines forensic investigation, courtroom excellence, and strategic legal counsel to deliver decisive outcomes that protect your interests and resolve disputes effectively.
</p>
```

**How to change it:**
1. Replace all the text inside this paragraph
2. This is the longer description below the tagline

**Example:**
```html
<!-- Before -->
<p class="text-base md:text-lg text-gray-400 leading-relaxed font-light max-w-xl">
    Navigate complex legal challenges with confidence. Our expert team combines forensic investigation, courtroom excellence, and strategic legal counsel to deliver decisive outcomes that protect your interests and resolve disputes effectively.
</p>

<!-- After -->
<p class="text-base md:text-lg text-gray-400 leading-relaxed font-light max-w-xl">
    Facing a legal challenge? Our experienced team provides comprehensive investigation services, strategic counsel, and powerful courtroom representation to protect your rights and achieve the best possible outcome.
</p>
```

#### Updating Hero Section Call-to-Action Buttons

**Current code:**
```html
<a href="https://somda.co.za/contact/" class="btn-gradient px-8 py-4 rounded font-semibold text-center flex items-center justify-center gap-3 smooth-transition">
    <span>Start Your Case</span>
    <span class="material-symbols-rounded">arrow_forward</span>
</a>
```

**How to change the button text:**
1. Replace `Start Your Case` with your preferred text
2. Change the `href="https://somda.co.za/contact/"` to your contact page URL

**Example:**
```html
<!-- Before -->
<a href="https://somda.co.za/contact/" class="btn-gradient px-8 py-4 rounded font-semibold text-center flex items-center justify-center gap-3 smooth-transition">
    <span>Start Your Case</span>
    <span class="material-symbols-rounded">arrow_forward</span>
</a>

<!-- After -->
<a href="https://yoursite.com/contact/" class="btn-gradient px-8 py-4 rounded font-semibold text-center flex items-center justify-center gap-3 smooth-transition">
    <span>Schedule Your Free Consultation</span>
    <span class="material-symbols-rounded">arrow_forward</span>
</a>
```

#### Updating the Hero Info Cards

**Location:** Lines 191-219

These are the four small cards on the right side of the hero section showing key stats.

**Current code for one card:**
```html
<div class="flex flex-col gap-4 p-6 bg-gray-800/50 rounded-xl border border-gray-700 hover:border-primary smooth-transition">
    <span class="material-symbols-rounded text-4xl text-primary">gavel</span>
    <h3 class="font-semibold text-lg">Legal Expertise</h3>
    <p class="text-sm text-gray-400">Decades of courtroom experience</p>
</div>
```

**How to change card content:**
1. Replace `Legal Expertise` with your card title
2. Replace `Decades of courtroom experience` with your description
3. To change the icon, replace `gavel` with another icon name (see icon reference below)

**Icon Reference:** Common icons you can use:
- `gavel` - Gavel/legal
- `search` - Search/investigation
- `verified` - Checkmark/verified
- `security` - Security/protection
- `shield` - Shield/protection
- `trending_up` - Growth/success
- `check_circle` - Completed/done
- `star` - Star/rating

**Example:**
```html
<!-- Before -->
<div class="flex flex-col gap-4 p-6 bg-gray-800/50 rounded-xl border border-gray-700 hover:border-primary smooth-transition">
    <span class="material-symbols-rounded text-4xl text-primary">gavel</span>
    <h3 class="font-semibold text-lg">Legal Expertise</h3>
    <p class="text-sm text-gray-400">Decades of courtroom experience</p>
</div>

<!-- After -->
<div class="flex flex-col gap-4 p-6 bg-gray-800/50 rounded-xl border border-gray-700 hover:border-primary smooth-transition">
    <span class="material-symbols-rounded text-4xl text-primary">verified</span>
    <h3 class="font-semibold text-lg">Award-Winning Team</h3>
    <p class="text-sm text-gray-400">Recognized for excellence and results</p>
</div>
```

---

### Features Section

**Location:** Lines 222-290

This section shows your three main services.

#### Section Header

**Current code:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-6 text-white">
    Comprehensive <span class="text-primary">Services</span>
</h2>
<p class="text-lg text-gray-400 max-w-2xl mx-auto leading-relaxed">
    We offer a complete suite of forensic investigation, legal representation, and strategic counsel services tailored to your specific needs.
</p>
```

**How to change it:**
1. Replace `Comprehensive` with your section title
2. The word in `<span class="text-primary">Services</span>` appears in the accent color
3. Update the description paragraph below

**Example:**
```html
<!-- Before -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-6 text-white">
    Comprehensive <span class="text-primary">Services</span>
</h2>

<!-- After -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-6 text-white">
    What We <span class="text-primary">Offer</span>
</h2>
```

#### Individual Feature Cards

**Current code for one feature:**
```html
<div class="card-hover p-8 md:p-12 bg-gradient-to-br from-gray-800 to-gray-900 rounded-lg border border-gray-700 hover:border-primary smooth-transition">
    <div class="flex flex-col gap-6 h-full">
        <div class="flex items-center justify-center w-16 h-16 bg-gradient-to-br from-primary/20 to-accent/20 rounded-lg">
            <span class="material-symbols-rounded text-3xl text-primary">search</span>
        </div>
        <h3 class="text-2xl font-semibold text-white">Forensic Probes</h3>
        <p class="text-gray-400 leading-relaxed flex-grow">
            Our expert forensic investigators employ cutting-edge techniques and methodologies to uncover critical evidence...
        </p>
        <div class="flex items-center gap-2 text-primary font-semibold pt-4">
            <span>Learn more</span>
            <span class="material-symbols-rounded">arrow_forward</span>
        </div>
    </div>
</div>
```

**How to change feature content:**
1. Replace `search` icon with a different icon if needed
2. Replace `Forensic Probes` with your service name
3. Replace the long description text
4. The "Learn more" link can be updated if needed

**Example:**
```html
<!-- Before -->
<h3 class="text-2xl font-semibold text-white">Forensic Probes</h3>
<p class="text-gray-400 leading-relaxed flex-grow">
    Our expert forensic investigators employ cutting-edge techniques and methodologies to uncover critical evidence...
</p>

<!-- After -->
<h3 class="text-2xl font-semibold text-white">Digital Investigation</h3>
<p class="text-gray-400 leading-relaxed flex-grow">
    We use advanced technology and proven methodologies to uncover digital evidence and cyber-related issues...
</p>
```

---

### Benefits Section

**Location:** Lines 293-360

Shows three key reasons to choose your firm.

**How to update:**

The structure is similar to features. Find each benefit card and update:
1. The icon (in `<span class="material-symbols-rounded text-2xl text-primary">check_circle</span>`)
2. The title (in `<h3>`)
3. The description (in `<p class="text-gray-400">`)

**Example:**
```html
<!-- Before -->
<h3 class="text-xl font-semibold text-white">Resolve Disputes</h3>
<p class="text-gray-400 leading-relaxed">
    Navigate complex conflicts with expert mediation, negotiation, and litigation strategies...
</p>

<!-- After -->
<h3 class="text-xl font-semibold text-white">Fast Resolution</h3>
<p class="text-gray-400 leading-relaxed">
    We work efficiently to resolve your legal matters quickly without compromising quality...
</p>
```

---

### About Us Section

**Location:** Lines 363-396

Company information and background.

**Current code:**
```html
<p class="text-lg text-gray-300 leading-relaxed font-light">
    SOMDA was founded with a singular mission: to deliver exceptional legal and investigative services that make a tangible difference in our clients' lives...
</p>
```

**How to change it:**
1. Replace the entire paragraph text with your company story
2. There are two paragraphs - update both

**Example:**
```html
<!-- Before -->
<p class="text-lg text-gray-300 leading-relaxed font-light">
    SOMDA was founded with a singular mission: to deliver exceptional legal and investigative services...
</p>

<!-- After -->
<p class="text-lg text-gray-300 leading-relaxed font-light">
    Our firm was established to provide comprehensive legal services that truly make a difference for our clients. With over 20 years of combined experience...
</p>
```

---

### Testimonials Section

**Location:** Lines 399-480

Client reviews and feedback.

#### Section Header

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-6 text-white">
    Client <span class="text-primary">Testimonials</span>
</h2>
```

**How to change it:**
Simply replace the text following the same pattern as other section headers.

#### Individual Testimonial Cards

**Current code for one testimonial:**
```html
<div class="card-hover p-8 bg-gradient-to-br from-gray-800 to-gray-900 rounded-lg border border-gray-700 hover:border-primary smooth-transition flex flex-col gap-6">
    <div class="flex gap-1">
        <span class="material-symbols-rounded text-xl text-accent">star</span>
        <span class="material-symbols-rounded text-xl text-accent">star</span>
        <span class="material-symbols-rounded text-xl text-accent">star</span>
        <span class="material-symbols-rounded text-xl text-accent">star</span>
        <span class="material-symbols-rounded text-xl text-accent">star</span>
    </div>
    <p class="text-gray-300 leading-relaxed flex-grow">
        "SOMDA's forensic investigation completely turned my case around..."
    </p>
    <div class="border-t border-gray-700 pt-4">
        <p class="font-semibold text-white">Michael Chen</p>
        <p class="text-sm text-gray-400">Business Owner</p>
    </div>
</div>
```

**How to change testimonials:**
1. Keep the five stars (or change the number by adding/removing `<span>` lines)
2. Replace the quoted testimonial text
3. Replace `Michael Chen` with the client name
4. Replace `Business Owner` with their title/role

**Example:**
```html
<!-- Before -->
<p class="text-gray-300 leading-relaxed flex-grow">
    "SOMDA's forensic investigation completely turned my case around. Their meticulous approach uncovered evidence that proved my innocence..."
</p>
<div class="border-t border-gray-700 pt-4">
    <p class="font-semibold text-white">Michael Chen</p>
    <p class="text-sm text-gray-400">Business Owner</p>
</div>

<!-- After -->
<p class="text-gray-300 leading-relaxed flex-grow">
    "Working with this team was an excellent experience. They provided clear guidance and achieved the best possible outcome for my case..."
</p>
<div class="border-t border-gray-700 pt-4">
    <p class="font-semibold text-white">Jennifer Smith</p>
    <p class="text-sm text-gray-400">Executive Director</p>
</div>
```

---

### FAQ Section

**Location:** Lines 483-596

Frequently asked questions with expandable answers.

#### Section Header

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-6 text-white">
    Frequently Asked <span class="text-primary">Questions</span>
</h2>
```

#### Individual FAQ Items

**Current code for one FAQ:**
```html
<div class="faq-item border border-gray-700 rounded-lg overflow-hidden bg-gradient-to-br from-gray-800 to-gray-900 hover:border-primary smooth-transition">
    <button class="faq-question w-full px-8 py-6 flex items-center justify-between gap-4 hover:bg-gray-700/50 smooth-transition cursor-pointer">
        <h3 class="text-lg md:text-xl font-semibold text-white text-left">
            What types of cases does SOMDA handle?
        </h3>
        <span class="faq-icon material-symbols-rounded text-2xl text-primary flex-shrink-0">expand_more</span>
    </button>
    <div class="faq-answer hidden px-8 pb-6 text-gray-400 leading-relaxed">
        <p>
            SOMDA specializes in a broad range of legal and investigative matters including civil litigation...
        </p>
    </div>
</div>
```

**How to change FAQ content:**
1. Replace the question text in the `<h3>` tag
2. Replace the answer text in the `<p>` tag inside `faq-answer`

**Example:**
```html
<!-- Before -->
<h3 class="text-lg md:text-xl font-semibold text-white text-left">
    What types of cases does SOMDA handle?
</h3>
...
<p>
    SOMDA specializes in a broad range of legal and investigative matters...
</p>

<!-- After -->
<h3 class="text-lg md:text-xl font-semibold text-white text-left">
    How much does your legal representation cost?
</h3>
...
<p>
    We offer flexible fee structures including hourly rates, flat fees, and contingency arrangements...
</p>
```

---

### Final CTA Section

**Location:** Lines 599-629

The "Ready to Protect Your Rights?" section before the footer.

**How to change:**
1. Update the main heading
2. Update the description paragraph
3. Update button texts and links

**Example:**
```html
<!-- Before -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-8 text-white">
    Ready to Protect Your <span class="text-primary">Rights</span>?
</h2>

<!-- After -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold mb-8 text-white">
    Let's Resolve Your <span class="text-primary">Case</span>
</h2>
```

---

### Footer Section

**Location:** Lines 676-750

The bottom section with company info, links, and contact details.

#### Footer Company Description

```html
<p class="text-gray-400 leading-relaxed text-sm">
    Professional legal and investigative services dedicated to protecting your rights and achieving exceptional outcomes.
</p>
```

**How to change it:**
Simply replace the text with your company description.

#### Footer Links

The footer has multiple link sections:

**Services Links:**
```html
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Forensic Investigations</a></li>
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Court Affidavits</a></li>
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Legal Counsel</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-primary smooth-transition">Case Strategy</a></li>
```

**How to change footer links:**
1. Replace the link text (e.g., `Forensic Investigations`)
2. Update the `href` if needed (e.g., change `#features` to link elsewhere)

**Example:**
```html
<!-- Before -->
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Forensic Investigations</a></li>

<!-- After -->
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Digital Forensics</a></li>
```

#### Footer Contact Information

```html
<a href="mailto:info@somda.co.za" class="text-white hover:text-primary smooth-transition">info@somda.co.za</a>
```

**How to change email:**
1. Update the email in `href="mailto:info@somda.co.za"`
2. Update the displayed email text

**Example:**
```html
<!-- Before -->
<a href="mailto:info@somda.co.za" class="text-white hover:text-primary smooth-transition">info@somda.co.za</a>

<!-- After -->
<a href="mailto:contact@yourfirm.com" class="text-white hover:text-primary smooth-transition">contact@yourfirm.com</a>
```

#### Copyright Text

```html
<p class="text-gray-400 text-sm leading-relaxed">
    © 2025 SOMDA Legal & Investigative Services. All rights reserved...
</p>
```

**How to change it:**
1. Update the year (2025)
2. Update the company name
3. Update the description

**Example:**
```html
<!-- Before -->
© 2025 SOMDA Legal & Investigative Services. All rights reserved.

<!-- After -->
© 2025 Your Law Firm Name. All rights reserved.
```

---

## Working with Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework that uses class names to style elements. Understanding these classes will help you maintain the design while making changes.

### What is Tailwind CSS?

Instead of writing traditional CSS, Tailwind uses pre-made classes. For example:
- `text-white` = white text
- `bg-gray-900` = dark gray background
- `px-8` = horizontal padding

### Common Tailwind Classes Used in This Landing Page

#### Text Styling

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | White text color | `<p class="text-white">White text</p>` |
| `text-gray-300` | Light gray text | `<p class="text-gray-300">Light gray</p>` |
| `text-gray-400` | Medium gray text | `<p class="text-gray-400">Medium gray</p>` |
| `text-primary` | Accent color (orange/red) | `<p class="text-primary">Accent text</p>` |
| `text-accent` | Secondary accent (gold) | `<p class="text-accent">Gold text</p>` |
| `text-xl` | Extra large text | `<p class="text-xl">Large</p>` |
| `text-lg` | Large text | `<p class="text-lg">Large</p>` |
| `text-base` | Normal text | `<p class="text-base">Normal</p>` |
| `text-sm` | Small text | `<p class="text-sm">Small</p>` |
| `font-semibold` | Semi-bold font weight | `<p class="font-semibold">Bold</p>` |
| `font-light` | Light font weight | `<p class="font-light">Light</p>` |

#### Background Colors

| Class | What It Does |
|-------|-------------|
| `bg-gray-900` | Very dark gray background |
| `bg-gray-800` | Dark gray background |
| `bg-gray-700` | Medium-dark gray background |
| `bg-white` | White background |
| `bg-primary` | Accent color background |

#### Spacing (Padding & Margin)

| Class | What It Does | Measurement |
|-------|-------------|------------|
| `px-8` | Horizontal padding (left & right) | 32px |
| `py-6` | Vertical padding (top & bottom) | 24px |
| `p-8` | Padding on all sides | 32px |
| `mb-6` | Margin bottom | 24px |
| `gap-6` | Space between flex items | 24px |
| `gap-8` | Space between flex items | 32px |

#### Sizing

| Class | What It Does |
|-------|-------------|
| `w-16` | Width of 64px |
| `h-16` | Height of 64px |
| `w-full` | 100% width |
| `max-w-7xl` | Maximum width (1280px) |
| `max-w-4xl` | Maximum width (896px) |

#### Borders & Shadows

| Class | What It Does |
|-------|-------------|
| `border` | 1px border |
| `border-gray-700` | Gray border color |
| `border-primary` | Accent color border |
| `rounded` | Rounded corners |
| `rounded-lg` | More rounded corners |
| `rounded-2xl` | Very rounded corners |
| `shadow-lg` | Large shadow |
| `shadow-2xl` | Extra large shadow |

#### Display & Layout

| Class | What It Does |
|-------|-------------|
| `flex` | Display as flexbox |
| `grid` | Display as grid |
| `hidden` | Hide element |
| `block` | Display as block |
| `inline-block` | Display inline-block |
| `flex-col` | Flex column direction |
| `items-center` | Center items vertically |
| `justify-center` | Center items horizontally |
| `gap-4` | Space between flex/grid items |

#### Responsive Design

These classes add prefixes for different screen sizes:

| Prefix | Screen Size | Usage |
|--------|------------|-------|
| (none) | Mobile first (all sizes) | `text-lg` |
| `md:` | Medium screens (768px+) | `md:text-2xl` |
| `lg:` | Large screens (1024px+) | `lg:text-3xl` |
| `sm:` | Small screens (640px+) | `sm:flex-row` |

**Example - Responsive Text:**
```html
<!-- This text is: -->
<!-- - text-4xl on mobile -->
<!-- - text-5xl on medium screens (md:) -->
<!-- - text-6xl on large screens (lg:) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold">
    Professional Legal Services
</h1>
```

### Custom Classes Used in This Page

The page also uses custom CSS classes defined in the `<style>` section (lines 28-67):

#### Custom Color Classes

```css
.text-primary {
    color: #FF5A5F;  /* Orange/Red color */
}

.text-accent {
    color: #FFD166;  /* Gold color */
}

.gradient-primary {
    background: linear-gradient(135deg, #FF5A5F 0%, #FFD166 100%);
    /* Gradient from red to gold */
}
```

#### Custom Animation Classes

```css
.smooth-transition {
    transition: all 300ms ease-out;
    /* Makes hover effects smooth */
}

.btn-gradient:hover {
    transform: scale(1.05);
    /* Button grows 5% on hover */
    box-shadow: 0 20px 25px -5px rgba(255, 90, 95, 0.3);
    /* Adds shadow on hover */
}

.card-hover:hover {
    transform: scale(1.05);
    /* Cards grow on hover */
    box-shadow: 0 25px 50px -12px rgba(255, 90, 95, 0.2);
}
```

### How to Modify Tailwind Classes While Maintaining Design

#### Changing Text Size

**Current:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold">
    Main Headline
</h1>
```

**To make text smaller on mobile:**
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-semibold">
    Main Headline
</h1>
```

**Size progression guide:**
- `text-2xl` = 24px (small)
- `text-3xl` = 30px (medium)
- `text-4xl` = 36px (large)
- `text-5xl` = 48px (extra large)
- `text-6xl` = 60px (huge)

#### Changing Spacing

**Current:**
```html
<div class="p-8 md:p-12 bg-gradient-to-br from-gray-800 to-gray-900">
    Content
</div>
```

**To add more padding:**
```html
<div class="p-12 md:p-16 bg-gradient-to-br from-gray-800 to-gray-900">
    Content
</div>
```

**Padding values:**
- `p-4` = 16px padding
- `p-6` = 24px padding
- `p-8` = 32px padding
- `p-12` = 48px padding

#### Changing Background Colors

**Current:**
```html
<div class="bg-gray-800">
    Content
</div>
```

**To change to darker background:**
```html
<div class="bg-gray-900">
    Content
</div>
```

**Color shades available:**
- `bg-gray-700` = lighter gray
- `bg-gray-800` = medium gray
- `bg-gray-900` = very dark gray

#### Adding More Rounded Corners

**Current:**
```html
<div class="rounded-lg">
    Content
</div>
```

**To make corners more rounded:**
```html
<div class="rounded-2xl">
    Content
</div>
```

**Roundness values:**
- `rounded` = 4px
- `rounded-lg` = 8px
- `rounded-2xl` = 16px
- `rounded-full` = completely circular

### Important: Maintaining Responsive Design

When modifying Tailwind classes, always maintain the responsive prefixes:

**Good - Maintains responsiveness:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl">
    Responsive Heading
</h2>
```

**Bad - Not responsive:**
```html
<h2 class="text-5xl">
    This is too big on mobile!
</h2>
```

**Keep the pattern:**
- Base class (mobile) = `text-3xl`
- Medium screen = `md:text-4xl`
- Large screen = `lg:text-5xl`

---

## Fixing and Managing Links

Links are critical to your website's functionality. This section shows you how to find, update, and fix all links on the page.

### Understanding Links

An HTML link looks like this:
```html
<a href="https://example.com">Click Here</a>
```

Breaking it down:
- `<a>` = link tag
- `href="https://example.com"` = where the link goes
- `Click Here` = the visible text
- `</a>` = closes the link

### Types of Links on This Page

#### 1. Internal Navigation Links (Jump to Sections)

These links jump to different sections on the same page using `#` symbols.

**Example:**
```html
<a href="#features">Services</a>
```

This jumps to the section with `id="features"`.

**Current internal links:**
| Link Text | Jumps To | ID Location |
|-----------|----------|-------------|
| Services | Features section | `id="features"` (line 222) |
| Benefits | Benefits section | `id="benefits"` (line 293) |
| Testimonials | Testimonials section | `id="testimonials"` (line 399) |
| FAQ | FAQ section | `id="faq"` (line 483) |

#### 2. External Links (External Websites)

These links go to other websites using full URLs.

**Example:**
```html
<a href="https://somda.co.za/contact/">Get Started</a>
```

#### 3. Email Links

These links open the user's email client.

**Example:**
```html
<a href="mailto:info@somda.co.za">Email Us</a>
```

#### 4. Page Links (Within Your Site)

These link to other pages in your website.

**Example:**
```html
<a href="privacy.html">Privacy Policy</a>
```

### All Links Currently in the Page

Here's a complete list of every link in the landing page:

#### Header Navigation Links

**Location:** Lines 110-116

```html
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>
<a href="#benefits" class="text-gray-300 hover:text-primary smooth-transition">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-primary smooth-transition">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-primary smooth-transition">FAQ</a>
```

**Status:** ✅ These work correctly - they jump to sections on the page

#### Header "Get Started" Button

**Location:** Lines 119-121

```html
<a href="https://somda.co.za/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
    Get Started
</a>
```

**Status:** ⚠️ **NEEDS UPDATING** - Replace `https://somda.co.za/contact/` with your contact page URL

#### Mobile Menu Links

**Location:** Lines 128-135

```html
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition font-medium">Services</a>
<a href="#benefits" class="text-gray-300 hover:text-primary smooth-transition font-medium">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-primary smooth-transition font-medium">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-primary smooth-transition font-medium">FAQ</a>
<a href="https://somda.co.za/contact/" class="btn-gradient px-8 py-3 rounded text-center font-semibold hover:shadow-lg smooth-transition">
    Get Started
</a>
```

**Status:** ✅ Internal links work | ⚠️ Contact link needs updating

#### Hero Section Buttons

**Location:** Lines 172-185

```html
<a href="https://somda.co.za/contact/" class="btn-gradient px-8 py-4 rounded font-semibold text-center flex items-center justify-center gap-3 smooth-transition">
    <span>Start Your Case</span>
    <span class="material-symbols-rounded">arrow_forward</span>
</a>
<button class="px-8 py-4 rounded border-2 border-primary text-primary hover:bg-primary hover:text-white smooth-transition font-semibold flex items-center justify-center gap-3">
    <span>Learn More</span>
    <span class="material-symbols-rounded">info</span>
</button>
```

**Status:** ⚠️ First link needs updating | ⚠️ Second button has no link

#### Footer Service Links

**Location:** Lines 707-711

```html
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Forensic Investigations</a></li>
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Court Affidavits</a></li>
<li><a href="#features" class="text-gray-400 hover:text-primary smooth-transition">Legal Counsel</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-primary smooth-transition">Case Strategy</a></li>
```

**Status:** ✅ These work correctly

#### Footer Company Links

**Location:** Lines 717-721

```html
<li><a href="#" class="text-gray-400 hover:text-primary smooth-transition">About Us</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-primary smooth-transition">Testimonials</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-primary smooth-transition">Blog</a></li>
<li><a href="#" class="text-gray-400 hover:text-primary smooth-transition">Contact</a></li>
```

**Status:** ⚠️ "About Us" link goes to `#` (nowhere) | ⚠️ "Contact" link goes to `#` (nowhere) | ✅ Blog link references blog.html

#### Footer Policy Links

**Location:** Lines 748-750

```html
<a href="privacy.html" class="text-gray-400 hover:text-primary smooth-transition text-sm font-medium">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-primary smooth-transition text-sm font-medium">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-primary smooth-transition text-sm font-medium">Blog</a>
```

**Status:** ⚠️ Links to privacy.html and terms.html (files don't exist yet) | ✅ Blog link references blog.html

#### Footer Email Link

**Location:** Lines 732-735

```html
<a href="mailto:info@somda.co.za" class="text-white hover:text-primary smooth-transition">info@somda.co.za</a>
```

**Status:** ⚠️ **NEEDS UPDATING** - Replace email with your actual email address

### Step-by-Step: How to Fix Links

#### Step 1: Update Contact Page Links

You need to replace all instances of `https://somda.co.za/contact/` with your actual contact page URL.

**Find these 4 locations:**

1. **Header desktop button** (Line 120)
```html
<!-- Before -->
<a href="https://somda.co.za/contact/">Get Started</a>

<!-- After - Replace with YOUR contact page URL -->
<a href="https://yourwebsite.com/contact/">Get Started</a>
```

2. **Mobile menu button** (Line 134)
```html
<!-- Before -->
<a href="https://somda.co.za/contact/">Get Started</a>

<!-- After -->
<a href="https://yourwebsite.com/contact/">Get Started</a>
```

3. **Hero section main button** (Line 173)
```html
<!-- Before -->
<a href="https://somda.co.za/contact/">Start Your Case</a>

<!-- After -->
<a href="https://yourwebsite.com/contact/">Start Your Case</a>
```

4. **Final CTA section button** (Line 607)
```html
<!-- Before -->
<a href="https://somda.co.za/contact/">Start Your Case Today</a>

<!-- After -->
<a href="https://yourwebsite.com/contact/">Start Your Case Today</a>
```

**How to find and replace all at once:**
- Open the HTML file in a text editor
- Press Ctrl+H (Windows) or Cmd+H (Mac)
- In "Find" field: `https://somda.co.za/contact/`
- In "Replace" field: `https://yourwebsite.com/contact/`
- Click "Replace All"

#### Step 2: Update Email Address

Replace `info@somda.co.za` with your actual email address.

**Locations:**
1. **Footer email link** (Line 733)
```html
<!-- Before -->
<a href="mailto:info@somda.co.za">info@somda.co.za</a>

<!-- After -->
<a href="mailto:your-email@yoursite.com">your-email@yoursite.com</a>
```

**Important:** Keep `mailto:` at the beginning - this tells the browser to open the email client.

#### Step 3: Fix "About Us" Link

Currently, this link goes nowhere (`href="#"`). You have two options:

**Option A: Link to an About page (if you have one)**
```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-primary smooth-transition">About Us</a></li>

<!-- After -->
<li><a href="about.html" class="text-gray-400 hover:text-primary smooth-transition">About Us</a></li>
```

**Option B: Link to the About section on this page**
```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-primary smooth-transition">About Us</a></li>

<!-- After -->
<li><a href="#about" class="text-gray-400 hover:text-primary smooth-transition">About Us</a></li>
```

Then add an ID to the About section (Line 363):
```html
<!-- Before -->
<section class="py-20 md:py-32 px-8 md:px-16 bg-gradient-to-b from-gray-900 to-gray-800">

<!-- After -->
<section id="about" class="py-20 md:py-32 px-8 md:px-16 bg-gradient-to-b from-gray-900 to-gray-800">
```

#### Step 4: Fix "Contact" Link

Currently, this link goes nowhere. Update it to point to your contact page:

```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-primary smooth-transition">Contact</a></li>

<!-- After -->
<li><a href="https://yourwebsite.com/contact/" class="text-gray-400 hover:text-primary smooth-transition">Contact</a></li>
```

#### Step 5: Update Social Media Links

Currently, these links go to `#` (nowhere). Update them to your social media profiles:

**Location:** Lines 701-709

```html
<!-- Before -->
<a href="#" class="flex items-center justify-center w-10 h-10 bg-gray-700 hover:bg-primary rounded-lg smooth-transition" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>

<!-- After -->
<a href="https://facebook.com/yourpage" class="flex items-center justify-center w-10 h-10 bg-gray-700 hover:bg-primary rounded-lg smooth-transition" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Do the same for:**
- Twitter: `https://twitter.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`

#### Step 6: Verify Blog and Policy Links

These links reference pages that should exist in your project folder:

```html
<a href="blog.html">Blog</a>
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
```

**Make sure you have these files:**
- `blog.html` (if you're using the blog link)
- `privacy.html` (required)
- `terms.html` (required)

If these files don't exist yet, either:
1. Create them (see next section)
2. Comment out the links by changing them to `href="#"`

### Common Link Problems & Solutions

#### Problem: Link doesn't work

**Possible causes:**
1. Typo in the URL
2. Missing `http://` or `https://`
3. File doesn't exist (for internal links)

**Solution:**
- Check spelling of the URL
- Make sure external links start with `http://` or `https://`
- Make sure files exist in your project folder

#### Problem: Link opens in same tab, but I want it to open in new tab

**Solution:** Add `target="_blank"` to the link

```html
<!-- Before -->
<a href="https://example.com">External Link</a>

<!-- After -->
<a href="https://example.com" target="_blank">External Link</a>
```

#### Problem: Email link doesn't work

**Possible causes:**
1. Missing `mailto:` at the beginning
2. Typo in email address

**Solution:**
```html
<!-- Correct -->
<a href="mailto:your-email@example.com">Email Us</a>

<!-- Incorrect -->
<a href="your-email@example.com">Email Us</a>
```

---

## Adding Privacy and Terms Pages

Privacy and Terms pages are legally important for your website. This section shows you how to create them and link them properly.

### Why You Need These Pages

1. **Legal requirement** - Most jurisdictions require privacy policies
2. **Trust** - Clients want to know how their data is handled
3. **Professional appearance** - Shows you're a legitimate business
4. **SEO benefit** - Search engines favor sites with proper policies

### Step 1: Create the Privacy Policy Page

#### Create a New File

1. Open your text editor
2. Create a new file
3. Save it as `privacy.html` in your project folder (same folder as `index.html`)

#### Add Basic HTML Structure

Copy this code into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Professional Legal & Investigative Services">
    <meta name="author" content="SOMDA">
    <title>Privacy Policy | Professional Legal Services</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    <style>
        * {
            font-family: 'Poppins', sans-serif;
        }
        
        .text-primary {
            color: #FF5A5F;
        }
        
        .smooth-transition {
            transition: all 300ms ease-out;
        }
        
        .btn-gradient {
            background: linear-gradient(135deg, #FF5A5F 0%, #FFD166 100%);
            color: white;
        }
        
        .btn-gradient:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 25px -5px rgba(255, 90, 95, 0.3);
        }
        
        .header-sticky {
            position: sticky;
            top: 0;
            z-index: 50;
            backdrop-filter: blur(10px);
            background: rgba(26, 26, 26, 0.95);
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header (Same as index.html) -->
    <header class="header-sticky border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <span class="material-symbols-rounded text-3xl text-primary">shield</span>
                <span class="text-2xl font-semibold text-white">SOMDA</span>
            </div>
            
            <div class="hidden md:flex items-center gap-12">
                <a href="index.html" class="text-gray-300 hover:text-primary smooth-transition">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-primary smooth-transition">FAQ</a>
            </div>
            
            <a href="https://yourwebsite.com/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
                Contact
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-8 md:px-16 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-semibold mb-4 text-white">Privacy Policy</h1>
        <p class="text-gray-400 mb-12">Last updated: January 2025</p>

        <!-- Introduction -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Introduction</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                SOMDA Legal & Investigative Services ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
            </p>
            <p class="text-gray-300 leading-relaxed">
                Please read this Privacy Policy carefully. If you do not agree with our policies and practices, please do not use our site. By accessing and using this website, you acknowledge that you have read, understood, and agree to be bound by all the provisions of this Privacy Policy.
            </p>
        </section>

        <!-- Information We Collect -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Information We Collect</h2>
            
            <h3 class="text-xl font-semibold mb-3 text-gray-100 mt-6">Personal Information You Provide</h3>
            <p class="text-gray-300 leading-relaxed mb-4">
                We collect information you voluntarily provide, including:
            </p>
            <ul class="list-disc list-inside text-gray-300 space-y-2 mb-6">
                <li>Name and contact information (email, phone number)</li>
                <li>Case details and legal matters you share with us</li>
                <li>Payment information for services rendered</li>
                <li>Any other information you choose to provide</li>
            </ul>

            <h3 class="text-xl font-semibold mb-3 text-gray-100">Automatically Collected Information</h3>
            <p class="text-gray-300 leading-relaxed mb-4">
                When you visit our website, we automatically collect:
            </p>
            <ul class="list-disc list-inside text-gray-300 space-y-2">
                <li>IP address and browser type</li>
                <li>Pages visited and time spent on each page</li>
                <li>Device information and operating system</li>
                <li>Referring website and pages visited after leaving our site</li>
            </ul>
        </section>

        <!-- How We Use Information -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">How We Use Your Information</h2>
            <p class="text-gray-300 leading-relaxed mb-4">We use the information we collect to:</p>
            <ul class="list-disc list-inside text-gray-300 space-y-2">
                <li>Provide and improve our legal and investigative services</li>
                <li>Communicate with you about your case or inquiries</li>
                <li>Process payments and send billing information</li>
                <li>Respond to your questions and provide customer support</li>
                <li>Send promotional materials (only with your consent)</li>
                <li>Comply with legal obligations and regulations</li>
                <li>Protect against fraud and maintain security</li>
            </ul>
        </section>

        <!-- Data Security -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Data Security</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                We implement appropriate technical, administrative, and physical security measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet or electronic storage is completely secure.
            </p>
            <p class="text-gray-300 leading-relaxed">
                While we strive to protect your personal information, we cannot guarantee its absolute security. You acknowledge that you provide information at your own risk.
            </p>
        </section>

        <!-- Third-Party Disclosure -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Third-Party Disclosure</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                We do not sell, trade, or rent your personal information to third parties. We may share information only:
            </p>
            <ul class="list-disc list-inside text-gray-300 space-y-2">
                <li>With service providers who assist us in operating our website and conducting our business</li>
                <li>When required by law or legal process</li>
                <li>To protect our rights and the safety of our clients</li>
                <li>With your explicit consent</li>
            </ul>
        </section>

        <!-- Your Rights -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Your Privacy Rights</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                Depending on your jurisdiction, you may have the right to:
            </p>
            <ul class="list-disc list-inside text-gray-300 space-y-2">
                <li>Access the personal information we hold about you</li>
                <li>Request correction of inaccurate information</li>
                <li>Request deletion of your information</li>
                <li>Opt-out of marketing communications</li>
            </ul>
            <p class="text-gray-300 leading-relaxed mt-4">
                To exercise these rights, please contact us at info@yourdomain.com.
            </p>
        </section>

        <!-- Contact Information -->
        <section class="mb-12 p-8 bg-gray-800 rounded-lg border border-gray-700">
            <h2 class="text-2xl font-semibold mb-4 text-white">Contact Us</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                If you have questions about this Privacy Policy or our privacy practices, please contact us:
            </p>
            <div class="text-gray-300">
                <p class="mb-2"><strong>Email:</strong> <a href="mailto:info@yourdomain.com" class="text-primary hover:underline">info@yourdomain.com</a></p>
                <p class="mb-2"><strong>Phone:</strong> Your Phone Number</p>
                <p><strong>Address:</strong> Your Physical Address</p>
            </div>
        </section>

        <!-- Policy Updates -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Policy Updates</h2>
            <p class="text-gray-300 leading-relaxed">
                We may update this Privacy Policy from time to time. Changes will be posted on this page with an updated "Last Updated" date. Your continued use of our website following the posting of revised Privacy Policy means that you accept and agree to the changes.
            </p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 border-t border-gray-700 py-12 px-8 md:px-16 mt-16">
        <div class="max-w-4xl mx-auto text-center">
            <p class="text-gray-400 text-sm mb-4">
                © 2025 SOMDA Legal & Investigative Services. All rights reserved.
            </p>
            <div class="flex justify-center gap-6">
                <a href="index.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Terms</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

#### Create Another New File

1. Save a new file as `terms.html` in your project folder

#### Add Basic HTML Structure

Copy this code into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Professional Legal & Investigative Services">
    <meta name="author" content="SOMDA">
    <title>Terms of Service | Professional Legal Services</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    <style>
        * {
            font-family: 'Poppins', sans-serif;
        }
        
        .text-primary {
            color: #FF5A5F;
        }
        
        .smooth-transition {
            transition: all 300ms ease-out;
        }
        
        .btn-gradient {
            background: linear-gradient(135deg, #FF5A5F 0%, #FFD166 100%);
            color: white;
        }
        
        .btn-gradient:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 25px -5px rgba(255, 90, 95, 0.3);
        }
        
        .header-sticky {
            position: sticky;
            top: 0;
            z-index: 50;
            backdrop-filter: blur(10px);
            background: rgba(26, 26, 26, 0.95);
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header -->
    <header class="header-sticky border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <span class="material-symbols-rounded text-3xl text-primary">shield</span>
                <span class="text-2xl font-semibold text-white">SOMDA</span>
            </div>
            
            <div class="hidden md:flex items-center gap-12">
                <a href="index.html" class="text-gray-300 hover:text-primary smooth-transition">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-primary smooth-transition">FAQ</a>
            </div>
            
            <a href="https://yourwebsite.com/contact/" class="hidden md:block btn-gradient px-8 py-3 rounded hover:shadow-lg smooth-transition font-semibold">
                Contact
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-8 md:px-16 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-semibold mb-4 text-white">Terms of Service</h1>
        <p class="text-gray-400 mb-12">Last updated: January 2025</p>

        <!-- Agreement -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Agreement to Terms</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                By accessing and using this website and our services, you accept and agree to be bound by and comply with these Terms of Service. If you do not agree to abide by the above, please do not use this service.
            </p>
            <p class="text-gray-300 leading-relaxed">
                We reserve the right to make changes to these Terms of Service at any time and for any reason. We will alert you about any changes by updating the "Last Updated" date of these Terms of Service. Any changes or modifications will be effective immediately upon posting to the website.
            </p>
        </section>

        <!-- Use License -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Use License</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                Permission is granted to temporarily download one copy of the materials (information or software) on SOMDA's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
            </p>
            <ul class="list-disc list-inside text-gray-300 space-y-2">
                <li>Modify or copy the materials</li>
                <li>Use the materials for any commercial purpose or for any public display</li>
                <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                <li>Remove any copyright or other proprietary notations from the materials</li>
                <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                <li>Violate any applicable laws or regulations</li>
            </ul>
        </section>

        <!-- Disclaimer -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Disclaimer</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                The materials on SOMDA's website are provided on an 'as is' basis. SOMDA makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
            </p>
            <p class="text-gray-300 leading-relaxed">
                Further, SOMDA does not warrant or make any representations concerning the accuracy, likely results, or reliability of the use of the materials on its Internet web site or otherwise relating to such materials or on any sites linked to this site.
            </p>
        </section>

        <!-- Limitations of Liability -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Limitations of Liability</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                In no event shall SOMDA or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on SOMDA's website, even if SOMDA or a SOMDA authorized representative has been notified orally or in writing of the possibility of such damage.
            </p>
        </section>

        <!-- Accuracy of Materials -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Accuracy of Materials</h2>
            <p class="text-gray-300 leading-relaxed">
                The materials appearing on SOMDA's website could include technical, typographical, or photographic errors. SOMDA does not warrant that any of the materials on our website are accurate, complete, or current. SOMDA may make changes to the materials contained on its website at any time without notice.
            </p>
        </section>

        <!-- Links -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Links</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                SOMDA has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by SOMDA of the site. Use of any such linked website is at the user's own risk.
            </p>
            <p class="text-gray-300 leading-relaxed">
                If you believe that your work has been copied in a way that constitutes copyright infringement, please provide SOMDA with the following information: your name, address, telephone number, email address, and a detailed description of the copyrighted work and how it has been infringed.
            </p>
        </section>

        <!-- Modifications -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Modifications</h2>
            <p class="text-gray-300 leading-relaxed">
                SOMDA may revise these terms of service for our website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
            </p>
        </section>

        <!-- Governing Law -->
        <section class="mb-12">
            <h2 class="text-2xl font-semibold mb-4 text-white">Governing Law</h2>
            <p class="text-gray-300 leading-relaxed">
                These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction], and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
            </p>
        </section>

        <!-- Contact Information -->
        <section class="mb-12 p-8 bg-gray-800 rounded-lg border border-gray-700">
            <h2 class="text-2xl font-semibold mb-4 text-white">Contact Us</h2>
            <p class="text-gray-300 leading-relaxed mb-4">
                If you have any questions about these Terms of Service, please contact us:
            </p>
            <div class="text-gray-300">
                <p class="mb-2"><strong>Email:</strong> <a href="mailto:info@yourdomain.com" class="text-primary hover:underline">info@yourdomain.com</a></p>
                <p class="mb-2"><strong>Phone:</strong> Your Phone Number</p>
                <p><strong>Address:</strong> Your Physical Address</p>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 border-t border-gray-700 py-12 px-8 md:px-16 mt-16">
        <div class="max-w-4xl mx-auto text-center">
            <p class="text-gray-400 text-sm mb-4">
                © 2025 SOMDA Legal & Investigative Services. All rights reserved.
            </p>
            <div class="flex justify-center gap-6">
                <a href="index.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-primary smooth-transition text-sm">Terms</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Customize the Policy Pages

#### Update Company Information

In both `privacy.html` and `terms.html`, find and replace:

1. **Email address:**
```html
<!-- Find this -->
<a href="mailto:info@yourdomain.com">info@yourdomain.com</a>

<!-- Replace with your email -->
<a href="mailto:your-actual-email@yoursite.com">your-actual-email@yoursite.com</a>
```

2. **Phone number:**
```html
<!-- Find this -->
<p><strong>Phone:</strong> Your Phone Number</p>

<!-- Replace with your phone -->
<p><strong>Phone:</strong> +1 (555) 123-4567</p>
```

3. **Physical address:**
```html
<!-- Find this -->
<p><strong>Address:</strong> Your Physical Address</p>

<!-- Replace with your address -->
<p><strong>Address:</strong> 123 Law Street, City, State 12345</p>
```

4. **Contact page URL** (in header):
```html
<!-- Find this -->
<a href="https://yourwebsite.com/contact/">Contact</a>

<!-- Replace with your actual contact page -->
<a href="https://youractualsite.com/contact/">Contact</a>
```

5. **Jurisdiction** (in terms.html):
```html
<!-- Find this -->
These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction]

<!-- Replace with your jurisdiction -->
These terms and conditions are governed by and construed in accordance with the laws of South Africa
```

### Step 4: Link Policies from Main Page

Now link the privacy and terms pages from your main `index.html` file.

#### Verify Footer Links

The footer already has these links (lines 748-750):

```html
<a href="privacy.html" class="text-gray-400 hover:text-primary smooth-transition text-sm font-medium">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-primary smooth-transition text-sm font-medium">Terms of Service</a>
```

**These should already work!** Just verify they're there.

#### Add Links to Header (Optional)

If you want to add policy links to the header navigation, add them after FAQ:

```html
<!-- Current header navigation -->
<a href="#features" class="text-gray-300 hover:text-primary smooth-transition">Services</a>
<a href="#benefits" class="text-gray-300 hover:text-primary smooth-transition">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-primary smooth-transition">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-primary smooth-transition">FAQ</a>

<!-- Add these new lines -->
<a href="privacy.html" class="text-gray-300 hover:text-primary smooth-transition">Privacy</a>
<a href="terms.html" class="text-gray-300 hover:text-primary smooth-transition">Terms</a>
```

### Step 5: Test the Links

1. Save all three files (`index.html`, `privacy.html`, `terms.html`)
2. Open `index.html` in your browser
3. Click the "Privacy Policy" link in the footer
4. You should see the privacy policy page
5. Click "Home" to go back
6. Click "Terms" link to verify terms page works

### Important: Customize the Content

The policies provided are templates. **You must customize them** with your actual information:

- [ ] Update company name (currently "SOMDA")
- [ ] Update email address
- [ ] Update phone number
- [ ] Update physical address
- [ ] Update jurisdiction (for terms)
- [ ] Review and modify policy text to match your actual practices
- [ ] Add any specific terms relevant to your business

**Note:** These are templates. For legal compliance, consider having an attorney review your policies.

---

## Color Customization

The landing page uses a specific color scheme. This section shows you how to customize it.

### Current Color Scheme

The page uses these main colors:

| Color Name | Hex Code | Usage |
|-----------|----------|-------|
| Primary (Red/Orange) | `#FF5A5F` | Buttons, accents, hover states |
| Accent (Gold) | `#FFD166` | Secondary accents, highlights |
| Dark Background | `#1A1A1A` | Dark sections |
| Gray 900 | `#111827` | Main background |
| Gray 800 | `#1F2937` | Card backgrounds |
| Gray 700 | `#374151` | Borders |
| White | `#FFFFFF` | Text |
| Gray 300 | `#D1D5DB` | Light text |
| Gray 400 | `#9CA3AF` | Medium text |

### Where Colors Are Defined

Colors are defined in two places:

#### 1. Custom CSS (Lines 28-67)

```css
.gradient-primary {
    background: linear-gradient(135deg, #FF5A5F 0%, #FFD166 100%);
}

.text-primary {
    color: #FF5A5F;
}

.text-accent {
    color: #FFD166;
}
```

#### 2. Tailwind Classes (Throughout HTML)

```html
<span class="text-primary">Services</span>  <!-- Uses #FF5A5F -->
<span class="text-accent">trending_up</span>  <!-- Uses #FFD166 -->
<div class="bg-gray-900">  <!-- Uses #111827 -->
```

### How to Change the Primary Color

**Step 1:** Find the color definition in the `<style>` section (line 41):

```css
.gradient-primary {
    background: linear-gradient(135deg, #FF5A5F 0%, #FFD166 100%);
}

.text-primary {
    color: #FF5A5F;
}
```

**Step 2:** Replace `#FF5A5F` with your new color:

```css
.gradient-primary {
    background: linear-gradient(135deg, #1E40AF 0%, #FFD166 100%);
}

.text-primary {
    color: #1E40AF;
}
```

**Step 3:** Find all uses of `.btn-gradient` and update the gradient:

```css
.btn-gradient {
    background: linear-gradient(135deg, #1E40AF 0%, #FFD166 100%);
}
```

### How to Change the Accent Color

**Step 1:** Find the accent color definition (line 48):

```css
.text-accent {
    color: #FFD166;
}
```

**Step 2:** Replace `#FFD166` with your new color:

```css
.text-accent {
    color: #FBBF24;
}
```

**Step 3:** Update the gradient that uses this color:

```css
.gradient-primary {
    background: linear-gradient(135deg, #FF5A5F 0%, #FBBF24 100%);
}

.btn-gradient {
    background: linear-gradient(135deg, #FF5A5F 0%, #FBBF24 100%);
}
```

### How to Change Background Colors

The page uses Tailwind's built-in gray colors. To change all backgrounds:

**Option 1: Change individual elements**

Find each `bg-gray-900` or `bg-gray-800` and replace:

```html
<!-- Before -->
<body class="bg-gray-900 text-white">

<!-- After - slightly lighter -->
<body class="bg-gray-800 text-white">
```

**Option 2: Create a custom background color**

Add a new class to your `<style>` section:

```css
.bg-custom {
    background-color: #0F172A;
}
```

Then use it in HTML:

```html
<body class="bg-custom text-white">
```

### Popular Color Combinations

Here are some professional color schemes you could use:

#### Blue & Gold
```css
.text-primary {
    color: #1E40AF;  /* Blue */
}

.text-accent {
    color: #F59E0B;  /* Gold */
}

.gradient-primary {
    background: linear-gradient(135deg, #1E40AF 0%, #F59E0B 100%);
}
```

#### Purple & Pink
```css
.text-primary {
    color: #7C3AED;  /* Purple */
}

.text-accent {
    color: #EC4899;  /* Pink */
}

.gradient-primary {
    background: linear-gradient(135deg, #7C3AED 0%, #EC4899 100%);
}
```

#### Green & Teal
```css
.text-primary {
    color: #059669;  /* Green */
}

.text-accent {
    color: #14B8A6;  /* Teal */
}

.gradient-primary {
    background: linear-gradient(135deg, #059669 0%, #14B8A6 100%);
}
```

### Finding Hex Color Codes

To find hex codes for colors you like:

1. Use **Google Color Picker**: Search "color picker" in Google
2. Use **Coolors.co**: Generate color palettes
3. Use **Adobe Color**: Create custom color schemes
4. Use browser DevTools: Right-click on any color element and inspect

### Testing Your Color Changes

After changing colors:

1. Save the HTML file
2. Refresh the browser (Ctrl+R or Cmd+R)
3. Check all sections: header, buttons, hover states, cards
4. Test on mobile by resizing the browser window
5. Verify text contrast (dark text on light backgrounds, light text on dark backgrounds)

---

## Responsive Design Tips

The landing page is designed to work on all device sizes. This section explains how to maintain responsiveness when making changes.

### What is Responsive Design?

Responsive design means the website adapts to different screen sizes:
- **Mobile:** 320px - 640px
- **Tablet:** 641px - 1024px
- **Desktop:** 1025px and above

### Tailwind Breakpoints

Tailwind uses prefixes to target different screen sizes:

| Prefix | Screen Width | Usage |
|--------|--------------|-------|
| (none) | All sizes | `text-lg` (applies to all) |
| `sm:` | 640px+ | `sm:flex-row` (small screens and up) |
| `md:` | 768px+ | `md:text-2xl` (medium screens and up) |
| `lg:` | 1024px+ | `lg:text-4xl` (large screens and up) |
| `xl:` | 1280px+ | `xl:text-5xl` (extra large) |

### Common Responsive Patterns in This Page

#### Pattern 1: Different Text Sizes

```html
<!-- Mobile: text-4xl (36px) -->
<!-- Tablet: text-5xl (48px) -->
<!-- Desktop: text-6xl (60px) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold">
    Main Headline
</h1>
```

**How to maintain this pattern:**
- Always include the base class (for mobile)
- Always add `md:` version (for tablets)
- Always add `lg:` version (for desktops)

#### Pattern 2: Hidden on Mobile

```html
<!-- Hidden on mobile, shown on medium screens and up -->
<div class="hidden md:block">
    Desktop content
</div>
```

**Common uses:**
- Desktop navigation (hidden on mobile)
- Large images (shown only on desktop)
- Extra information (shown on larger screens)

#### Pattern 3: Grid Layouts

```html
<!-- Mobile: 1 column -->
<!-- Tablet: 2 columns -->
<!-- Desktop: 3 columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Cards go here -->
</div>
```

**How to maintain this pattern:**
- Base: `grid-cols-1` (one column on mobile)
- Medium: `md:grid-cols-2` (two columns on tablets)
- Large: `lg:grid-cols-3` (three columns on desktop)

#### Pattern 4: Flex Direction

```html
<!-- Mobile: vertical (flex-col) -->
<!-- Desktop: horizontal (flex-row) -->
<div class="flex flex-col md:flex-row gap-6">
    <div>Item 1</div>
    <div>Item 2</div>
</div>
```

### When Modifying Content, Keep Responsiveness in Mind

#### ❌ Don't Do This (Not Responsive)

```html
<!-- This text is too big on mobile! -->
<h1 class="text-6xl font-semibold">
    Main Headline
</h1>
```

#### ✅ Do This (Responsive)

```html
<!-- Scales properly on all devices -->
<h1 class="text-3xl md:text-4xl lg:text-5xl font-semibold">
    Main Headline
</h1>
```

#### ❌ Don't Do This (Mobile Menu Broken)

```html
<!-- Always visible, breaks mobile layout -->
<nav class="flex items-center gap-12">
    <!-- Navigation items -->
</nav>
```

#### ✅ Do This (Mobile Menu Works)

```html
<!-- Hidden on mobile, shown on medium screens -->
<nav class="hidden md:flex items-center gap-12">
    <!-- Navigation items -->
</nav>
```

### How to Test Responsiveness

#### Method 1: Browser Resize

1. Open your HTML file in a browser
2. Start with a narrow window (mobile size)
3. Slowly drag the right edge to make it wider
4. Watch how the layout adapts
5. Check all text sizes, spacing, and layouts

#### Method 2: Browser DevTools

1. Open your HTML file in a browser
2. Press F12 (or right-click → Inspect)
3. Click the mobile icon (top-left of DevTools)
4. Select different devices from the dropdown
5. Test on iPhone, iPad, Android, etc.

#### Method 3: Actual Devices

1. Upload your file to a web server
2. Open the URL on your phone, tablet, and computer
3. Test all interactions on real devices
4. Check that buttons are clickable on mobile

### Common Responsive Issues & Fixes

#### Issue: Text Too Small on Mobile

**Problem:**
```html
<p class="text-sm">Small text</p>
```

**Solution:**
```html
<p class="text-base md:text-sm">Readable on mobile, small on desktop</p>
```

#### Issue: Images Too Large on Mobile

**Problem:**
```html
<img src="image.jpg" class="w-full max-w-2xl">
```

**Solution:**
```html
<img src="image.jpg" class="w-full max-w-md md:max-w-2xl">
```

#### Issue: Too Much Padding on Mobile

**Problem:**
```html
<div class="p-16">Content</div>
```

**Solution:**
```html
<div class="p-6 md:p-12 lg:p-16">Content</div>
```

#### Issue: Menu Overlaps Content on Mobile

**Problem:**
```html
<nav class="flex">  <!-- Always visible -->
```

**Solution:**
```html
<nav class="hidden md:flex">  <!-- Hidden on mobile -->
```

### Best Practices for Responsive Design

1. **Mobile First:** Always start with mobile styles, then add larger screen styles
2. **Test Often:** Test on multiple devices and screen sizes
3. **Keep Patterns:** Use consistent responsive patterns throughout
4. **Maintain Hierarchy:** Ensure important content is visible on all sizes
5. **Touch Friendly:** Make buttons and links large enough to tap on mobile

---

## Troubleshooting

This section covers common problems and how to fix them.

### Problem: Changes Don't Show Up

**Possible causes:**
1. File not saved
2. Browser showing cached version
3. Wrong file being edited

**Solutions:**

1. **Save the file:**
   - Ctrl+S (Windows) or Cmd+S (Mac)
   - Look for the save indicator in your editor

2. **Clear browser cache:**
   - Ctrl+Shift+Delete (Windows) or Cmd+Shift+Delete (Mac)
   - Select "All time" and check "Cached images and files"
   - Click "Clear data"

3. **Hard refresh:**
   - Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)
   - This reloads the page without using cache

4. **Check file path:**
   - Make sure you're editing the correct file
   - Check that the file is in the right folder

### Problem: Links Don't Work

**Possible causes:**
1. Typo in URL
2. Missing `http://` or `https://`
3. File doesn't exist
4. Wrong file name or path

**Solutions:**

1. **Check for typos:**
```html
<!-- Wrong -->
<a href="https://exmaple.com">Link</a>

<!-- Right -->
<a href="https://example.com">Link</a>
```

2. **Add protocol for external links:**
```html
<!-- Wrong -->
<a href="example.com">Link</a>

<!-- Right -->
<a href="https://example.com">Link</a>
```

3. **Verify file exists:**
- Make sure `privacy.html` is in the same folder as `index.html`
- Check exact spelling and capitalization

4. **Test the link:**
- Right-click the link → "Open Link in New Tab"
- Check if it goes to the correct place

### Problem: Website Looks Broken on Mobile

**Possible causes:**
1. Missing responsive classes
2. Fixed width elements
3. Overflow issues

**Solutions:**

1. **Check responsive classes:**
```html
<!-- Bad - not responsive -->
<h1 class="text-6xl">Title</h1>

<!-- Good - responsive -->
<h1 class="text-3xl md:text-5xl lg:text-6xl">Title</h1>
```

2. **Avoid fixed widths:**
```html
<!-- Bad - fixed width -->
<div class="w-1000">Content</div>

<!-- Good - responsive -->
<div class="w-full max-w-4xl">Content</div>
```

3. **Test on mobile:**
- Use browser DevTools (F12)
- Select mobile device from dropdown
- Resize and check layout

### Problem: Text Appears Blurry or Hard to Read

**Possible causes:**
1. Poor color contrast
2. Font size too small
3. Line height too tight

**Solutions:**

1. **Improve color contrast:**
```html
<!-- Bad contrast -->
<p class="text-gray-600 bg-gray-700">Hard to read</p>

<!-- Good contrast -->
<p class="text-white bg-gray-900">Easy to read</p>
```

2. **Increase font size:**
```html
<!-- Too small -->
<p class="text-xs">Tiny text</p>

<!-- Better -->
<p class="text-base md:text-lg">Readable text</p>
```

3. **Add line height:**
```html
<!-- Cramped -->
<p class="text-base">Text</p>

<!-- Better spacing -->
<p class="text-base leading-relaxed">Text</p>
```

### Problem: Buttons Not Clickable

**Possible causes:**
1. Button is covered by another element
2. Button has `pointer-events: none`
3. JavaScript preventing clicks

**Solutions:**

1. **Check z-index:**
```html
<!-- Ensure button is on top -->
<button class="relative z-10">Click me</button>
```

2. **Remove pointer-events:**
```css
/* Don't use this on buttons */
pointer-events: none;
```

3. **Verify button code:**
```html
<!-- Correct button -->
<button class="btn-gradient px-8 py-4 rounded">
    Click me
</button>

<!-- Not a button -->
<div class="btn-gradient px-8 py-4 rounded">
    Not clickable
</div>
```

### Problem: Images Not Loading

**Possible causes:**
1. Wrong file path
2. File doesn't exist
3. File name has spaces or special characters

**Solutions:**

1. **Check file path:**
```html
<!-- Wrong path -->
<img src="images/photo.jpg">

<!-- Right path -->
<img src="photo.jpg">
```

2. **Use correct file names:**
```html
<!-- Bad - spaces in name -->
<img src="my photo.jpg">

<!-- Good - no spaces -->
<img src="my-photo.jpg">
```

3. **Verify file exists:**
- Check that the image file is in the correct folder
- Check exact spelling and capitalization

### Problem: Form Not Submitting

**Possible causes:**
1. Missing access key
2. JavaScript error
3. Form fields not named correctly

**Solutions:**

1. **Check access key:**
```html
<!-- Correct -->
<input type="hidden" name="access_key" value="3bb39263-2490-491b-89f8-213fa513edae">

<!-- Wrong - empty or invalid -->
<input type="hidden" name="access_key" value="">
```

2. **Verify form setup:**
```html
<!-- Correct form structure -->
<form action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="YOUR_KEY">
    <input type="text" name="name" required>
    <textarea name="message" required></textarea>
    <button type="submit">Send</button>
</form>
```

3. **Check browser console:**
- Press F12 to open DevTools
- Click "Console" tab
- Look for error messages
- Fix any JavaScript errors

### Problem: Animations Not Working

**Possible causes:**
1. CSS not loading
2. JavaScript disabled
2. Browser doesn't support animation

**Solutions:**

1. **Check CSS is loaded:**
```html
<!-- Verify this line is in <head> -->
<script src="https://cdn.tailwindcss.com"></script>
```

2. **Enable JavaScript:**
- Check browser settings
- Make sure JavaScript is enabled

3. **Check browser compatibility:**
- Test in different browsers
- Some older browsers don't support all animations

### Problem: Hover Effects Not Working

**Possible causes:**
1. CSS not applied
2. Element doesn't have hover class
3. Mobile devices don't support hover

**Solutions:**

1. **Check hover class exists:**
```html
<!-- With hover effect -->
<a href="#" class="text-gray-300 hover:text-primary">Link</a>

<!-- Without hover effect -->
<a href="#">Link</a>
```

2. **Test on desktop:**
- Hover effects work on desktop/mouse
- Mobile/touch devices don't support hover
- This is normal behavior

3. **Verify CSS is loaded:**
- Open DevTools (F12)
- Check "Styles" tab
- Look for hover rules

---

## Best Practices

This section covers recommended practices for maintaining and updating the landing page.

### Content Management

#### 1. Keep a Change Log

Track all changes you make:

```
Date: January 15, 2025
- Updated company tagline in hero section
- Changed primary button text from "Start Your Case" to "Book Consultation"
- Added new testimonial from Jennifer Smith
- Updated footer contact email

Date: January 10, 2025
- Created privacy.html page
- Updated all contact page links
- Fixed broken social media links
```

#### 2. Backup Before Major Changes

Always keep a backup copy:

```
Project Folder/
├── index.html (current version)
├── index-backup-2025-01-15.html (backup)
├── privacy.html
└── terms.html
```

#### 3. Update Content Regularly

- Review testimonials quarterly
- Update case statistics annually
- Refresh team information as needed
- Keep contact information current

### Code Quality

#### 1. Maintain Consistent Formatting

Keep your code organized and readable:

```html
<!-- Good - organized -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold mb-6 text-white">
    Professional Legal & Investigative Services
</h1>

<!-- Bad - hard to read -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-semibold mb-6 text-white">Professional Legal & Investigative Services</h1>
```

#### 2. Use Comments for Important Sections

```html
<!-- Hero Section - Main Introduction -->
<section class="py-32 md:py-40">
    <!-- Main headline -->
    <h1>...</h1>
    
    <!-- Description -->
    <p>...</p>
</section>
```

#### 3. Avoid Inline Styles

```html
<!-- Bad - inline style -->
<div style="background-color: red; padding: 20px;">Content</div>

<!-- Good - use Tailwind classes -->
<div class="bg-primary p-5">Content</div>
```

### SEO Best Practices

#### 1. Update Meta Descriptions

```html
<!-- In <head> section -->
<meta name="description" content="Professional Legal & Investigative Services - Forensic probes, court affidavits, and legal counsel.">
```

Keep descriptions:
- Between 150-160 characters
- Include main keywords
- Compelling and accurate

#### 2. Use Proper Heading Structure

```html
<!-- Correct - proper hierarchy -->
<h1>Main Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>

<!-- Incorrect - skipping levels -->
<h1>Main Title</h1>
<h3>Skipped h2!</h3>
```

#### 3. Optimize Images

- Use descriptive file names: `legal-consultation.jpg` (good) vs `img123.jpg` (bad)
- Add alt text: `<img alt="Legal consultation with attorney">`
- Compress images to reduce file size

### Performance

#### 1. Minimize HTTP Requests

The page uses:
- One CSS framework (Tailwind)
- One icon library (Font Awesome)
- One font family (Poppins)

Keep these minimal to maintain fast loading.

#### 2. Optimize Images

```html
<!-- Large image - slow -->
<img src="huge-image-5mb.jpg">

<!-- Optimized - fast -->
<img src="optimized-image-200kb.jpg">
```

Use tools like:
- TinyPNG.com
- Compressor.io
- ImageOptim

#### 3. Monitor Page Speed

Test your page with:
- Google PageSpeed Insights
- GTmetrix
- WebPageTest

### Security

#### 1. Always Use HTTPS

```html
<!-- Secure -->
<a href="https://yoursite.com">Link</a>

<!-- Insecure -->
<a href="http://yoursite.com">Link</a>
```

#### 2. Validate Form Input

```html
<!-- Good - required fields -->
<input type="email" name="email" required>
<textarea name="message" required></textarea>

<!-- Bad - no validation -->
<input type="text" name="anything">
```

#### 3. Protect Sensitive Information

```html
<!-- Good - doesn't expose sensitive data -->
<input type="hidden" name="access_key" value="...">

<!-- Bad - exposes sensitive data -->
<input type="hidden" name="password" value="admin123">
```

### Accessibility

#### 1. Use Semantic HTML

```html
<!-- Good - semantic -->
<header>Navigation</header>
<main>Content</main>
<footer>Footer</footer>

<!-- Bad - not semantic -->
<div id="header">Navigation</div>
<div id="main">Content</div>
<div id="footer">Footer</div>
```

#### 2. Add Alt Text to Images

```html
<!-- Good - descriptive alt text -->
<img src="attorney.jpg" alt="Senior attorney reviewing legal documents">

<!-- Bad - no alt text -->
<img src="attorney.jpg">
```

#### 3. Use Sufficient Color Contrast

```html
<!-- Good contrast -->
<p class="text-white bg-gray-900">Easy to read</p>

<!-- Poor contrast -->
<p class="text-gray-500 bg-gray-600">Hard to read</p>
```

### Testing Checklist

Before publishing changes, verify:

- [ ] All links work correctly
- [ ] Page displays properly on mobile
- [ ] Page displays properly on tablet
- [ ] Page displays properly on desktop
- [ ] All images load
- [ ] Forms submit without errors
- [ ] No JavaScript errors in console
- [ ] Spelling and grammar are correct
- [ ] Contact information is current
- [ ] Page loads in reasonable time

### Version Control (Advanced)

If you're comfortable with Git, use version control:

```bash
# Initialize repository
git init

# Add files
git add .

# Commit changes
git commit -m "Update testimonials and fix contact links"

# View history
git log
```

This allows you to:
- Track all changes
- Revert to previous versions
- Collaborate with others
- Maintain backup history

---

## Quick Reference Guide

### Most Common Tasks

#### Update Main Headline
Find line 157, update text between `<h1>` tags

#### Change Contact Page URL
Find all instances of `https://somda.co.za/contact/` and replace with your URL

#### Update Company Name
Find `SOMDA` in header (line 108) and replace

#### Add New Testimonial
Copy testimonial card (lines 425-440) and paste below

#### Change Primary Color
Update `#FF5A5F` in `<style>` section (lines 41-48)

#### Fix Mobile Menu
Check that `mobile-menu-button` and `mobile-menu` classes are present

#### Update Footer Links
Scroll to footer section (lines 700-750) and update href attributes

#### Add Social Media Links
Replace `href="#"` with actual social media URLs (lines 701-709)

---

## File Checklist

Before considering your site complete:

- [ ] `index.html` - Main landing page
- [ ] `privacy.html` - Privacy policy page
- [ ] `terms.html` - Terms of service page
- [ ] `blog.html` - Blog page (if using)
- [ ] All images in correct folder
- [ ] All links tested and working
- [ ] All contact information updated
- [ ] Mobile responsiveness tested
- [ ] SEO meta tags updated
- [ ] Backup copy saved

---

## Getting Help

### Common Resources

- **HTML Reference:** MDN Web Docs (developer.mozilla.org)
- **CSS/Tailwind:** Tailwind CSS Documentation (tailwindcss.com)
- **Color Tools:** Coolors.co, Adobe Color
- **Font Awesome Icons:** fontawesome.com/icons
- **Web Performance:** Google PageSpeed Insights

### When Something Breaks

1. **Check the error message** - Browser console (F12 → Console)
2. **Look for typos** - Common cause of issues
3. **Check file paths** - Make sure files are in the right place
4. **Test in different browser** - Issue might be browser-specific
5. **Clear cache** - Old version might be showing
6. **Restore from backup** - Last resort option

---

## Conclusion

This landing page is designed to be:
- **Easy to maintain** - Clear structure and organization
- **Customizable** - Tailwind CSS for flexible styling
- **Responsive** - Works on all devices
- **Professional** - Modern design suitable for legal services

By following this guide, you can confidently update and maintain your landing page. Remember to:

1. Always backup before major changes
2. Test thoroughly on all devices
3. Keep content current and relevant
4. Maintain consistent branding
5. Monitor performance and user feedback

Good luck with your legal services website!