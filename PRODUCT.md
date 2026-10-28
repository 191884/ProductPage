# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Two audiences, weighted equally:

- **Reviewers and partners checking legitimacy.** These are Google Play and App Store review, ad networks such as AdMob, and prospective partners. They visit to confirm that Sage Lab is a real, reachable, compliant developer: a registered business, a privacy policy and terms at stable URLs, and a working contact address.
- **People who use or might install Sage Lab apps.** These are everyday Android and iOS users. They come from a store listing or an in-app link to decide whether to trust the developer, read the privacy policy or terms, or send a question or privacy request.

The legitimacy job dominates today because no apps are live. As apps launch, the site also becomes the place to find and install them.

## Product Purpose

sagelab.in is the developer website for Sage Lab, an independent mobile app studio that designs, builds and publishes its own Android and iOS apps. It exists to give the store listings and apps a trustworthy home: who the studio is, how it treats user data and money, the legal pages the stores require, and how to reach a person. It succeeds when a reviewer can verify the developer quickly and a user leaves confident enough to install, or gets the answer or contact they came for.

## Positioning

Sage Lab is a general studio. It builds simple, reliable everyday-utility apps in any category where a well-made app can solve an everyday problem, with no single category named as its focus. Its claims are concrete commitments, not superlatives: the apps are fast on budget phones, user content stays on the device, and ads and subscriptions are disclosed plainly, with cancelling one tap away in the app store.

## Operating Context

- Visitors usually arrive from a Play Store or App Store listing, an in-app privacy or terms link, or a reviewer's checklist, and often on a phone.
- `https://sagelab.in/privacy.html` is the privacy policy URL registered in Play Console and must stay at that path.
- Hosted on GitHub Pages from `main`, with the custom domain in `CNAME`.
- The apps use these third-party services, which the privacy policy discloses: Google AdMob, Firebase (Analytics, Crashlytics, Remote Config), AppMetrica, Adapty, and Google Play / App Store billing.

## Capabilities and Constraints

- Static HTML and one stylesheet, with no build step and no JavaScript. Pages: home (about, apps, contact), privacy policy, terms of use, 404.
- Links stay relative so the site works under a subpath. The header, footer and `<head>` are duplicated on every page.
- Contact is email only (`aman@sagelab.in`), with a promised reply within two working days. There is no contact form, account or newsletter system.
- Business details: a sole proprietorship in Bhiwani, Haryana, India, registered as an MSME (Udyam No. UDYAM-HR-02-0056471).
- Light theme only. Dark mode is out by decision.
- Undecided: how app listings will be presented once apps ship (they replace the placeholder in the Apps section), and any category grouping for them.

## Brand Commitments

- Name: **Sage Lab**. Logo: `assets/logo.svg` (the favicon and header mark). `assets/email-logo.png` is for email signatures.
- Voice: calm, plain and first-person plural ("we"). Honest about ads, data collection and subscriptions. No hype, superlatives or buzzwords.
- The individual behind the studio is not named on the site. Don't add a founder name or bio unless the user confirms it.
- No reference sites have been chosen to aim toward or avoid.

## Evidence on Hand

- Real: the MSME/Udyam registration, the Bhiwani location, the contact email, and the privacy policy and terms (last updated 27 October 2026).
- Absent: **no apps are live yet.** Don't invent app names, screenshots, store badges linking to real listings, ratings, download counts, testimonials, press, partners or user numbers. The Apps section stays an honest "in development" placeholder until real listings exist.

## Product Principles

1. **Verifiable over impressive.** Every claim is something a reviewer or user could check, such as registration, policy or contact. Trust comes from specifics, not polish alone.
2. **Plain about data and money.** Any surface that mentions ads, analytics, purchases or subscriptions says so directly and matches the privacy policy.
3. **Stable, required pages come first.** The privacy policy and terms URLs, their accuracy and their "last updated" dates matter more than any marketing surface.
4. **Honest about stage.** The site reflects what exists today and grows as apps launch, never ahead of them.
5. **Light on the visitor's phone.** It should be fast and readable on budget devices, consistent with the promise made for the apps.
