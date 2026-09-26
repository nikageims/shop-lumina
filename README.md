# Lumina Ultimate — Next-Gen Immersive Marketplace

A single-file, front-end-only e-commerce demo built with vanilla JavaScript, Tailwind CSS, and Three.js. It simulates a full storefront — product catalog, search, filtering, cart, and checkout — entirely in the browser with no backend.

## Features

- **100+ product catalog** — 16 hand-crafted items plus 89 procedurally generated ones across 6 categories (Electronics, Accessories, Workspace, Apparel, Home & Kitchen, Gaming)
- **Live search with autocomplete** — instant results dropdown as you type, synced between desktop and mobile search bars
- **Category filtering & sorting** — filter by category pill, sort by price (low/high) or rating
- **Client-side routing** — simple hash-free router switching between Home (grid) and Detail (single product) views
- **Product detail pages** — full spec view with related-items recommendations from the same category
- **Shopping cart** — slide-out drawer with quantity controls, live subtotal/total, and a simulated checkout flow
- **3D visual flair**
  - Three.js particle field animated in the background, reacting to mouse movement
  - CSS 3D tilt effect on product cards on hover
- **Toast notifications** for cart actions and newsletter signup
- **Responsive, glassmorphism-styled UI** built with Tailwind CSS and Lucide icons

## Tech Stack

| Layer | Library |
|---|---|
| Styling | Tailwind CSS (CDN, Play CDN) |
| 3D graphics | Three.js r128 |
| Icons | Lucide |
| Font | Plus Jakarta Sans (Google Fonts) |
| Logic | Vanilla JavaScript (no framework, no build step) |

## Running It

This is a single self-contained HTML file — no installation or build process required.

1. Download the HTML file.
2. Open it directly in any modern browser (double-click, or `open index.html`).

That's it — all product data, state management, and rendering logic live inline in the file.

## Project Structure (single file)

```
index.html
├── <head>        — Tailwind config, custom CSS, font/icon imports
├── <header>      — Sticky nav bar with live search + cart button
├── <main>        — Dynamic view mountpoint (#appView)
├── <footer>      — Site links + newsletter signup
├── Cart drawer   — Slide-out panel with items, subtotal, checkout
└── <script>
    ├── PRODUCTS_DB          — Static + generated product data
    ├── state / router       — App state and view routing
    ├── renderHomeView()     — Product grid, filters, sorting
    ├── renderDetailView()   — Single product page + related items
    ├── Cart functions       — add/update/remove/checkout
    ├── Search functions     — live filtering + autocomplete
    └── Three.js background  — animated particle field
```

## Notes

- All data is in-memory and resets on page reload (no persistence layer).
- Product images are sourced from Unsplash via URL — an internet connection is needed to display them.
- This is a front-end demo/prototype; there is no real payment processing or backend order handling.

## License

For demonstration purposes.
