# Elavora Spices website

Plain HTML, CSS and JavaScript. No build step, no dependencies. Works on GitHub Pages.

## Deploy on GitHub Pages
1. Create a new repository on GitHub (for example `elavora-spices`).
2. Upload everything in this folder to the repository root (the `index.html` file must be at the top level).
3. Repository **Settings > Pages > Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

All links and image paths are relative, so it works under that sub-path and on a custom domain.
To test locally, just double-click `index.html`.

## Where to edit
| What | File |
|---|---|
| WhatsApp number, Instagram, phone, currency | `js/config.js` |
| Products, pack sizes, prices, explore items, gallery photos, Instagram highlight circles | `js/data.js` |
| Colours, fonts, layout | `css/style.css` (colours are variables at the top) |
| Page text | `index.html`, `about.html`, `products.html`, `explore.html`, `contact.html` |

### Add a product
Copy a block in `PRODUCTS` (`js/data.js`). Set `status: "available"` and add `variants` with a `price` (for example `price: 450`) to show prices; use `status: "enquire"` until you have pack photos.

### Replace images
Keep the same file names, or change the paths in `js/data.js`.
- `assets/img/logo/` logo PNGs (cut from your poster) and favicons
- `assets/img/spices/` transparent PNG spice illustrations (cardamom, pepper, cloves, ...)
- `assets/img/products/` and `assets/img/gallery/` photos cropped from your packaging images. Replace with original high-resolution photos when you have them.

## Growing into an e-commerce site
Products already follow a shop-ready structure (`id`, `category`, `variants`, `price`). Later you can add a cart (store items in `localStorage`) and a payment link or gateway (Razorpay, Shopify Buy Button, Stripe) without changing the page layout. The buttons carry `data-product-id` and `data-variant` attributes for this.

## Please verify before publishing
- The nutrition values for cardamom (`js/data.js`) were copied from the 100 g label design.
- The "About" text is generic brand copy; replace it with your real story.
