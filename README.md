# NOCTRA — Premium Urban Fashion E-commerce

Portfolio project: a complete urban fashion e-commerce site, built with **plain HTML, CSS, and JavaScript** (no frameworks, no build dependencies). Minimalist, luxury-streetwear design — black, white, grey, and silver accents — inspired by brands like Fear of God and Represent.

> ⚠️ This is a fictional project built for portfolio purposes. All payments, products, and user data are simulated.

---

## 🚀 How to view it

No installation or build step required. Two options:

1. **Direct:** open `index.html` in any modern browser.
2. **With a local server** (recommended, avoids path/`fetch` restrictions in some browsers):
   ```bash
   npx serve .
   # or
   python3 -m http.server 8000
   ```
   Then visit `http://localhost:8000`.

---

## 🗂️ Project structure

```
├── index.html              Main homepage
├── tienda.html              Catalog with filters, sorting, and search
├── producto.html             Product detail (gallery, zoom, reviews)
├── carrito.html                Cart + checkout (4 payment methods)
├── cuenta.html                   Login / register / orders / favorites / addresses
├── coleccion.html                  Individual collection page
├── promociones.html                  Active promotions
├── lista-espera.html                   Countdown + launch waitlist signup
├── blog.html                            Blog + publishing panel
├── admin.html                            Owner's admin dashboard
├── 404.html                              Custom error page
├── favicon.svg
├── css/
│   └── style.css            Global design system (variables, components)
├── img/                      Real project photography (products, collections, gallery...)
└── js/
    ├── data.js              Simulated database (products, blog, coupons...)
    ├── main.js              Header, cart, favorites, drawers, UI utilities
    └── tienda.js / producto.js / carrito.js / cuenta.js / ...
```

Every HTML page loads `data.js` → `main.js` → its own page-specific script, in that order.

---

## ✨ Implemented features

- **Catalog:** filter by category/size/color, sorting, live search.
- **Product page:** touch-swipe gallery with zoom, size/color selection, reviews (read + write), related products, restock notification for sold-out items.
- **Cart & checkout:** coupons, automatic free shipping threshold, 4 simulated payment methods (Card, PayPal, Mercado Pago, Bank Transfer), order history.
- **Account:** simulated login/register, orders, favorites, addresses.
- **Collections:** dedicated page per collection with its own hero photo.
- **Promotions:** coupons that auto-apply straight from the promotions page.
- **Waitlist:** live countdown to the next product launch.
- **Blog:** category filter, article modal, working publishing form.
- **Admin panel:** full product CRUD (price, stock, photos, sizes, colors), promotion controls, order overview — all changes reflect live on the storefront.
- **Persistence:** all state (cart, favorites, session, orders, admin edits) lives in `localStorage`, making the whole site fully interactive without a backend.

---

## 🖼️ Photography

The project uses real photography (`img/` folder), distributed as follows:

| Use | Content |
|---|---|
| Product cards | Denim Jacket Legacy, Polo Uncommon, Cargo Pants Shadow |
| Collection heroes | Uncommon, Shadow Line, Elevate, Legacy (one photo per collection) |
| Homepage gallery | 3 editorial photographs |
| Brand story section | Store interior photo |
| Promotions | Campaign banner |
| Waitlist | Upcoming launch background image |

Remaining products use stock imagery (Unsplash) as placeholders, easily swappable from `js/data.js`.

---

## 🛠️ Technical decisions

- **No frameworks:** plain HTML/CSS/JS, meant to demonstrate solid fundamentals.
- **Shared state via `localStorage`:** simulates a real database without needing a server.
- **`main.js` as a shared layer:** header, cart/profile drawers, favorites, and UI utilities are shared across every page to avoid duplication.
- **Centralized data in `data.js`:** products, collections, coupons, blog, testimonials, etc. live in a single, easy-to-edit file.
- **Live-connected admin panel:** changes made in `admin.html` (price, stock, new products, promotions) merge into `BT_DATA` on every page load, so the site always reflects the latest state.

---

## 📌 Roadmap (v2 — future improvements, non-blocking)

- Full-screen lightbox for product zoom.
- Real "2x1" promotion logic applied in the cart.
- Edit/delete already-published blog posts.
- Card validation with the Luhn algorithm.
- Real backend (or Supabase/Firebase) to replace `localStorage`.
- True multi-user support in the account panel.
- Replace remaining stock images with original photography.

---

## 👤 Author

Built as a front-end portfolio piece.
