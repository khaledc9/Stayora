# Stayora — Luxury Boutique Hotel & Resort Website

A complete, production-ready, multi-page website for **Stayora**, a fictional luxury boutique hotel and resort. Built entirely with **pure HTML5 and CSS3** — no JavaScript, no third-party frameworks, no pre-made templates.

---

## Project Overview

Stayora is a calm, editorial, and immersive hotel website designed to evoke the feeling of a high-end resort retreat. The site features transparent navigation, a full-bleed hero with a floating booking search bar, CSS Grid room galleries, CSS Columns masonry photo galleries, sticky booking sidebars, alternating experience layouts, and a fully responsive design that works flawlessly from 360px mobile to 1440px+ desktop.

All interactivity — including the mobile navigation menu, filter pills, form inputs, and hover states — is achieved using semantic HTML and modern CSS only. No JavaScript is used anywhere in the project.

---

## File Structure

```
stayora/
├── index.html              # Homepage
├── README.md               # This documentation
├── pages/
│   ├── rooms.html          # Room listing with filter pills
│   ├── room-details.html   # Single room with sticky booking sidebar
│   ├── experiences.html    # Alternating image/text experience rows
│   ├── gallery.html        # CSS Columns masonry photo gallery
│   ├── about.html          # Hotel history, philosophy, team, culture
│   └── contact.html        # Reservation inquiry form + contact info
├── css/
│   ├── reset.css           # Modern CSS reset
│   ├── variables.css       # Design tokens (colors, typography, spacing)
│   ├── components.css      # Reusable UI components
│   ├── style.css           # Layout, header, footer, page-specific styles
│   └── responsive.css      # Media queries for all breakpoints
└── assets/
    └── images/             # (Images are loaded from Pexels CDN)
```

---

## Page Breakdown

### 1. `index.html` — Homepage

- **Transparent header** floating over a full-bleed hero image with gradient overlay
- **Hero section** with the headline "Slow Down. Stay Somewhere Special." and subtitle
- **Booking search bar** UI with check-in date, check-out date, guests selector, and "Check Availability" CTA — positioned to float over the hero bottom edge
- **Featured rooms grid** (CSS Grid, 3 columns): Garden Suite, Mountain Suite, Signature Villa — each with image, specs, amenities, price, and "Explore" link
- **Experiences preview** (6 cards in a 3×2 grid): Breakfast, Garden Walks, Village Tours, Hiking, Spa, Sunset Dinners — each with image overlay titles
- **Gallery teaser** — an asymmetric CSS Grid of 4 images (1 large + 3 small)
- **Guest testimonials** — 3 testimonial cards with star ratings, quotes, and author info
- **Location preview** — split layout with image and key location highlights
- **Stats bar** — 4 statistics on a dark forest-green background
- **CTA banner** — "Begin Your Stayora Story" with booking CTA
- **Footer** — 4-column layout with brand, navigation, room links, and contact details

### 2. `pages/rooms.html` — Room Listing

- Page hero with room interior background image
- Breadcrumb navigation
- **Visual filter pills** (All Rooms, Suites, Villas, Family, Signature) — CSS-styled toggle buttons
- **6 room cards** in a responsive grid: Garden Suite, Mountain Suite, Signature Villa, Forest Retreat, Heritage Suite, Pool Villa
- Each card shows: image, badge, room name, specs (guests, beds, size), amenities with checkmark icons, price per night, and "Explore Room" CTA
- CTA banner for concierge assistance

### 3. `pages/room-details.html` — Room Detail

- Breadcrumb navigation (Home › Rooms › Mountain Suite)
- **Hero gallery grid**: 1 large featured image + 2 smaller supporting images using CSS Grid (2 columns, 2 rows, featured spans both rows)
- Room title block with star rating, review count, guest capacity, bed configuration, and room size
- Detailed description paragraphs
- **Amenities list** — 10 amenities in a responsive auto-fill grid with circular icon badges (Wi-Fi, AC, Breakfast, Terrace, Fireplace, Soaking Tub, Bath Products, Minibar, Housekeeping, Yoga Mat)
- **Resort policies** — 5 policy sections with icons (Check-in/out, Cancellation, Children, Pets, Payment)
- **Sticky booking sidebar** (`position: sticky; top: 100px;`) containing: price per night, star rating, date inputs, guest selector, "Check Availability" CTA, and a complimentary perks info block
- Similar rooms recommendation grid (3 cards)

