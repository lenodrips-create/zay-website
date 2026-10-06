# FORGIVN

**Faith / Grace / Forever**

The storefront website for FORGIVN, a Christian clothing brand built around one idea: the F in the logo is a cross.

The whole site is a single file, `index.html`. It has no build step and no dependencies, so you can open it in a browser or upload it anywhere.

---

## What's on the page

From top to bottom:

1. **Dove intro.** A dove carrying an olive branch glides onto a black screen, then flies at the viewer, and the black opens up to show the site. It takes about 3 seconds.
2. **Top bar.** A three-line menu button on the left, the FORGIVN logo in the middle, and the cart icon and Contact button on the right.
3. **Hero.** A looping video of the cross in the clouds plays in the background, with the large FORGIVN logo and tagline in front.
4. **Moving banner.** A strip that scrolls "Faith ✝ Grace ✝ Forever ✝ Same God. New story."
5. **Shop by category.** Four round buttons: Hoodies, Camo, Tees and New Arrivals. Each one jumps to the shop and filters it.
6. **The Cross Collection (Drop 001).** Ten products with drawn clipart, prices and Add to cart buttons, plus filter buttons for All, Hoodies, Camo, Tees, Accessories and New.
7. **Our Story.** A short bio of Xay Carey.
8. **Journal.** A "coming soon" placeholder.
9. **Footer.** © 2026 Forgivn, and Ephesians 1:7.

## Features

- **Cart panel.** Lets shoppers change quantities, remove items and see the subtotal. The cart is saved in the visitor's browser, so it survives a refresh.
- **Contact form.** Has name, email and message fields, and checks that the email looks real before sending.
- **Menu panel.** Slides out from the left and links to Shop, Collection, About, Journal and Contact.
- **Animations:**
  - The logo builds itself on load: the cross drops in, then the letters wipe in.
  - The hero video slowly settles as the page opens.
  - The logo drifts up and fades as you scroll.
  - Categories, products and sections fade in as you scroll to them.
  - Product pictures tilt in 3D toward the mouse.
  - Items fly into the cart when added.
- **Phone-ready.** The category row and the product grid both drop to two columns on small screens.
- **Accessible.**
  - The keyboard can reach everything, and Escape closes any open panel.
  - Animations turn off for visitors who set their device to reduce motion.

## Products

| Product | Color | Price | Filters |
|---|---|---|---|
| Signature Hoodie | Black | $75 | Hoodies |
| Grace Hoodie | Brown | $75 | Hoodies |
| Camo Hoodie | Woodland camo | $80 | Hoodies, Camo, New |
| Essential Tee | Cream | $35 | Tees |
| Paid For Tee ("It Is Finished") | Charcoal | $35 | Tees |
| Redeemed Long Sleeve | Burgundy | $45 | Tees, New |
| Signature Hat | Washed charcoal | $30 | Accessories |
| Cross Beanie | Black | $28 | Accessories, New |
| Cross Bracelet | Black beads | $20 | Accessories |
| Faith Tote | Natural canvas | $25 | Accessories, New |

## Editing the site

Open `index.html` in any code editor and search for the text you want to change.

**Change a price or name.** Each product is an `<article class="prod">`. Change the price in two places:
- the `<p class="price">` text
- the `data-price` value on its Add to cart button

```html
<article class="prod" data-cat="hoodies">
  ...
  <h3>Signature Hoodie</h3>
  <p class="price">$75</p>
  <button class="add" data-name="Signature Hoodie" data-price="75">Add to cart</button>
</article>
```

**Change which filters a product shows up under.** Edit its `data-cat`. The values are `hoodies`, `camo`, `tees`, `accessories` and `new`, separated by spaces. Products that include `new` also need a `<span class="badge">New</span>` inside their picture box.

**Change the colors.** All the colors are set in the `:root` block at the top of the `<style>` section:

| Setting | Used for |
|---|---|
| `--bg` | the page background (pure black) |
| `--ink` | the cream color for text and the logo |
| `--muted` | the grey for secondary text |
| `--line` | the thin divider lines |

**Change the fonts.** The fonts are Oswald for labels and Cormorant Garamond for the italic text, both loaded from Google Fonts.

**Change Our Story.** Find `<section class="about" id="about">` and replace the paragraph inside it.

## Videos and file size

The hero video, its poster image and the dove intro are all embedded right inside `index.html`. That keeps it one file, but it makes the file about 2.4 MB.

For the live site, it's better to move them into separate files, such as `hero.mp4` and `dove.mp4`, and point the `src` at them. The page will load faster and the HTML will be easier to edit.

## Before going live

- [ ] **Checkout.** It isn't connected yet; the button shows a notice. Connect Shopify, Stripe or Snipcart.
- [ ] **Contact form.** It doesn't send messages yet. Connect a form service such as Formspree or Netlify Forms.
- [ ] **Product photos.** Replace the clipart with real product photos.
- [ ] **Shop pages.** Give each product its own page with sizes S–XXL.
- [ ] **Journal.** Write the Journal section.
- [ ] **Dove license.** The dove GIF is marked © 2001 Animation Factory. Confirm you have the rights to use it, or replace it.
- [ ] **Xay's privacy.** Our Story includes Xay's full name and age. Decide whether that should stay public.
- [ ] **Hosting.** Put it on Netlify, Vercel or GitHub Pages, and connect the domain (forgivn.co).

---

*"In Him we have redemption through His blood, the forgiveness of sins."* Ephesians 1:7
