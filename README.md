# Hyper India — Product Affiliate Platform starter

Responsive product discovery site with product cards, categories, search, partner outbound links, member accounts, referral attribution, click tracking, affiliate dashboard, payout requests and an admin panel.

## Run locally
- Install Node.js 20+.
- Copy `.env.example` to `.env`.
- Set a long random `SESSION_SECRET`, a strong unique `ADMIN_PASSWORD`, and `ADMIN_EMAIL`.
- Run `npm install` then `npm start`.
- Open http://localhost:3000.

## Admin
Log in with the admin credentials from `.env`. Open `/api/admin` after login to inspect the admin data endpoint. This starter includes API endpoints for adding products, recording verified commissions and processing payout requests; an admin UI for these actions is a next development step. Add products using `POST /api/admin/product` with JSON fields: title, category, price, merchant, image, affiliate_url, description. Record a verified commission using `POST /api/admin/commission` with userId, amount, note. Mark payout requests using `POST /api/admin/payout/:id` with status `paid` or `rejected`.

## Important
- Demo product links point to example.com. Replace them with your own approved affiliate URLs before launch.
- Amazon, Flipkart and Meesho are not automatically connected. Apply to each program, obtain approval, use their permitted affiliate links and follow their current terms. Some programs restrict sub-affiliate arrangements; verify permission before sharing commissions with your own users.
- Affiliate commissions are not guaranteed. Clicks are tracked, but purchase attribution and actual commission confirmation depend on the partner network. Admin must record commissions only after verified partner reports.
- Payouts are manual requests; no payment gateway or automated payout integration is included.
- Before public launch add email verification, password reset, rate limiting, CSRF protection, audit logs, admin product-management UI, privacy/terms pages, backup strategy, persistent storage, security review and applicable tax/legal review.
- Never ask users for UPI PIN, OTP, card PIN or banking password.
- For Render: build `npm install`, start `npm start`; set `NODE_ENV=production`, `BASE_URL`, secrets and a persistent disk. Set `DB_PATH` and `SESSION_DIR` to the mounted disk path.