### 4. `pages/experiences.html` — Experiences

- Page hero with pool/terrace background
- **6 alternating layout rows** using `.experience-row:nth-child(even) .experience-row__image { order: 2; }`:
  1. Farm-to-Table Breakfast (image left)
  2. Garden Walks & Foraging (image right)
  3. Local Village Tours (image left)
  4. Mountain Hiking Trails (image right)
  5. Spa & Wellness Sanctuary (image left)
  6. Sunset Dinner Series (image right)
- Each row features: eyebrow label, heading, descriptive paragraph, and 3 feature highlights with circular icons
- CTA banner noting all experiences are complimentary for guests

### 5. `pages/gallery.html` — Masonry Photo Gallery

- Page hero with courtyard architecture background
- Filter pills (All, Architecture, Rooms, Nature, Experiences, Details)
- **Masonry layout** built with `column-count: 3` and `break-inside: avoid` — 18 images of varying aspect ratios
- Hover effect: image zoom + caption slide-up with gradient overlay
- Responsive column collapse: 3 columns → 2 columns (tablet) → 1 column (mobile 360px)

### 6. `pages/about.html` — About

- Page hero with resort-at-dusk background
- **About hero** — split layout with portrait image and history text (family estate → resort)
- **Philosophy section** (dark background) — 3 cards: Presence, Place, Care
- **Timeline** — 5 milestone years (2004, 2011, 2016, 2020, 2026) with descriptions
- **Team grid** — 4 team members with portrait photos, names, and roles
- **Local culture feature** — split layout with village market image and text about community partnership
- **Stats bar** — 4 statistics on dark background

### 7. `pages/contact.html` — Contact & Reservations

- Page hero with resort entrance background
- **Reservation inquiry form** with accessible `<label>` elements for every input:
  - Full Name (text, required)
  - Email Address (email, required)
  - Phone Number (tel)
  - Inquiry Type (select: Reservation, Group, Event, Corporate, General)
  - Check-In Date (date)
  - Check-Out Date (date)
  - Number of Guests (select)
  - Message (textarea)
  - "Send Inquiry" submit button
- **Contact info sidebar** with 3 cards: direct contact (phone, email, address), concierge hours, and a location map image with transfer note

---

## Design System

### Color Palette

All colors are defined as CSS custom properties in `variables.css`:

| Token             | Value     | Usage                              |
|-------------------|-----------|------------------------------------|
| `--c-cream`       | `#f5f0e7` | Warm luxury base background        |
| `--c-cream-deep`  | `#ebe3d3` | Deeper cream for alternating sections |
| `--c-forest`      | `#22352c` | Deep primary accent (dark sections, buttons) |
| `--c-forest-light`| `#2d4a3c` | Hover state for forest elements    |
| `--c-forest-dark` | `#18241d` | Footer background                  |
| `--c-sand`        | `#c8ac87` | Muted gold / warm sand (accents, badges) |
| `--c-sand-light`  | `#d8c4a8` | Light sand for dark backgrounds    |
| `--c-sand-dark`   | `#b0956f` | Hover state for sand elements      |
| `--c-charcoal`    | `#202421` | Body text                          |
| `--c-charcoal-light`| `#3a403c`| Muted text                         |
| `--c-white`       | `#ffffff` | White                              |

### Typography

- **Headings**: `Cormorant Garamond` (serif) — editorial, high-end feel, weights 300–500
- **Body**: `Inter` (sans-serif) — clean, modern, weights 300–600
- **Fluid typography** using `clamp()` for all type sizes:
  - H1: `clamp(2.5rem, 1.9rem + 3vw, 5rem)`
  - H2: `clamp(2rem, 1.68rem + 1.6vw, 3.25rem)`
  - H3: `clamp(1.6rem, 1.42rem + 0.9vw, 2.25rem)`
  - Body: `clamp(1rem, 0.96rem + 0.2vw, 1.125rem)`
  - Eyebrow: `clamp(0.7rem, 0.68rem + 0.1vw, 0.8rem)`
