# VASTRADEV

Premium everyday T-shirts. This repository contains the VASTRADEV storefront: a fast, responsive static website that runs directly on GitHub Pages with no build step and no dependencies.

## Features
- Product grid with category filters and price sorting
- Quick-view popup with colour and size selection
- Cart drawer saved in the browser, with free-shipping progress
- Orders sent to WhatsApp as a pre-filled message
- Size guide (inches / cm), FAQ and contact section
- Mobile-first, accessible, with SEO and social preview tags
- Custom 404 page

## Project structure
```
vastradev/
├── index.html      # main page
├── 404.html        # custom "page not found"
├── css/
│   └── styles.css  # all styling
├── js/
│   └── main.js     # products, cart, config
├── robots.txt
├── .nojekyll       # tells GitHub Pages to serve files as-is
├── .gitignore
├── LICENSE
└── README.md
```

## 1. Add your real details (important)
Open `js/main.js` and edit the `CONFIG` block at the top:

```js
email: "hello@vastradev.example",   // your email
whatsapp: "910000000000",           // country code + number, no + or spaces
freeShippingAbove: 999,
shippingFee: 79,
```

Then review the product list (names, prices, colours) in the same file, and the shipping and exchange answers in the FAQ section of `index.html`, so they match your real policies.

## 2. Publish on GitHub Pages
1. Create a new repository on GitHub, for example `vastradev`.
2. Upload every file in this folder (keep the `css` and `js` folders), or use the commands below.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select branch `main` and folder `/ (root)`, then **Save**.
5. After a minute or two your site is live at `https://<your-username>.github.io/vastradev/`.

```bash
git init
git add .
git commit -m "Launch VASTRADEV website"
git branch -M main
git remote add origin https://github.com/<your-username>/vastradev.git
git push -u origin main
```

Tip: naming the repository `<your-username>.github.io` publishes the site at `https://<your-username>.github.io/` with no sub-path.

## 3. Custom domain (optional)
Buy a domain (for example `vastradev.in`), then go to **Settings → Pages → Custom domain**, enter it and add the DNS records GitHub shows. Turn on **Enforce HTTPS**.

If you serve the site from a sub-path (`/vastradev/`) without a custom domain, change the "Back to VASTRADEV" link in `404.html` from `/` to `/vastradev/`.

## 4. Use real product photos (recommended)
Products currently use built-in vector T-shirt illustrations so the site works out of the box. When you have photography, add the images to an `images/` folder and replace the `shirtSVG(...)` calls in `js/main.js` with `<img>` tags.

## Before you take real orders
- Confirm your shipping, return and privacy policies, and consider adding dedicated pages for them.
- Add your business details (registration/GST number, address) in the footer where required.
- Add customer reviews only once you have real ones.
- Update `robots.txt` with a sitemap line once your final URL is known.

## License
Released under the [MIT License](LICENSE). The VASTRADEV name and branding remain the property of their owner.
