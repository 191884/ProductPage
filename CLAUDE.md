# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

The static marketing and legal site for Sage Lab, an independent mobile app studio, served by GitHub Pages at `sagelab.in` (`CNAME`). It is plain HTML and one stylesheet: no build step, package manager, JavaScript, linter or tests. GitHub Pages deploys from `main` at the repo root.

Preview locally with:

```bash
python3 -m http.server 8000
```

## Structure that spans files

- **Shared chrome is copied, not included.** Every page (`index.html`, `privacy.html`, `terms.html`, `404.html`) has its own copy of the `<head>` (Google Fonts link, `assets/style.css`, favicon, `theme-color`), the skip link, `.site-header` and `.site-footer`. A change to the nav, footer, fonts or contact email must be made in all four files. Pages other than the home page link back with `./#apps` and `./#contact`.
- **Links stay relative** (`./`, `assets/...`, `privacy.html`) so the site also works when served under a subpath. Don't add root-absolute `/` paths. Canonical, OG and JSON-LD URLs in `<head>` are the exception and use `https://sagelab.in/...`.
- **Styling** lives entirely in `assets/style.css`. Design tokens are CSS custom properties on `:root`: the palette (`--mist`, `--paper`, `--ink`, `--sage`, `--leaf`, `--cobalt`, ...) and fonts (`--display` = Bricolage Grotesque, `--body` = Hanken Grotesk). Breakpoints are 820px and 480px. Motion is gated behind `prefers-reduced-motion: no-preference`. The hero's phone mockups on the home page are pure CSS built from empty `<span>`/`<div>` elements.
- **Legal pages** (`privacy.html`, `terms.html`, and `404.html`, which reuses the layout) use `main.legal > .wrap > article` with a `p.updated` date line. `privacy.html` has a third-party services table (AdMob, Firebase, AppMetrica, Adapty, Play/App Store billing). Keep it in sync with the SDKs the apps actually ship.

## When editing

- `https://sagelab.in/privacy.html` is the privacy policy URL registered in Play Console. Don't rename or move it.
- When you change a page's content, update its `<lastmod>` in `sitemap.xml`. For the privacy policy or terms, also update the "Last updated" line.
- Business details appear in several places: the contact email `aman@sagelab.in`, Bhiwani, Haryana, and the Udyam number. They're in the page bodies, the footers and the JSON-LD block in `index.html`. Change all of them together.
- `assets/email-logo.png` is for email signatures. Pages don't reference it.

## Impeccable skill

`.claude/skills/impeccable/` is a copy of the Impeccable design skill (https://github.com/pbakaus/impeccable, skill v4.8.0, engine 0.1.18), taken from that repo's `.claude/skills/impeccable`. Use it as `/impeccable <command> [target]`, e.g. `init`, `audit`, `critique` or `polish`. Its launcher, `scripts/impeccable`, downloads a checksum-verified engine binary from the repo's GitHub releases into `~/.impeccable/bin/` on first run. To update the skill, copy the folder again from upstream rather than editing it here. `/impeccable init` writes product context to `PRODUCT.md`, and `/impeccable document` writes the visual system to `DESIGN.md`. Once those files exist, they take precedence over the design context below.

## Design context

This section is inferred from the current site, not from a brief. Treat it as the default direction, and check with the user before departing from it.

- **Audience and product truth** (users, positioning, evidence, principles) live in `PRODUCT.md`, confirmed by the user. Read it before design or copy work.
- **Personality:** calm, honest, small and competent. Copy is short, first-person plural, and plain about ads, data and subscriptions. No hype, superlatives or startup buzzwords.
- **Palette:** muted sage greens on an off-white mist (`--mist` page, `--paper` cards), with deep green `--ink` for text and solid surfaces. `--cobalt` is the only saturated colour. It's reserved for links and focus rings, so don't use it decoratively.
- **Type:** Bricolage Grotesque (600–800) for display, set tight (negative letter-spacing, line-height around 1) and large via `clamp()`. Hanken Grotesk (400/600) for body at 1.0625rem/1.6. Secondary text uses `--ink-soft`, not lighter weights.
- **Shapes:** big rounded radii (22–28px on cards, pill buttons) and 1.5px hairlines in `--line`. Surfaces are flat, with a single soft shadow on the front hero phone. Illustrations are abstract CSS/SVG phone UIs drawn from the palette, never stock imagery or real app screenshots.
- **Motion:** minimal. One fan-out on hero load, only under `prefers-reduced-motion: no-preference`.
- **Accessibility:** keep the skip link, visible `:focus-visible` outlines, `aria-hidden` on decorative art, and semantic landmarks on every page.

- **No dark mode.** The site is light-only by decision, so don't add `prefers-color-scheme` styles.
- **No reference sites** have been chosen to aim toward or avoid yet.

Still open: how app listings should look once the apps ship. They will replace the `.empty` placeholder in `#apps`.