- **Line heights**: 1.2 for headings, 1.6 for body, 1.5 for lead text
- **Maximum 3 font weights** used per typeface (light 300, regular 400, medium 500)

### Spacing

- **8px base system** with CSS custom properties:
  - `--sp-1` (4px) through `--sp-10` (128px)
- **Fluid section padding**: `clamp(3.5rem, 2.5rem + 5vw, 7rem)` vertical, `clamp(1.5rem, 0.5rem + 4vw, 5rem)` horizontal
- Consistent application throughout all components and sections

### Layout Systems

- **CSS Grid** — room galleries, room detail layout, gallery teaser, team grid, philosophy grid, timeline, footer columns
- **Flexbox** — header navigation, booking bar, room card footers, amenity lists, filter pills, footer bottom row
- **CSS Columns** (`column-count`) — masonry photo gallery on `gallery.html`
- **CSS Order** — alternating experience rows on `experiences.html`

### Visual Details

- Rounded corners: `6px` (small), `12px` (medium), `20px` (large), `999px` (full/pill)
- Shadows: 3-level system (sm, md, lg) for depth and card hover states
- Transitions: `0.2s` (fast), `0.35s` (base), `0.6s` (slow) with custom cubic-bezier
- Hover effects: card lift + shadow, image zoom, underline animation on nav links, arrow slide on link CTAs, caption reveal on gallery items

---

## Responsive Breakpoints

The site is fully responsive across 5 defined breakpoints. Media queries are in `responsive.css` and follow a max-width cascade (large → small):

| Breakpoint         | Media Query         | Key Changes                                                    |
|--------------------|---------------------|----------------------------------------------------------------|
| **Desktop 1440px+**| `min-width: 1440px` | Wider containers, larger section padding                       |
| **Laptop 1024px**  | `max-width: 1024px` | Room grids → 2 columns, sticky sidebar → static, footer → 2 columns, gallery stays 3 columns |
| **Tablet 768px**   | `max-width: 768px`  | Mobile nav (checkbox hack), booking bar stacks vertically, grids → 1–2 columns, experience rows stack, gallery → 2 columns |
| **Tablet S 700px** | `max-width: 700px`  | Gallery teaser adjusts, stats → 2 columns, gallery → 2 columns |
| **Mobile 360px**   | `max-width: 360px`  | All grids → single column, gallery → 1 column, reduced padding, smaller buttons, timeline stacks |

### Mobile Navigation (CSS-only)

The mobile menu uses the **checkbox hack** — a hidden `<input type="checkbox">` paired with a `<label>` hamburger icon. When checked:
- The nav panel slides in from the right (`transform: translateX(0)`)
- The hamburger lines animate into an X
- A semi-transparent overlay covers the page behind the menu

No JavaScript is required for this interaction.

### No Horizontal Scroll

All layouts use `overflow-x: hidden` on the body and fluid sizing (`clamp()`, percentages, `auto-fit`/`auto-fill` grids) to prevent horizontal scrollbars at any viewport width.

---

## Accessibility

- **Semantic HTML5**: `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<main>`-equivalent sections, `<form>`, `<label>`, `<fieldset>`-equivalent groupings
- **Alt text**: Every `<img>` has a descriptive `alt` attribute describing the image content
- **Label associations**: Every form input has a `<label>` with a matching `for`/`id` pairing
- **Focus outlines**: `:focus-visible` uses a 2px sand-colored outline with 3px offset for keyboard navigation
- **ARIA labels**: Navigation regions, breadcrumbs, and form sections have `aria-label` attributes
- **Color contrast**: Body text (charcoal on cream) exceeds WCAG AA contrast ratio. White text on forest-green backgrounds also meets AA standards
- **Reduced motion**: `@media (prefers-reduced-motion: reduce)` disables all animations and transitions
- **Skip-link ready**: Semantic heading structure (single H1 per page, ordered H2/H3/H4) enables screen reader navigation
- **Keyboard accessible**: All interactive elements (links, buttons, form controls) are natively keyboard-focusable

