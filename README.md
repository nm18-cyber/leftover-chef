# Leftover Chef

A little left. A lot of possibility. Live at **https://leftover-chef.pages.dev**

Pick the ingredients already in your fridge and Leftover Chef matches them against 24 easy recipes.

- Quick-select ingredient capsules (proteins, veggies, carbs, fruit & extras) or type your own
- Filters for cooking time, vegetarian and gluten-free
- Recipe view with a 1 / 2 / 4 serving scaler, tick-off ingredients and steps (remembered between visits), and real prep and cook times
- Every quantity in both US customary and metric units
- Save favourites, share a link to any recipe, print a clean copy
- Light and dark mode (follows your device, or use the toggle)

It is a single static page with no build step, no server and no accounts. Everything you save stays in your own browser's local storage.

## Files

```
public/              everything that gets published
  index.html         the whole app (HTML, CSS and JavaScript)
  og-image.png       1200 × 630 image shown when the link is shared
  favicon.svg/.ico   browser tab icon
  apple-touch-icon.png  home-screen icon
.github/workflows/deploy.yml   automatic deploy to Cloudflare Pages
```

To try changes locally, open `public/index.html` in a browser.

## Deploying

Every push to `main` that changes `public/` deploys automatically through GitHub Actions, once this one-time setup is done:

1. In Cloudflare, go to **My Profile → API Tokens → Create Token → Create Custom Token**. Give it the permission **Account → Cloudflare Pages → Edit**, then create it and copy the token.
2. In this GitHub repo, go to **Settings → Secrets and variables → Actions → New repository secret**. Name it `CLOUDFLARE_API_TOKEN` and paste the token.

To deploy by hand instead:

```sh
npx wrangler pages deploy public --project-name leftover-chef --branch main
```
