# Hyper India — Product Affiliate Website

## Render deployment (important)
This ZIP is arranged so that `package.json` is at the project root. When creating the Render Web Service, connect this repository and use:

- Runtime: Node
- Branch: `main`
- Root Directory: leave blank
- Build Command: `npm install`
- Start Command: `npm start`

The project pins Node.js 20 using `.node-version` and `package.json` to avoid native SQLite build failures on newer Node versions.

## Environment variables
Set these in Render → Environment:

- `NODE_ENV` = `production`
- `SESSION_SECRET` = a long random secret (do not share it)
- `ADMIN_EMAIL` = your admin email
- `ADMIN_PASSWORD` = a strong unique password
- `BASE_URL` = your deployed HTTPS website URL

For persistent data on Render, attach a persistent disk and set `DB_PATH` and `SESSION_DIR` to paths on that disk (for example `/var/data/hyper-india.sqlite` and `/var/data`). Without persistent storage, SQLite data may be lost when the service is recreated. The included session store uses SQLite as well.

## Run locally
Install Node.js 20, then run `npm install` and `npm start`. Open `http://localhost:3000`.

## Current functionality and limitations
- Product listing, categories/search, member registration/login, referral link attribution, outbound click tracking, affiliate dashboard and payout request API.
- Admin data and product/commission/payout APIs are included, but a complete visual admin panel is not yet included.
- Demo product links use `example.com`; replace them with your own approved affiliate URLs.
- Amazon, Flipkart and Meesho are not automatically connected. You must join each affiliate program and use approved links under its terms. Confirm that any sub-affiliate sharing model is permitted before offering commissions to your own members.
- Purchase attribution and commission confirmation depend on the affiliate network. Clicks alone do not mean a sale or earned commission.
- Payouts are manual requests; no payment gateway or automatic payout is connected.
- Before public launch, add email verification, password reset, rate limiting, CSRF protection, audit logs, privacy/terms pages, backups and a security/legal review.
- Never collect a user's UPI PIN, OTP, card PIN or banking password.
