# EcoCharge - Responsive Mini-Site

> **HTML + CSS Assignment**: A responsive single-page website showcasing sustainable solar charging solutions with CSS-only interactive components.

---

## 📊 Market Research Report

A companion **market research report** has been added to this repository, identifying the highest-demand countries, cities, and business niches for digital services (website development, online booking, automation, and AI tools).

**File:** [`market-research.html`](market-research.html) &nbsp;|&nbsp; **Styles:** [`market-research.css`](market-research.css)

### Highlights
| Output | Details |
|--------|---------|
| 🌍 **Top 5 Countries** | USA, UK, UAE, Australia, Canada |
| 🏙️ **Top 10 Cities** | NYC, Dubai, London, LA, Sydney, Toronto, Chicago, Manchester, Melbourne, Houston |
| 💼 **Best Niches** | Barber Shops, Dental Clinics, Beauty Salons, Restaurants, Retail, Gyms |
| 📈 **Opportunity Levels** | High / Medium scored per region-niche pair |
| 🔬 **Methodology** | Google Maps audits, social media analysis, 200K+ customer reviews, market trend data |

---

## 🌱 Project Overview

**EcoCharge** is a fictional sustainable energy company offering revolutionary solar-powered charging solutions. This project demonstrates modern web development techniques using only HTML5 and CSS3, with no JavaScript or frameworks.

**Live Demo**: https://YOUR-GITHUB-USERNAME.github.io/ecocharge/

**GitHub Repository**: https://github.com/YOUR-GITHUB-USERNAME/ecocharge

---

## 📁 Project Structure
```
ecocharge/
│
├── index.html                      # Main HTML file
├── styles.css                      # External CSS stylesheet
├── README.md                       # Project documentation
│
└── assets/
    ├── screenshots/
    │   ├── desktop-view.png       # Desktop layout screenshot
    │   ├── tablet-view.png        # Tablet layout screenshot
    │   ├── mobile-view.png        # Mobile layout screenshot


## 🎨 Design Rationale

### Color Scheme
The color palette reflects the eco-friendly nature of the product:

| Color | Hex Code | Purpose |
|-------|----------|---------|
| Primary Green | `#2ecc71` | Sustainability, growth, eco-friendliness |
| Secondary Green | `#27ae60` | Depth and visual hierarchy |
| Accent Orange | `#f39c12` | Energy, sun, warmth |
| Dark Navy | `#1a1a2e` | Professional contrast |
| Light Gray | `#f8f9fa` | Clean background |

### Typography
- **Font Family**: Segoe UI (system font for optimal performance)
- **Hierarchy**: 
  - Hero H1: 4rem (desktop) → 2rem (mobile)
  - Section H2: 2.5rem
  - Card H3: 1.5rem
  - Body Text: 1rem
  - Line Height: 1.6 (optimal readability)

### Layout Philosophy
- **Mobile-First Approach**: Base styles optimized for mobile, enhanced for larger screens
- **Grid System**: CSS Grid for page structure (5 main areas)
- **Flexbox System**: Component-level layouts (cards, navigation, forms)
- **Whitespace**: Generous padding and margins for breathing room

---

## ✅ Assignment Requirements Compliance

### Part A - Structure & Layout

#### ✅ Semantic HTML5 Elements
- `<header>` - Site header with logo and navigation
- `<nav>` - Main navigation menu with role attribute
- `<main>` - Primary content wrapper
- `<section>` - Content sections (hero, features, form)
- `<article>` - Individual feature cards
- `<form>` - Contact/signup form with proper structure
- `<fieldset>` & `<legend>` - Grouped form inputs
- `<footer>` - Site footer with copyright and social links

#### ✅ Three Responsive Breakpoints

1. **Mobile (< 768px)**:
   - Single column layout
   - Stacked navigation
   - Reduced font sizes
   - Full-width cards
   - Vertical form layout

2. **Tablet (768px - 1023px)**:
   - Two-column form inputs
   - Larger typography
   - Flexible card grid
   - Enhanced spacing

3. **Desktop (≥ 1024px)**:
   - Horizontal navigation
   - Maximum typography scale
   - Three-column card layout
   - Optimal content width (1200px)

#### ✅ CSS Grid Implementation
```css
.site-container {
    display: grid;
    grid-template-areas:
        "header"
        "hero"
        "features"
        "form"
        "footer";
}
```

#### ✅ Flexbox Implementation
- Navigation menu (horizontal/vertical)
- Feature card grid (wrapping)
- Form input groups
- Footer social links

---

### Part B - Smart Form Components

#### ✅ All Required Elements

1. **Text Input (Name)**:
   - Type: `text`
   - Validation: `required`, `minlength="2"`
   - Label: Properly associated with `for` attribute

2. **Email Input**:
   - Type: `email`
   - Validation: `required`, HTML5 email pattern

3. **Four Checkboxes (Interests)**:
   - Portable Chargers
   - Home Solar Panels
   - Vehicle Charging
   - Commercial Solutions

