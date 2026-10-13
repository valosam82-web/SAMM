# VASTRADEV: T-shirt storefront

A fast, responsive static website for the VASTRADEV T-shirt brand. No build step, no dependencies: it runs directly on GitHub Pages.

## Features
- Product grid with category filters and sorting
- Quick-view modal with colour and size selection
- Cart drawer (saved in the browser), free-shipping progress, quantity controls
- Orders go to your WhatsApp as a pre-filled message
- Size guide with inches/cm toggle, FAQ, contact section
- Mobile-first, accessible, SEO meta tags, custom 404 page

## 1. Add your real details (important)
Open `js/main.js` and edit the `CONFIG` block at the top:

```js
email: "hello@vastradev.example",   // your email
whatsapp: "910000000000",           // country code + number
freeShippingAbove: 999,
shippingFee: 79,
```

Also review prices, products, and the shipping/exchange text in the FAQ section of `index.html` so they match your actual policies.

## 2. Publish on GitHub Pages
1. Create a new repository on GitHub, e.g. `vastradev`.
2. Upload all files in this folder (or run the commands below).
3. In the repo go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
5. After about a minute your site is live at `https://<your-username>.github.io/vastradev/`.

```bash
git init
git add .
git commit -m "Launch VASTRADEV website"
git branch -M main
git remote add origin https://github.com/<your-username>/vastradev.git
git push -u origin main
```

## 3. Custom domain (optional)
Buy a domain (e.g. `vastradev.in`), then in **Settings → Pages → Custom domain** enter it and add the DNS records GitHub shows. Enable **Enforce HTTPS**.

If the site is served from a sub-path (`/vastradev/`), the 404 page's "Back" link points to `/`; change it to `/vastradev/` if you are not using a custom domain.

## 4. Replace the illustrations with real photos (recommended)
Products currently use built-in vector T-shirt illustrations so the site works out of the box. When you have product photography, add images to an `images/` folder and swap the `shirtSVG(...)` calls in `js/main.js` for `<img>` tags.

## Before you take real orders
- Confirm your return, shipping and privacy policies, and consider adding dedicated pages for them.
- Add your business details (GST/registration, address) in the footer if required.
- Only add customer reviews once you have real ones.
