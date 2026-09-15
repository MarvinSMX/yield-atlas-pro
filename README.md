# YieldAtlas PRO

Static site (GitHub Pages). Visual/CSS/JS cloned 1:1 from the competitor niche skin; **names, domains, Sheet, and Apps Script are ours**.

## Local preview

```bash
pnpm dlx serve .
# open http://localhost:3000
```

## Custom domain

`CNAME` → `yieldatlaspro.com`

GitHub Pages (user **marvinsmx**): Settings → Pages → Deploy from branch `main` / root (or `/docs`).

DNS:
- Apex `A` → GitHub Pages IPs (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`)
- `www` `CNAME` → `marvinsmx.github.io`

## Data (Google Sheet CSV)

1. Create a Google Sheet with columns matching this site’s table (see `data/seed.csv`).
2. File → Share → **Publish to web** → CSV.
3. Replace `REPLACE_ME_*` in HTML `CSV_URL` with your publish URL:

```
(n/a)
```

Seed file: `data/seed.csv` (upload these rows to bootstrap; never ship competitor publish IDs in production HTML).



## Ads

Advertise pages use **mailto:advertise@mrvn.me** (rate card on-page). Optional Stripe Payment Link can replace mailto later — leave placeholder until created.

## PRO note

ETF network sites have **no auth**. YieldAtlas PRO (separate folder `yield-atlas-pro/`) uses Stripe Payment Links + a secret member HTML URL.

## Payments (placeholders)

Replace every `https://buy.stripe.com/REPLACE_ME_YIELD_ATLAS_PRO` with your real Stripe Payment Links:

| Plan | Approx competitor price | Your Payment Link |
|------|-------------------------|-------------------|
| Monthly | $12.95/mo | `buy.stripe.com/...` |
| Lifetime | $74.95 | `buy.stripe.com/...` |

Flow: Payment Link → `thanks.html` → secret member page `authorized2026.html` (URL is the key; **no username/password**).
