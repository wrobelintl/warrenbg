# warrenbg.com

Corporate site for Warren Business Group LLC. Plain static HTML/CSS, no build step,
no JavaScript, no third-party requests. Matches the stack of the other portfolio
properties and deploys on Cloudflare Pages with no build command.

## Deploy settings (Cloudflare Pages)

- Framework preset: **None**
- Build command: *(leave empty)*
- Build output directory: **/**
- Production branch: **main**

## Deliberate omissions

- **No AdSense, no analytics, no cookies, no contact form.** The privacy policy
  states the site collects nothing; that must stay true. Do not add ad or
  analytics code without rewriting `privacy.html` to match.
- **No `ads.txt`** — there is no advertising on this site.
- Email is a plain `mailto:`. Cloudflare's Email Address Obfuscation rewrites it
  at serve time, which is the same pattern used across the other properties.

## Content rule

Every factual claim on this site must be verifiable. No client counts, no
testimonials, no case studies, no team bios, no founding-date or years-in-business
figure unless it can be sourced. This is the site that vouches for the others.
