# Colorado AI Lab — coloradoailab.com

GitHub Pages static website. Single `index.html` with Tailwind CSS, Alpine.js, and Formspree lead capture.

## Deploy in 5 minutes

1. Push to GitHub: `git push -u origin main`
2. Go to repo → Settings → Pages → Source: **main branch, / (root)**
3. Point `coloradoailab.com` DNS to GitHub Pages (see below)

## Before going live — swap these placeholders

| Placeholder | Where | What to replace with |
|---|---|---|
| `YOUR_FORM_ID` | `index.html` script block | Your [Formspree](https://formspree.io) form ID |
| Calendly block | Thank-you step (step 6) | Your Calendly embed code |
| `G-XXXXXXXXXX` | `<head>` comments | Your GA4 Measurement ID (then uncomment) |
| `(720) 000-0000` | Footer | Real phone number |
| `hello@coloradoailab.com` | Footer | Real email address |

## DNS setup for coloradoailab.com (GitHub Pages)

Add these records at your domain registrar:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  semiagenticRob.github.io
```

Then add `coloradoailab.com` in repo Settings → Pages → Custom domain.

## Hero image

Currently using a free Unsplash mountain photo via CDN URL in `.hero-bg` CSS.
To replace with a local image: drop a `hero.webp` (<200KB, 1920px wide) into `/assets/`
and update the `url(...)` in the `.hero-bg` style block.

## Stack

- HTML5 (single file)
- [Tailwind CSS CDN](https://tailwindcss.com)
- [Alpine.js v3](https://alpinejs.dev)
- [Formspree](https://formspree.io) for form submissions
- [Calendly](https://calendly.com) embed for strategy call booking
- Google Analytics 4 (commented out until ID is set)
