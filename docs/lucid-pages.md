# Lucid beta information pages

Static, script-free pages under `public/lucid/` are copied unchanged by the CRA
build. They are deliberately absent from the main site's navigation and sitemap.
`noindex, nofollow, noarchive` appears both in HTML and Vercel response headers.
This discourages indexing; it is not authentication or a secrecy guarantee.

- `/lucid/privacy/`: current collection, providers, retention, and choices.
- `/lucid/support/`: contact and beta troubleshooting.
- `/lucid/delete-account/`: in-app deletion and broader data requests.
- `/lucid/terms/`: beta conditions and YouTube terms links.

Keep these pages synchronized with the app's actual behavior and App Store
Connect disclosures. A published notice does not replace required in-app consent.
Recheck provider settings, deletion behavior, and retention before each release.
Contact: infinite@julian.ai. Do not publish the private Apple review phone number.

The CSP applies only to the four published documents (including index.html
URLs), permits local CSS/images, and blocks scripts, frames and forms. Unknown
paths retain the React fallback; `/lucid/` redirects to support. The policy
headers do not change the React site's other routes. Node 22 replaces the previous
open-ended Node requirement because the linked Vercel project used retired Node 18.

Validation: production build with Node 22; browser checks at 320, 390 and 1280px;
200% text sizing; keyboard skip link; internal links and no horizontal overflow.
Always verify actual deployed page headings and headers: a missing CRA route can
return HTTP 200 with the homepage instead of the requested policy.
