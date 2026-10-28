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

Check with the user before departing from these.

- **Audience and product truth** (users, positioning, evidence, principles) live in `PRODUCT.md`, confirmed by the user. Read it before design or copy work.
- **Visual system** (colours, type, layout, shapes, components, do's and don'ts) lives in `DESIGN.md`, with tokens in its YAML frontmatter and extras in `.impeccable/design.json`. Treat it as authoritative and regenerate both with `/impeccable document` after visual changes. Voice: calm, plain, first-person plural, with no hype.

- **No dark mode.** The site is light-only by decision, so don't add `prefers-color-scheme` styles.
- **No reference sites** have been chosen to aim toward or avoid yet.

Still open: how app listings should look once the apps ship. They will replace the `.empty` placeholder in `#apps`.
