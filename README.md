# Leftover Chef

A little left. A lot of possibility.

Pick the ingredients already in your fridge and Leftover Chef matches them against 24 easy recipes, with filters for cooking time, vegetarian and gluten-free. Recipes can be saved and printed. Quantities are shown in both US customary and metric units.

It is a single static page (`index.html`) with no build step, no server and no accounts. Saved recipes and your pantry stay in your own browser's local storage.

## Run locally

Open `index.html` in any modern browser.

## Deploy

Hosted on Cloudflare Pages:

```sh
npx wrangler pages deploy . --project-name leftover-chef
```
