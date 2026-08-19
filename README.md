# warrenbg.com

Corporate site for **Warren Business Group LLC** — a Wyoming limited liability company
operating as a **commodity trading and supply business** sourcing physical commodity
material in Mexico and the wider Latin American region, and working through the
**Commod** platform (`https://commod.network/`).

Plain static HTML/CSS, no build step, no JavaScript, no third-party requests. Matches the
stack of the other portfolio properties and deploys on Cloudflare Pages with no build
command.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Positioning, what the business does, what it does not promise, contact |
| `commod.html` | Interstitial explaining Commod and linking out to `commod.network` |
| `properties.html` | The nine web properties, footer-linked only, with the honesty panel |
| `terms.html` | Terms of use — no-offer / no-solicitation / no-placement-undertaking |
| `privacy.html` | Privacy policy — the site still collects nothing |
| `404.html`, `robots.txt`, `sitemap.xml`, `favicon.svg` | Housekeeping |

## Deploy settings (Cloudflare Pages)

- Cloudflare Pages project: **`warrenbg`** (`warrenbg.pages.dev`)
- Framework preset: **None**
- Build command: *(leave empty)*
- Build output directory: **/**
- Production branch: **main**

## Deliberate omissions

- **No AdSense, no analytics, no cookies, no contact form, no form handler.** The privacy
  policy states the site collects nothing; that must stay true. Do not add ad or analytics
  code without rewriting `privacy.html` to match.
- **No `ads.txt`** — there is no advertising on this site.
- Email is a plain `mailto:`. Cloudflare's Email Address Obfuscation rewrites it at serve
  time, which is the same pattern used across the other properties.
- The Commod link is a **plain untracked link**. Do not invent a `?ref=` parameter — an
  untracked parameter would falsely suggest attribution exists. See the
  `TODO(owner)` comment in `commod.html`; swap in a real tracked URL only when Commod
  supplies one.

## Content rules

Every factual claim on this site must be verifiable. Specifically, this site must never:

- publish **tonnages, volumes, shipments, assay results, offtakes, client or counterparty
  names, testimonials, years-in-trade, licences, certifications, memberships or team bios**;
- claim **ownership or control of any mining concession, título or water right**;
- **promise placement** — state or imply that any material will be bought, sold, placed,
  verified or accepted, or on what terms;
- use **investment, securities, financing or returns language**, or solicit capital;
- claim **export permits, customs authorisations or KYC/AML programmes** that do not exist;
- publish any **commercial terms** of the Commod arrangement — fees, floors, term, tail,
  schedules or counterparty names are all off-limits;
- imply that material sourced for export is routed anywhere other than **Commod**.

This is the site that vouches for the owner's credibility with mining counterparties. An
invented claim here is more expensive than a thin page.

## Do not touch

**DNS.** No record changes, and specifically none to `MX`, `SPF`, `DKIM` or `DMARC` — the
owner's email runs on this zone and was restored on 2026-08-18 after an outage. See
`_project-os/resources/servers/WARRENBG_EMAIL_RESTORE_2026-08-18.md`.
