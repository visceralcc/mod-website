# Mod website

The website for Mod, live at https://moddesign.io

## How to update the site

1. Edit the files inside the `public/` folder (the logo page is `public/index.html`).
2. From this folder, run:

   ```
   npm run deploy
   ```

That publishes your changes to Cloudflare. The domain stays connected automatically.

## One-time setup

- Install Node.js (LTS): https://nodejs.org
- Install dependencies: `npm install`
- Connect Wrangler to Cloudflare: `npx wrangler login`

## How it works

The site is a Cloudflare Worker that serves the static files in `public/`.
Settings live in `wrangler.toml`. Config files stay outside `public/`, so they
are never served on the web.
