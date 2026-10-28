---
name: Sage Lab
description: Calm, plain-spoken studio site in sage greens on mist, with big tight display type and flat rounded surfaces.
colors:
  deep-forest-ink: "#17322b"
  forest-night: "#0f241f"
  moss-shadow: "#4a6159"
  sage-leaf: "#7e9c8b"
  pale-shoot: "#cfe3d5"
  lichen-whisper: "#b9cfc2"
  morning-mist: "#eef2ef"
  field-paper: "#fbfcfb"
  pressed-fern-line: "#d3ddd7"
  signal-cobalt: "#2f4bd8"
typography:
  display:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "clamp(3.25rem, 9.5vw, 7.5rem)"
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: "-0.045em"
  headline:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "clamp(2rem, 4.5vw, 3rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "-0.03em"
  headline-legal:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 6vw, 3.5rem)"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: "-0.035em"
  title:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "1.35rem"
    fontWeight: 700
    letterSpacing: "-0.015em"
  lede:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "1.15rem"
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 400
  label-strong:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 600
rounded:
  focus: "4px"
  control: "6px"
  tile: "10px"
  card: "22px"
  article: "24px"
  panel: "28px"
  pill: "999px"
spacing:
  xs: "0.6rem"
  sm: "1rem"
  gutter: "1.25rem"
  md: "1.5rem"
  lg: "2rem"
  xl: "3rem"
  container: "72rem"
components:
  button-primary:
    backgroundColor: "{colors.deep-forest-ink}"
    textColor: "{colors.field-paper}"
    typography: "{typography.label-strong}"
    rounded: "{rounded.pill}"
    padding: "0.85rem 1.4rem"
  button-primary-hover:
    backgroundColor: "{colors.forest-night}"
    textColor: "{colors.field-paper}"
  nav-link:
    textColor: "{colors.moss-shadow}"
    typography: "{typography.label}"
  nav-link-hover:
    textColor: "{colors.deep-forest-ink}"
  contact-panel:
    backgroundColor: "{colors.deep-forest-ink}"
    textColor: "{colors.field-paper}"
    rounded: "{rounded.panel}"
    padding: "clamp(2rem, 6vw, 4rem)"
  legal-article:
    backgroundColor: "{colors.field-paper}"
    textColor: "{colors.deep-forest-ink}"
    rounded: "{rounded.article}"
    padding: "clamp(1.5rem, 5vw, 3.5rem)"
  empty-state:
    textColor: "{colors.deep-forest-ink}"
    rounded: "{rounded.card}"
    padding: "clamp(1.75rem, 5vw, 3rem)"
  skip-link:
    backgroundColor: "{colors.deep-forest-ink}"
    textColor: "{colors.field-paper}"
    rounded: "{rounded.control}"
    padding: "0.5rem 1rem"
---

# Design System: Sage Lab

## Overview

**Creative North Star: "The Quiet Workshop"**

Sage Lab looks like a calm, well-kept studio bench. The tools are laid out plainly, nothing is there for show, and the craft is in the details. The page is a soft field of mist and paper greens, and one confident voice speaks over it: very large, tightly set Bricolage Grotesque headlines. Everything else steps back. Body text is relaxed and readable, surfaces are flat, and colour stays inside one green family. The only exception is the cobalt that marks something you can act on.

Density is low and unhurried. Sections breathe on generous vertical padding, content sits in a single 72rem column, and each section makes one point. The hero illustration of three fanned, abstract phone screens is drawn from the same palette as the page. It suggests "we make apps" without showing an app that doesn't exist yet. Depth comes from tone (mist, paper, ink) rather than shadow.

Components feel **soft but sure**. Corners are generously rounded and colours are calm, but actions are solid, high-contrast and unambiguous. Nothing is tentative or ghosted.

**Key Characteristics:**
- One green family, from deep forest ink to near-white mist, with cobalt reserved for interaction.
- Oversized, tight-tracked display type against relaxed, readable body text.
- Flat tonal layering: mist page, paper cards and an ink panel for emphasis.
- Big rounded corners (22–28px) and pill-shaped actions.
- Abstract, palette-drawn illustration only, never photos or real screenshots.
- Light theme only.

## Colors

A restrained botanical palette of greys tinted green, with a single saturated blue kept for interaction.

### Primary
- **Deep Forest Ink** (`deep-forest-ink`): text colour on every page, and the fill for the strongest surfaces: the primary button, the contact panel and the skip link. It's the system's anchor. Wherever the eye should land and act, it's ink.
- **Forest Night** (`forest-night`): the pressed or hover state of ink surfaces, used only for primary-button hover.

