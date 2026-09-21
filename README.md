# CampusMarket — CCS 2314 Semester Project

Starter scaffold for Week 1 (**HTML/CSS**) of the development path:

```
HTML/CSS → JavaScript → validation/events → animation/media → AJAX/JSON
→ PHP → sessions/authentication → MySQL → CRUD → security/accessibility
→ shopping cart → checkout → final integrated application
```

## What's here now

```
CampusMarket/
├── index.html      Product browsing page (static placeholder data)
├── css/
│   └── style.css   All styling — layout, typography, responsive grid
├── js/
│   └── main.js      Empty-ish stub; Week 2 builds this out
└── images/          Empty; drop real product photos here later
```

## Why it's built this way

- **Static placeholder products** in `index.html` (`.product-card` items)
  stand in for what will eventually come from a MySQL `products` table.
  Keep the markup structure (class names, data attributes) the same when
  you later generate these cards with a PHP loop, so the CSS keeps working
  without changes.
- `data-product-id` and `data-category` attributes are already on each
  card — they're unused today but will make JS filtering (Week 2/3) and
  the real cart (Week 9) much less of a rewrite.
- `js/main.js` has a placeholder click handler on "Add to cart" so the
  page isn't inert, but it is **not** the real cart — no persistence, no
  server call. That's built for real once sessions + MySQL exist.

## Next steps, in order

1. **JavaScript**: wire up the search box and category-bar filtering
   against the in-page product data.
2. **Validation/events**: build a "list an item" form with client-side
   validation before it ever touches a server.
3. **PHP + MySQL**: move the product list into a database and render
   `.product-card`s with a PHP loop instead of hardcoded HTML.
4. **Sessions/auth**: make "Log in" / "Sign up" real.
5. **Shopping cart → checkout**: replace the placeholder cart counter
   with a persisted cart (session or DB-backed).

## Running locally

1. Put this folder inside your XAMPP `htdocs` directory.
2. Start Apache (and MySQL once you need it) from the XAMPP control panel.
3. Visit `http://localhost/CampusMarket/index.html`.
4. Keep committing to the **same** Git repository all semester — don't
   start a new project for each milestone.
