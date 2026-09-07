# LaunchPad Fair

Landing page for LaunchPad Fair — premium AI prompt toolkits and Arduino digital project kits.

## Live Site

Deployed via GitHub Pages: `https://<your-username>.github.io/<repo-name>`

## What's Included

- Hero section with main CTA
- Value proposition
- 4 toolkit pillars (prompts, Notion workspace, AI configs, lifetime updates)
- Arduino digital product grid (auto-generated from a JS array)
- Bank/payout connect section for seller payments
- Closing CTA with checkout link

## Adding a New Product

Open `index.html`, find the `products` array near the bottom of the file (inside the `<script>` tag), and add a new object:

```js
{
  name: "Product Name",
  desc: "Short one-line description.",
  price: "$XX",
  checkoutUrl: "https://yourstore.lemonsqueezy.com/buy/xxxxxxxx"
}
```

The page builds the product card automatically — no HTML editing needed.

## Payment Setup

Checkout is handled through [Lemon Squeezy](https://www.lemonsqueezy.com):

1. Create a store and connect your bank/payout details in Lemon Squeezy settings.
2. Create one product per item (toolkit bundle, each Arduino kit).
3. Copy each product's **Buy Link** into its `checkoutUrl` field in `index.html`.
4. Update the `connect-bank` button `href` and the closing CTA button `href` with your live links.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Branch** to `main`, folder to `/ (root)`.
4. Save — site goes live at `https://<your-username>.github.io/<repo-name>` within a few minutes.

## Tech

Single-file static site — plain HTML, CSS, and vanilla JS. No build step, no dependencies. Fonts loaded from Google Fonts (Plus Jakarta Sans, Inter).
