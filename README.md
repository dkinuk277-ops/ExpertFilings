# expert-filings.com

Website for Expert Filings (Ravi Kumar) — income tax, GST and financial guidance, India.

- Static site in `public/` (`index.html`, single page, tabbed)
- `src/worker.js` serves the site and handles `POST /api/enquiry` (sends enquiries via Resend, `src/enquiry.js`)
- Hosting: Cloudflare Workers project `expertfilings`, connected to this repo. Every push to `main` builds and deploys (`wrangler.jsonc`)
- Secrets (Cloudflare > expertfilings > Settings > Variables and Secrets): `RESEND_API_KEY` (required), `TO_EMAIL`, `FROM_EMAIL` (optional)
