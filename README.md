# STEDTOP Pharmaceuticals — Official Website

> **"Quality You Can Trust"**  
> A professional, multi-page static website for STEDTOP Pharmaceuticals Pvt. Ltd., built with pure HTML, CSS, and JavaScript. No frameworks. No dependencies.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Live Preview](#live-preview)
- [Project Structure](#project-structure)
- [Pages](#pages)
- [Features](#features)
- [Design System](#design-system)
- [How to Run](#how-to-run)
- [File Replacement Guide](#file-replacement-guide)
- [Product Filter System](#product-filter-system)
- [Contact & Email](#contact--email)
- [Browser Support](#browser-support)
- [Credits](#credits)

---

## Project Overview

This is the official static website for **STEDTOP Pharmaceuticals Pvt. Ltd.**, a science-driven pharmaceutical company based in Bhubaneswar, India. The website showcases the company's therapeutic areas, featured products, quality promise, and contact information.

| Detail | Info |
|---|---|
| **Company** | STEDTOP Pharmaceuticals Pvt. Ltd. |
| **Type** | Static Website (HTML / CSS / JS) |
| **Pages** | 4 (Home, About, Products, Contact) |
| **Framework** | None — Pure Vanilla HTML/CSS/JS |
| **Fonts** | Playfair Display + Inter (Google Fonts) |
| **Contact Email** | stp.bhubaneswar@gmail.com |

---

## Live Preview

Open `index.html` directly in any modern browser — no server required.

```
Double-click index.html  →  Opens in browser
```

Or use a local server for best results (see [How to Run](#how-to-run)).

---

## Project Structure

```
STEDTOP/
│
├── index.html               ← Homepage
├── about.html               ← About Us page
├── products.html            ← Products listing with filter
├── contacts.html            ← Contact form & info
├── README.md                ← This file
│
└── assets/
    ├── css/
    │   └── style.css        ← All styles (design tokens, layout, components)
    │
    ├── js/
    │   └── script.js        ← Hamburger menu, scroll reveal, product filter, contact form
    │
    └── images/
        ├── logo.png                  ← STEDTOP logo (navbar + footer)
        ├── icon-pain.jfif            ← Therapeutic area icon — Pain
        ├── icon-neuro.jpg            ← Therapeutic area icon — Neuro
        ├── icon-gastro.jfif          ← Therapeutic area icon — Gastro
        ├── icon-wellness.jfif        ← Therapeutic area icon — Wellness
        ├── product-zetpar-ac.png     ← ZETPAR AC product image
        ├── product-galatop-pn-sr.png ← GALATOP-PN SR product image
        ├── product-oopan-dsr.png     ← OOPAN DSR product image
        └── product-galatop-k2-7.png  ← GALATOP K2-7 product image
```

---

## Pages

### 1. `index.html` — Homepage
- Animated hero section with gold/navy gradient, floating orbs, and grid texture
- **"Advanced *Healthcare* Solutions"** headline with italic gold highlight
- Trust stats bar: 4+ Therapeutic Areas · GMP Certified · 100% Quality Assured
- **Who We Are** — company intro with 3 numbered pillar cards
- **Therapeutic Expertise** — 4 clickable tiles (each links directly to filtered products page)
- **Featured Products** — 2 product cards (ZETPAR AC + GALATOP-PN SR) with deep-linked "View Details" buttons
- **Quality Promise** banner — dark navy with gold grid texture and checklist
- Footer with quick links, therapeutic area deep-links, and contact email

### 2. `about.html` — About Us
- Page hero with animated background
- Mission / Vision / Values — 3 cards
- Our Story section with stat grid (4+ Areas, 100% Quality, GMP, ∞ Commitment)
- Therapeutic Areas overview cards
- Quality Promise CTA banner

### 3. `products.html` — Products
- Page hero
- **Filter bar** — All Products / Pain Management / Neuro Care / Gastro Care / Wellness
- **4 product cards** in horizontal layout:
  - ZETPAR AC (Pain)
  - GALATOP-PN SR (Neuro)
  - OOPAN DSR (Gastro)
  - GALATOP K2-7 (Wellness)
- CTA section linking to contact page

### 4. `contacts.html` — Contact
- Page hero
- Contact info: address, email, business hours
- Enquiry type chips: Product Info / Sample Requests / Distribution / Medical Queries / Partnership
- Contact form: First Name, Last Name, Email, Subject, Message
- Success message on form submission

---

## Features

### Navigation
- Sticky header with blur backdrop effect
- Logo left-aligned, nav links right-aligned
- Active page highlighting with gold underline
- "Get In Touch" CTA button in navbar
- Fully responsive hamburger menu (slide-in panel on mobile)

### Hero Section
- Full-viewport height with animated floating orbs
- Subtle CSS grid texture overlay
- Animated scroll indicator
- Smooth wave SVG transition to next section

### Scroll Reveal Animations
- All sections animate in as user scrolls down
- Uses `IntersectionObserver` API — progressive enhancement
- Content is visible by default (no flash of hidden content)

### Product Filter (Deep-Link Routing)
- Click any filter button to show only that category
- URL hash-based routing: `products.html#gastro` shows only Gastro products
- Works from any link across the site (footer, homepage tiles, featured product buttons)

| Link | Result |
|---|---|
| `products.html` | All products shown |
| `products.html#pain` | Only ZETPAR AC shown |
| `products.html#neuro` | Only GALATOP-PN SR shown |
| `products.html#gastro` | Only OOPAN DSR shown |
| `products.html#wellness` | Only GALATOP K2-7 shown |

### Contact Form
- Client-side validation (HTML5 required fields)
- Simulated async submission with loading state
- Success message displayed after submission
- Form auto-resets after send

### Hover Effects
- Therapy tiles: lift + gold underline bar reveal
- Product cards: lift + shadow + image scale
- Pillar cards: slide right + background shift
- Footer links: slide right on hover
- All buttons: lift + glow on hover

---

## Design System

### Color Palette

| Token | Value | Usage |
|---|---|---|
| `--navy` | `#07111e` | Primary background, header, footer |
| `--navy-2` | `#0c1a2e` | Secondary dark backgrounds |
| `--navy-3` | `#132340` | Gradient stops |
| `--gold` | `#c8a84b` | Primary accent, headings highlight |
| `--gold-lt` | `#e6c96a` | Lighter gold, gradients |
| `--cream` | `#f9f5ee` | Light section backgrounds |
| `--cream-2` | `#f2ebdc` | Card backgrounds, image areas |
| `--white` | `#ffffff` | Base white |
| `--text` | `#1a2535` | Primary body text |
| `--muted` | `#677489` | Secondary text, descriptions |

### Typography

| Font | Role | Weights |
|---|---|---|
| **Playfair Display** | Headings, display text, hero | 400, 500, 600, 700 (incl. italic) |
| **Inter** | Body text, labels, buttons, UI | 300, 400, 500, 600 |

### Breakpoints

| Breakpoint | Width | Changes |
|---|---|---|
| Desktop | > 1100px | Full multi-column layouts |
| Tablet | ≤ 1100px | 2-column footer, 2-column therapy grid |
| Mobile | ≤ 768px | Hamburger menu, stacked layouts |
| Small Mobile | ≤ 560px | 2-column therapy grid, stacked buttons |

---

## How to Run

### Option 1 — Direct (Quickest)
```
Double-click index.html in your file explorer
```

### Option 2 — VS Code Live Server (Recommended)
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html` → **Open with Live Server**
3. Opens at `http://127.0.0.1:5500`

### Option 3 — Node.js `serve`
```bash
npx serve .
# Opens at http://localhost:3000
```

### Option 4 — Python HTTP Server
```bash
# Python 3
python -m http.server 8080
# Opens at http://localhost:8080
```

---

## File Replacement Guide

When you receive updated files, replace them in your project folder exactly as shown:

| File Received | Replace At |
|---|---|
| `index.html` | `/index.html` (root) |
| `about.html` | `/about.html` (root) |
| `products.html` | `/products.html` (root) |
| `contacts.html` | `/contacts.html` (root) |
| `style.css` | `/assets/css/style.css` |
| `script.js` | `/assets/js/script.js` |

> **Important:** Always keep the `assets/images/` folder intact. Never rename or move image files.

---

## Product Filter System

The filter system uses **URL hash routing** — no backend required.

### How It Works

1. Every filter link appends a `#hash` to `products.html`
2. When `products.html` loads, `script.js` reads `window.location.hash`
3. It calls `applyFilter(hash)` which shows only cards with matching `data-category`
4. The correct filter button is highlighted automatically

### Adding a New Product

To add a new product, add a new `.pcard` block inside `#products-grid` in `products.html`:

```html
<div class="pcard" data-category="pain">
  <div class="pcard-img">
    <img src="assets/images/your-product.png" alt="Product Name">
    <span class="pcard-badge" style="background:#c0392b">Pain</span>
  </div>
  <div class="pcard-body">
    <div class="pcard-head">
      <h3>PRODUCT NAME</h3>
      <span class="pcard-cat">Pain Management</span>
    </div>
    <p class="pcard-tagline">Short tagline here</p>
    <p class="pcard-desc">Full product description here.</p>
    <div class="pcard-features">
      <span>Feature 1</span>
      <span>Feature 2</span>
      <span>Feature 3</span>
    </div>
  </div>
</div>
```

**Valid `data-category` values:** `pain` · `neuro` · `gastro` · `wellness`

---

## Contact & Email

The contact email is set to:

```
stp.bhubaneswar@gmail.com
```

It appears in the following locations across all pages:
- Footer → Contact column (all 4 pages)
- `contacts.html` → Contact info section

To update the email, search for `stp.bhubaneswar@gmail.com` across all HTML files and replace.

---

## Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Internet Explorer | ❌ Not supported |

---

## Credits

| Item | Detail |
|---|---|
| **Company** | STEDTOP Pharmaceuticals Pvt. Ltd. |
| **Location** | Bhubaneswar, Odisha, India |
| **Fonts** | [Google Fonts](https://fonts.google.com) — Playfair Display, Inter |
| **Built With** | HTML5, CSS3, Vanilla JavaScript |

| **No frameworks used** | Pure hand-coded static site |

---

*© 2025 STEDTOP Pharmaceuticals Pvt. Ltd. All rights

reserved.*

<img width="1901" height="859" alt="image" src="https://github.com/user-attachments/assets/3bf2e099-c2dd-493b-8c27-e38c68290797" />

<img width="1900" height="862" alt="image" src="https://github.com/user-attachments/assets/4f249e62-0eeb-4f9e-a0ba-6426ce630154" />

<img width="1901" height="866" alt="image" src="https://github.com/user-attachments/assets/8992d596-4e2d-4374-8d88-64e527d75212" />

<img width="1901" height="861" alt="image" src="https://github.com/user-attachments/assets/0878cdf4-28f9-4b89-9553-235237d6402d" />