---

## CSS Architecture

Stylesheets are loaded in this order on every page:

1. **`reset.css`** — Modern CSS reset normalizing browser defaults
2. **`variables.css`** — Design tokens (colors, fonts, spacing, breakpoints, shadows, transitions)
3. **`components.css`** — Reusable UI components (buttons, cards, badges, forms, booking bar, testimonials, amenities, policies, gallery items, breadcrumbs)
4. **`style.css`** — Page layout, header/navigation, footer, and page-specific styles (hero, rooms grid, experiences rows, gallery masonry, about sections, contact layout)
5. **`responsive.css`** — Media queries for all 5 breakpoints

### Stylesheet Path References

- **`index.html`**: `css/style.css` (relative to root)
- **`pages/*.html`**: `../css/style.css` (relative to pages/ directory)

---

## Interactivity Without JavaScript

| Feature              | CSS Technique Used                                      |
|----------------------|---------------------------------------------------------|
| Mobile menu toggle   | Checkbox hack (`:checked` pseudo-class + sibling selector) |
| Filter pills         | Styled `<button>` elements with `:hover` and `.is-active` |
| Booking bar inputs   | Native `<input>` and `<select>` with CSS styling        |
| Sticky booking sidebar | `position: sticky; top: 100px;`                      |
| Alternating layouts  | `:nth-child(even)` with `order` property                |
| Masonry gallery      | `column-count` + `break-inside: avoid`                  |
| Image hover zoom     | `transform: scale()` on `:hover`                        |
| Nav link underline   | `::after` pseudo-element with `width` transition        |
| Gallery caption reveal | `opacity` + `transform` transition on `:hover`       |
| Button hover lift    | `transform: translateY()` + box-shadow transition       |

---

## Known Limitations

1. **No live reservation engine**: The booking search bar, filter pills, and contact form are UI demonstrations only. Form submissions do not process data — there is no backend, no JavaScript, and no server-side handling. This is a pure HTML/CSS UI demo.

2. **Filter pills are visual only**: The filter pills on the rooms and gallery pages are styled buttons without JavaScript filtering logic. They demonstrate the visual design but do not filter content when clicked.

3. **No form validation beyond HTML5**: Form inputs use HTML5 `required` attributes and type validation (`email`, `tel`, `date`) but there is no custom validation or error messaging.

4. **Images are external**: All images are loaded from the Pexels CDN. An internet connection is required to view images. The `assets/images/` directory is included in the structure for future local image hosting.

5. **No image lightbox**: The gallery does not support click-to-enlarge since that would require JavaScript. Hover effects provide visual feedback instead.

6. **Transparent header transition**: On the homepage, the header is transparent over the hero and does not dynamically switch to a solid background on scroll (that would require JavaScript scroll detection). Interior pages use a solid header by default.

---

## Browser Support

The site uses modern CSS features that are well-supported in current browsers:

- CSS Custom Properties (variables) — all modern browsers
- CSS Grid — all modern browsers
- Flexbox — all modern browsers
- `clamp()` — Chrome 79+, Firefox 75+, Safari 13.4+
- `column-count` — all modern browsers
- `:focus-visible` — Chrome 86+, Firefox 84+, Safari 15.4+
- `scroll-behavior: smooth` — all modern browsers
- `position: sticky` — all modern browsers
- `aspect-ratio` — Chrome 88+, Firefox 89+, Safari 15+

---

## How to Run

1. Open the project folder in any code editor or file browser
2. Double-click `index.html` to open it in a web browser
3. Navigate between pages using the header links or in-page CTAs

No build tools, package managers, or servers are required. The site works by simply opening the HTML files in a browser.

---

## Credits

- **Images**: [Pexels](https://www.pexels.com) — royalty-free stock photography
- **Fonts**: [Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond) and [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts
- **Design & Code**: Built as a pure HTML/CSS demonstration project

---

&copy; 2026 Stayora. All rights reserved.