### Secondary
- **Sage Leaf** (`sage-leaf`): the mid-green accent for illustration fills, the dashed empty-state border, and the underline beneath the contact email. It's decorative weight, not text.
- **Pale Shoot** (`pale-shoot`): the light green for illustration bars, the back phone and the hover underline on the contact email. It also serves as the focus colour on the ink panel.

### Tertiary
- **Signal Cobalt** (`signal-cobalt`): links and `:focus-visible` outlines on light surfaces. It's the only saturated hue in the system.

### Neutral
- **Morning Mist** (`morning-mist`): the page background and `theme-color`.
- **Field Paper** (`field-paper`): raised surfaces (the About section band, legal articles, phone screens) and text on ink.
- **Moss Shadow** (`moss-shadow`): secondary text (ledes, descriptions, nav links, footer, "last updated" lines).
- **Lichen Whisper** (`lichen-whisper`): secondary text on the ink panel.
- **Pressed Fern Line** (`pressed-fern-line`): hairline dividers, table rules and phone outlines.

### Named Rules
**The Cobalt Means Click Rule.** Signal Cobalt appears only on links and focus outlines. Never use it as a fill, an illustration colour or a heading colour. If it's blue, you can act on it.

**The One Family Rule.** Every neutral is tinted toward green (hue around 150–175). Don't introduce pure greys, pure black or a second accent hue.

## Typography

**Display Font:** Bricolage Grotesque, weights 600–800 (with system-ui, sans-serif)
**Body Font:** Hanken Grotesk, weights 400 and 600 (with system-ui, sans-serif)

**Character:** Bricolage brings a slightly quirky, optical-size-aware grotesque that reads as handmade confidence when set huge and tight. Hanken Grotesk is a quiet, even workhorse that keeps long policy text easy to read.

### Hierarchy
- **Display:** the hero `h1` only. Set enormous, with line-height under 1 so the wordmark-scale headline locks together.
- **Headline:** section `h2`s, capped at 20ch so they wrap into short, punchy lines.
- **Headline (legal):** the `h1` on the privacy, terms and 404 pages. Slightly smaller than the hero, same tight voice.
- **Title:** `h3`s in principle lists and the empty state, plus `h2`s inside legal articles at 1.4rem.
- **Lede:** the intro paragraph under a section headline, in Moss Shadow, up to 38rem wide.
- **Body:** all running text. Legal paragraphs are capped at 68ch.
- **Label:** nav, footer and small metadata (`dt` at 0.9rem). The strong variant (600) is for buttons and table headers.

### Named Rules
**The Weight Not Grey Rule.** Hierarchy comes from size and the display face, and secondary text uses Moss Shadow. Don't use lighter font weights or reduced opacity to de-emphasise text.

**The Tight Display Rule.** Bricolage at headline size and above always carries negative letter-spacing (−0.015em to −0.045em, getting tighter as it gets larger). Body text is never tracked.

## Layout

A single centred column, `container` (72rem) wide, with a 1.25rem side gutter. Sections stack vertically with fluid padding (`clamp(3.5rem, 8vw, 6rem)` top and bottom). The hero is a two-column grid (about 1.15fr text to 1fr illustration). The About section uses a 1fr / 1.4fr split, with the headline and lede beside the principles list. The contact panel splits about 1.3fr / 1fr, aligned to the bottom.

Responsive behaviour has two breakpoints. At **820px and below**, every split collapses to one column, the phone illustration moves above the hero text and shrinks to a 22rem maximum, and the empty state stacks its icon above its text. At **480px and below**, nav gaps tighten and the About link hides. Type scales fluidly with `clamp()` throughout instead of jumping at breakpoints.

The spacing rhythm is loose and literal rather than a strict scale: 0.6rem inside the brand lockup, 1–1.25rem for nav and gutters, 1.5–2rem between blocks, and 3rem for split gaps and the footer.

## Elevation & Depth

The system is flat and uses tonal layering. Depth comes from stacking Morning Mist (page), Field Paper (raised band or card) and Deep Forest Ink (the emphatic panel). Separation inside a surface uses 1.5px Pressed Fern hairlines. There is exactly one shadow in the system, on the front hero phone, and it exists to lift that illustration off the stack.

### Shadow Vocabulary
- **Illustration lift** (`box-shadow: 0 30px 50px -30px rgba(23, 50, 43, 0.45)`): only on the front phone of the hero stack. The ink-tinted colour keeps it inside the palette.

