# nusami-site

The start page of **nusami.xyz**: "Test network, coming soon". A static site on Cloudflare Workers (static assets):

- `public/` — the whole site (HTML, CSS, font, images) and `public/_headers` (security headers);
- `wrangler.jsonc` — project `nusami-site`, assets from `./public`, unknown paths → `public/404.html`.

No build step. Cloudflare deploys on push with `npx wrangler deploy`.

Check locally (Node.js 18+): `npx wrangler dev`, open http://localhost:8787 — the page, a 404 page for `/nope`, and the
headers from `_headers` (`curl -I http://localhost:8787/`).

Test network. Tokens have no value. You can lose all funds. This is not advice.
