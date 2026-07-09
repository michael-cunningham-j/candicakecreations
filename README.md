# Candi's Cake Creations - Website

A responsive multi-page website for Candi's Cake Creations, a home-based bakery in Cedar Rapids, IA.

## File Structure

```
candis-cake-creations/
├── index.html              - Home (services, about, reviews, contact)
├── weddings.html           - Weddings & Anniversaries gallery
├── birthdays.html          - Birthdays gallery
├── cupcakes.html           - Cupcakes & cake balls gallery
├── specialty.html          - Specialty Creations (sculpted / one-of-a-kind cakes)
├── styles.css              - Global stylesheet (all pages)
├── script.js               - Mobile menu + gallery lightbox
├── README.md
└── images/
    ├── logo.jpg            - Business logo (used in the header of every page)
    ├── hero.jpg            - Home hero background
    ├── about.jpg           - About section photo
    ├── weddings/
    │   └── wedding-1.jpg ... wedding-4.jpg
    ├── birthdays/
    │   └── birthday-1.jpg ... birthday-3.jpg
    ├── cupcakes/
    │   └── cupcake-1.jpg ... cupcake-3.jpg
    └── specialty/
        ├── guitar-cake.jpg
        ├── swan-cake.jpg
        └── ghost-cake.jpg
```

## Adding More Photos

To add another photo to a gallery, drop the file into the correct folder and add
a matching gallery block in the page's HTML:

```html
<div class="gallery-item" data-caption="Your caption here">
  <img src="images/weddings/wedding-5.jpg" alt="Description of the cake">
</div>
```

The `data-caption` shows on hover; clicking the photo opens the lightbox.

## Editing Content

- **Business info** (phone, email, address) appears on every page's footer and on the
  home page's contact section. Search-and-replace to update once.
- **Reviews** on `index.html`: edit or add `.review-card` blocks in the Reviews section.
- **Contact form**: set the `action` attribute on the `<form>` in `index.html` to your
  Formspree endpoint, e.g. `https://formspree.io/f/YOUR_ID`.
- **Logo**: replace `images/logo.jpg` with any new logo file (keep the filename or update
  the `<img src>` in the navbar of every page).

## Brand Colors

Defined at the top of `styles.css` under `:root`. Change once, updates everywhere:
- `--pink` / `--pink-dark` - brand pinks
- `--cream` - background
- `--gold` - accent (buttons, review border)
- `--brown` - headings, footer

## Deploying to GitHub Pages

1. Push this folder to a GitHub repository.
2. Enable **GitHub Pages** in repo Settings > Pages > deploy from `main` branch, root.
3. Your site goes live at `https://<username>.github.io/<repo-name>/`.

## Responsive Features

- Hamburger menu on mobile (< 768px)
- Gallery grid auto-fits to screen width
- Contact form and about section stack on mobile
- Lightbox works on touch devices
