# VelocitySPX — marketing website

A single-page cinematic scroll site. Everything is local: no build step, no framework,
no external JavaScript. Open `index.html` in a browser and it works.

## Publishing to GitHub Pages

1. Create a repository (Pages on the free plan needs it to be **public** — the page
   currently carries `noindex,nofollow` so search engines will not list it).
2. Upload the whole contents of this folder to the root of the repository.
3. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
4. The site appears at `https://<user>.github.io/<repo>/` within a minute or two.
5. When you own the domain: add a file called `CNAME` containing `velocityspx.com`,
   point the DNS at GitHub, and remove the `noindex` line from `index.html` (line 6).

## What's in here

- `index.html` — the whole site: markup, styles, motion, copy.
- `assets/` — imagery, favicon, app icon, share card.
- `assets/vendor/` — GSAP, ScrollTrigger and Lenis, vendored locally so the site does
  not depend on a CDN staying up.

Fonts (Sora and Inter) load from Google Fonts. Both are open licence.

## Notes

- The whole film respects the operating system's "reduce motion" setting and falls
  back to a static, fully readable page.
- Every claim on the page was checked against what the software actually does for an
  in-house agency. Nothing that is switched off for in-house clients — invoicing, the
  agent portal, fee reporting — appears anywhere.
- `?jump=<pixels>` loads the page pre-scrolled to a position, for checking a section
  without scrolling to it.
