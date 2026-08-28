# THE SELLERS

A Shipfront marketing site. Three static pages, no build step, no dependencies.

- `index.html` - Home. Hero, value bar, four-step how it works, Warehousing / Fulfillment / eCommerce Integrations / Location, closing CTA.
- `get-a-quote.html` - Fast & Easy Quotes. Name, Email, Phone, Submit.
- `contact.html` - 1933 S. Broadway, Los Angeles CA 90007 and info@myshipfront.com.

Live: https://davidtphung.github.io/shipfront-the-sellers/

## Copy

All marketing copy comes from the live site at https://www.myshipfront.com/. Nothing here is invented: no prices, no SLAs, no testimonials, no partner logos.

## Design

- Ground `#000000`, type `#ffffff`, accent `#ff6a00`, Space Grotesk.
- Layout and chrome follow David's direction mock: numbered dark how-it-works cards, hero split, feature bar.
- Interaction model follows a Substrate-style dark SaaS page.
- Brand mark is the 1A EVEN cube: vertical corner up, three visible face edges, black fill, uniform bold orange stroke, `viewBox="0 0 24 26"`, nav size 27x30.

## Run locally

Any static server works. For example:

```bash
python3 -m http.server 43117
```

Then open http://127.0.0.1:43117.

## Deploy

The repo root is the site root. `.github/workflows/pages.yml` publishes the root of `main` to GitHub Pages on every push. There is no build step.

## Structure

```
index.html
get-a-quote.html
contact.html
assets/
  css/site.css
  js/site.js
```

The quote form is client side only. It validates the three fields, then hands the details to `info@myshipfront.com` via the visitor's mail client. Wire it to a real endpoint by replacing the submit handler in `assets/js/site.js`.

Built by David T Phung. 28 AUG 2026.