### Named Rules
**The Flat Surface Rule.** Cards, panels, buttons and articles have no shadow, at rest or on hover. If something needs to stand out, change its tone (paper to ink), not its elevation.

## Shapes

The shapes are soft and pebble-round without being bubbly. Containers use large radii: Card (22px) for the empty state, Article (24px) for legal pages, and Panel (28px) for the contact panel and phone outlines. Actions are full pills. Small details step down to Tile (10px), Control (6px) and Focus (4px). Borders are rare, and when present they're 1.5px Pressed Fern hairlines or, for the empty state alone, a 2px dashed Sage Leaf outline that reads as "a space waiting to be filled". Illustrations are built from the same vocabulary: rounded bars, dots, a conic progress ring and rounded phone silhouettes.

## Components

### Buttons
Solid and certain: one style only.
- **Shape:** full pill (Pill radius).
- **Primary:** Deep Forest Ink fill, Field Paper text, label-strong type, 0.85rem × 1.4rem padding, no underline.
- **Hover / Focus:** hover deepens the fill to Forest Night. Focus shows the global 3px Signal Cobalt outline, offset 3px.
- **Secondary / Ghost:** none exist. Don't add an outlined or ghost button. Text links do that job.

### Links
- **Default:** Signal Cobalt, underlined with a 0.18em offset.
- **Hover:** the underline thickens to 2px. The colour doesn't change.
- **On ink:** the contact email is a large display-type link in Field Paper with a 2px Sage Leaf bottom border, which turns Pale Shoot on hover.

### Cards / Containers
- **Legal article:** a Field Paper surface with Article radius, fluid padding, and a maximum width of 48rem, on the Mist page.
- **Contact panel:** a Deep Forest Ink surface with Panel radius, Field Paper headline and Lichen Whisper body text. Inside it, focus outlines switch to Pale Shoot.
- **Empty state:** no fill, a 2px dashed Sage Leaf border, Card radius, and a 64px palette-drawn phone icon beside the text.
- **Shadow strategy:** none (see Elevation & Depth).

### Navigation
- **Header:** the brand lockup (30px logo plus "Sage Lab" in Bricolage 700 at 1.2rem) sits left, and the text nav sits right.
- **Links:** label type in Moss Shadow with no underline. Hover and `aria-current` turn them Deep Forest Ink with an underline.
- **Footer:** the same Moss Shadow label type. Links are underlined and the layout wraps on small screens.
- **Skip link:** an ink pill-ish tab (Control radius) that slides in at the top left on focus.

### Principles list
Stacked rows divided by 1.5px hairlines (top on every row, bottom on the last). Each row is a Title-type heading over Moss Shadow body text. There are no icons or numbers.

### Phone stack (signature)
Three abstract phones fanned from the bottom centre. The back one is Pale Shoot with a grid of tiles, rotated −11°. The middle one is a light green tint with list rows, rotated −4°. The front one is Field Paper with a title bar, conic ring and text bars, rotated 6° and given the single illustration shadow. They fan out over 900ms on load, but only under `prefers-reduced-motion: no-preference`. All of it is CSS and decorative (`aria-hidden`).

## Do's and Don'ts

### Do:
- **Do** keep every colour inside the green family (hue around 150–175), and use Signal Cobalt only for links and focus outlines.
- **Do** set headlines in Bricolage Grotesque with negative tracking and line-height of 1.05 or less, sized with `clamp()`.
- **Do** separate surfaces by tone (Mist, Paper, Ink) and divide inside them with 1.5px Pressed Fern hairlines.
- **Do** use large radii (22–28px) on containers and full pills on buttons.
- **Do** draw any new illustration from palette shapes (rounded bars, dots, rings, phone silhouettes) and mark it `aria-hidden`.
- **Do** keep a visible `:focus-visible` outline on every interactive element, in Signal Cobalt on light surfaces and Pale Shoot on ink.

### Don't:
- **Don't** add shadows to cards, buttons or panels. The front hero phone keeps the only one.
- **Don't** add a dark theme or `prefers-color-scheme` styles. The site is light-only by decision.
- **Don't** use stock photography, generic device mockups or fake app screenshots.
- **Don't** introduce a second accent hue, gradients behind text, or pure black or grey.
- **Don't** de-emphasise text with light weights or opacity. Use Moss Shadow (or Lichen Whisper on ink).
- **Don't** add ghost or outlined buttons. There is one solid button style, and links cover everything else.
- **Don't** add motion beyond the hero fan-out without gating it behind `prefers-reduced-motion: no-preference`.
