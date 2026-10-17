# Anthony Nguyen — Game Operations Portfolio

A responsive portfolio website with a live Roblox tracker. Built as a static HTML/CSS/JS site with Cloudflare Pages Functions as lightweight API proxies. No Discord bot token, Roblox cookie, or other secret is required.

## Included
- Portfolio and selected case studies
- 13 experiences from the existing `index.js` configuration (the prior summary mentioned 12, but the source list has 13)
- Live current players, visits, game thumbnails, creator, and creation date from public Roblox endpoints
- Discord approximate member counts for configured invite codes
- Rolimon's all-time peak CCU where available
- Automatic refresh every 5 minutes, manual refresh, search, and active-game filter
- Local cache so last fetched values can display while reconnecting

## Deploy free to Cloudflare Pages
1. Sign in to Cloudflare and open **Workers & Pages**.
2. Create a Pages project from a Git repository, or use Direct Upload if your account's dashboard supports uploading this project structure. Git integration is recommended because it deploys future changes automatically.
3. Upload/push the contents of this folder to a GitHub repository.
4. Create a Pages project connected to that repository. Framework preset: **None**. Build command: leave blank or use `exit 0`. Build output directory: `/` (the repository root).
5. Deploy. Cloudflare will assign a free `*.pages.dev` address; you do not need to buy a domain.

Important: the `/functions` directory must be at the project root for the live API routes to work. Do not upload only `index.html` as a lone static file if you want API-backed live data.

## Before publishing
- Replace `hello@example.com` in `index.html` with your preferred professional contact email.
- Review the education/current status wording and selected portfolio metrics.
- The metrics on the hero are manually stated portfolio milestones; tracker cards are live API values. Peak CCU or Discord member counts may show unavailable if the source is down, blocks requests, or has no public data.
- The source tracker config includes 13 games even though an earlier summary said 12; all 13 are included.

## Local preview
Use a local static server that supports Cloudflare Pages Functions for the complete API-backed preview, e.g. install Wrangler and run `npx wrangler pages dev .`. Opening `index.html` directly from the filesystem will not run `/api/*` functions.