4. **Three Radio Buttons (Plans)**:
   - Starter Plan ($99)
   - Pro Plan ($199)
   - Enterprise Plan ($499)

5. **Select Dropdown**:
   - Label: "How did you hear about us?"
   - 6 options + default placeholder

6. **Textarea**:
   - Label: "Additional Comments"
   - Rows: 5, resizable vertically

7. **Submit Button**:
   - Text: "Reserve Your Spot"
   - Full-width with gradient background

---

## 🎯 Three CSS-Only Interactive Components

### Component 1: Animated CTA Button ✨

**Location**: Hero section

**How It Works**:
- Uses CSS `transform` to elevate button 3px on Y-axis
- Enhances `box-shadow` for depth perception
- Smooth `transition: all 0.3s ease`
- Accessible via keyboard with focus outline
```css
.cta-button:hover,
.cta-button:focus {
    transform: translateY(-3px);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}
```

---

### Component 2: 3D Flip Cards 🃏

**Location**: Features section (3 cards)

**How It Works**:
- Uses `perspective: 1000px` for 3D space
- `transform-style: preserve-3d` maintains positioning
- `backface-visibility: hidden` prevents transparency
- Rotates 180° on Y-axis over 0.8s
- Works with both `:hover` and `:focus-within`
```css
.feature-card:hover .card-inner,
.feature-card:focus-within .card-inner {
    transform: rotateY(180deg);
}
```

---

### Component 3: Custom Form Controls 🎨

**Location**: Form section (checkboxes and radio buttons)

**How It Works**:
1. Hide native inputs with `opacity: 0`
2. Create custom `.checkmark` and `.radiomark` elements
3. Use `:checked` pseudo-class to detect state
4. Show `::after` pseudo-element for check/dot icon
5. Smooth transitions on all state changes
```css
input[type="checkbox"]:checked + .checkmark {
    background-color: var(--primary-color);
}
```

---

## 📱 Responsive Design Details

### Mobile (< 768px)
- Navigation stacks vertically
- Hero text: 2rem
- Feature cards: Full-width
- Form: Single column
- Reduced padding

### Tablet (768px - 1023px)
- Hero text: 3.5rem
- Form inputs: 2 columns
- Checkboxes/radios: Horizontal layout
- Enhanced spacing

### Desktop (≥ 1024px)
- Hero text: 4rem (maximum)
- Navigation: Full horizontal (3rem gap)
- Feature cards: Side-by-side
- Optimal content width (1200px)

---

## 🎨 Custom SVG Logo

**Implementation**: Inline SVG in header
```html

    
    
    

```

**Design Elements**:
- Outer Circle (Green): Sustainability
- Diamond Path (Orange): Solar energy
- Center Circle (Navy): Brand core
- Fully scalable vector graphic

---

## ♿ Accessibility Features

### Form Accessibility
- ✅ All inputs have associated `<label>` elements
- ✅ `for` and `id` attributes properly linked
- ✅ `aria-required="true"` on mandatory fields
- ✅ Fieldsets with legends for grouped inputs

### Keyboard Navigation
- ✅ All interactive elements focusable
- ✅ Visible focus indicators (`:focus-visible`)
- ✅ Logical tab order maintained
- ✅ `tabindex="0"` on flip cards

### Visual Accessibility
- ✅ Color contrast ratios meet WCAG AA standards
- ✅ Focus outlines: 3px solid orange
- ✅ Text size minimum 16px (1rem)
- ✅ Clear visual hierarchy

---

## 📊 Code Quality & Standards

### HTML Validation ✅
- **Tool**: W3C HTML Validator (https://validator.w3.org/)
- **Result**: No errors, no warnings
- **Standards**: HTML5 compliant

### CSS Validation ✅
- **Tool**: W3C CSS Validator (https://jigsaw.w3.org/css-validator/)
- **Result**: Valid CSS3
- **Standards**: No vendor prefixes needed

### Code Organization
- **Indentation**: Consistent 4 spaces
- **Comments**: Section headers and explanations
- **Naming**: BEM-inspired, semantic class names
- **Variables**: Centralized in `:root`

---

## 🚀 Technologies Used

| Technology | Purpose | Version |
|------------|---------|---------|
| HTML5 | Semantic structure, forms | Latest |
| CSS3 | Styling, layout, animations | Latest |
| CSS Grid | Page layout structure | Modern |
| Flexbox | Component layouts | Modern |
| CSS Transforms | 3D flip cards | 3D transforms |
| CSS Variables | Theme management | Custom properties |

**No JavaScript** - Pure HTML/CSS implementation  
**No Frameworks** - Vanilla code only

---

## 📸 Screenshots

### Desktop View (1920x1080)
![Desktop Layout](assets/screenshots/desktop-view.png)

### Mobile View (375x667)
![Mobile Layout](assets/screenshots/mobile-view.png)

### Form Interaction
![Filled Form](assets/screenshots/form-demo.png)


---
