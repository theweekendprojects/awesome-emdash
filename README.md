# Awesome EmDash [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of plugins, themes, and resources for [EmDash](https://emdashcms.com) — the Astro-native, Cloudflare-friendly CMS.

EmDash has two extension surfaces (auth providers and native/standard plugins) and a growing community shipping things on top of both. This list collects what's out there so you don't have to rebuild it.

Contributions welcome — see [Contributing](#contributing). Adding your own plugin is one PR.

## Contents

- [Official](#official)
- [Plugins](#plugins)
  - [Email & transactional delivery](#email--transactional-delivery)
  - [Auth](#auth)
  - [Commerce & payments](#commerce--payments)
  - [Events](#events)
  - [Analytics](#analytics)
  - [SEO & metadata](#seo--metadata)
  - [Content blocks & field widgets](#content-blocks--field-widgets)
  - [Content import & sync](#content-import--sync)
  - [Engagement](#engagement)
  - [Forms & contact](#forms--contact)
  - [Security & bot protection](#security--bot-protection)
  - [Privacy & consent](#privacy--consent)
  - [AI & agents](#ai--agents)
  - [Domain-specific](#domain-specific)
  - [Utility & ops](#utility--ops)
- [Themes & starters](#themes--starters)
- [Resources](#resources)
- [Contributing](#contributing)

## Official

- [EmDash](https://github.com/emdash-cms/emdash) — The CMS itself.
- [Documentation](https://docs.emdashcms.com) — Official docs (also available as an MCP server at `https://docs.emdashcms.com/mcp`).
- [Discussions](https://github.com/emdash-cms/emdash/discussions) — Feature requests, Q&A, and the "Show and tell" plugin showcase.

## Plugins

> Community-built unless noted. Not an endorsement — check each plugin's license, maintenance status, and requested permissions before installing.

### Email & transactional delivery

The busiest category — each implements EmDash's `email:deliver` / `email:provide` pipeline.

- [emdash-smtp](https://github.com/masonjames/emdash-smtp) — Full-parity SMTP + transactional email; the widely-used one. [`npm`](https://www.npmjs.com/package/emdash-smtp)
- [emdash-resend](https://github.com/bison-digital/emdash-resend) — Resend provider. [`npm`](https://www.npmjs.com/package/emdash-resend)
- [emdash-plugin-resend](https://github.com/maikunari/emdash-plugin-resend) — Resend provider (a separate implementation). [`npm`](https://www.npmjs.com/package/emdash-plugin-resend)
- [emdash-aws-ses](https://github.com/ab6162/emdash-aws-ses) — Amazon SES transport. [`npm`](https://www.npmjs.com/package/emdash-aws-ses)
- [emdash-plugin-postmark](https://github.com/drudge/emdash-plugin-postmark) — Postmark with delivery log, webhook tracking, sender pickers. [`npm`](https://www.npmjs.com/package/emdash-plugin-postmark)
- [emdash-plugin-anymail](https://github.com/nexed-tech/emdash-plugin-anymail) — One plugin, any HTTP provider (Resend, Maileroo, Mailgun, Postmark); no SMTP, just fetch. [`npm`](https://www.npmjs.com/package/emdash-plugin-anymail)
- [compass-mail](https://github.com/ecropolis/emdash-plugin-compass-mail) — SendGrid or Resend transport. [`npm`](https://www.npmjs.com/package/@ecropolis/emdash-plugin-compass-mail)
- [forward-email](https://github.com/numoteq/emdash-plugins) — Forward Email transport. [`npm`](https://www.npmjs.com/package/@numoteq/emdash-plugin-forward-email)
- [lettermint](https://github.com/jdevalk/emdash-plugin-lettermint) — Lettermint provider. [`npm`](https://www.npmjs.com/package/@jdevalk/emdash-plugin-lettermint)
- [larksuite-email](https://github.com/MAV3Ndev/emdash-larksuite-email) — LarkSuite Mail transport. [`npm`](https://www.npmjs.com/package/@mav3ndev/emdash-larksuite-email)
- [jetemail](https://github.com/jetemail/jetemail-emdash) — JetEmail provider. [`npm`](https://www.npmjs.com/package/@jetemail/emdash)
- [@dullaz/email](https://github.com/Dullaz/emdash-email) — Email transport with a pluggable provider abstraction (Cloudflare first). [`npm`](https://www.npmjs.com/package/@dullaz/email)

### Auth

- [emdash-better-auth](https://github.com/theweekendprojects/emdash-better-auth) — Email/password + social (Google, GitHub) auth via [Better Auth](https://better-auth.com), with prebuilt sign-in/sign-up pages, email verification, and an admin settings page. [`npm`](https://www.npmjs.com/package/emdash-better-auth)

### Commerce & payments

- [DashCommerce](https://github.com/emdashCommerce/dashcommerce) — Full WooCommerce-equivalent commerce plugin. [`npm`](https://www.npmjs.com/package/@dashcommerce/core)
- [@dullaz/commerce](https://github.com/Dullaz/emdash-commerce) — Products, inventory, orders, checkout, pluggable payment providers. [`npm`](https://www.npmjs.com/package/@dullaz/commerce)
- [emdash-mika](https://github.com/bnomei/emdash-mika) — Agent-ready commerce primitives for content-led storefronts. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-mika)
- [Tender](https://github.com/foreztgump/tender) — Payments layer with Stripe & Square providers, webhooks, refunds, subscriptions (`@tenderpay/*`). [`npm`](https://www.npmjs.com/package/@tenderpay/core)
- [DinkusKit](https://github.com/dinkuskit) — A kit of commerce plugins (commerce, bundles, coupons, inventory, Stripe-first payments) plus a section-blocks plugin and Astro store/services/marketing templates. Under construction; packages will ship as `@dinkuskit/*`.

### Events

- [Dateline](https://github.com/foreztgump/dateline-events-plugin) — Events, venues, organizers, calendar feeds (JSON + iCal), schema.org JSON-LD, importer, and free RSVP (`@dateline/*`). [`npm`](https://www.npmjs.com/package/@dateline/core)

### Analytics

- [@plukio/emdash-analytics](https://www.npmjs.com/package/@plukio/emdash-analytics) — First-party analytics events routed to PostHog and GA4. [`npm`](https://www.npmjs.com/package/@plukio/emdash-analytics)
- [em-analytics-hub](https://github.com/facuzarate04/em-analytics-hub) — Portable, privacy-first analytics hub (pageviews, UTM, custom events). [`npm`](https://www.npmjs.com/package/em-analytics-hub)
- [em-content-insights](https://github.com/facuzarate04/em-content-insights) — Privacy-first per-post analytics (views, read rate, time on page, referrers). [`npm`](https://www.npmjs.com/package/em-content-insights)

### SEO & metadata

- [aexeo-emdash](https://github.com/schiste/Aexeo/tree/main/packages/aexeo-emdash) — Aexeo SEO/GEO content evaluator (WASM, Cloudflare). [`npm`](https://www.npmjs.com/package/@aeptus/aexeo-emdash)
- [emdash-taki](https://github.com/bnomei/emdash-taki) — Waterfall head renderer + dynamic head/metadata helpers (OpenGraph, JSON-LD, Turnstile). [`npm`](https://www.npmjs.com/package/@bnomei/emdash-taki)
- [emdash-plugin-seo](https://github.com/jdevalk/emdash-plugin-seo) — Comprehensive SEO via the `page:metadata` hook: meta tags, Open Graph, Twitter Cards, canonical URLs, JSON-LD schema graph, hreflang, breadcrumbs, llms.txt, IndexNow, and a fuzzy-redirects admin tool.
- [emdash-auto-meta](https://github.com/marcusbellamyshaw-cell/emdash-auto-meta) — Lets AI agents assign taxonomy terms and set SEO metadata via `content:afterSave`. [`npm`](https://www.npmjs.com/package/emdash-auto-meta)

### Content blocks & field widgets

- [emdash-plugin-puck](https://github.com/markoinla/emdash-plugin-puck) — Puck visual editor as a field widget — edit a JSON field as a page layout. [`npm`](https://www.npmjs.com/package/emdash-plugin-puck)
- [emdash-plugin-media-gallery](https://github.com/gg3orgiev/emdash-plugin-media-gallery) — Multi-image gallery field: ordered arrays, per-item metadata, primary flag, media search. [`npm`](https://www.npmjs.com/package/emdash-plugin-media-gallery)
- [featured-image-studio](https://github.com/devondragon/emdash-plugins) — Featured-image picker with Unsplash stock search. [`npm`](https://www.npmjs.com/package/@devondragon/emdash-plugin-featured-image-studio)
- [emdash-plugin-highlightjs](https://github.com/adrianoamalfi/emdash-plugin-highlightjs) — Syntax highlighting via Highlight.js — themes, dark/light, copy button. [`npm`](https://www.npmjs.com/package/emdash-plugin-highlightjs)
- [emdash-plugin-modern-images](https://github.com/adrianoamalfi/emdash-plugin-modern-images) — Converts images to WebP/AVIF with responsive srcset and LCP preload. [`npm`](https://www.npmjs.com/package/emdash-plugin-modern-images)
- [tabler-icons](https://github.com/wenke-studio/emdash-plugin-tabler-icons) — Tabler Icons Portable Text block. [`npm`](https://www.npmjs.com/package/@wenke.studio/emdash-plugin-tabler-icons)
- [@plugdash/callout](https://github.com/plugdash/plugdash) — Callout / admonition blocks. [`npm`](https://www.npmjs.com/package/@plugdash/callout)
- [emdash-plugin-stl-viewer](https://github.com/ebootheee/emdash-plugin-stl-viewer) — Embed interactive 3D previews of STL / 3MF files in Portable Text. [`npm`](https://www.npmjs.com/package/emdash-plugin-stl-viewer)
- [members-block](https://www.npmjs.com/package/@han-x/members-block) — Member-card grid block with per-member accent colors + Astro renderer. [`npm`](https://www.npmjs.com/package/@han-x/members-block)
- [emdash-blocks](https://github.com/bnomei/emdash-blocks) — JSON block-list field widget with normalized block props and visibility state. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-blocks)
- [emdash-fields](https://github.com/bnomei/emdash-fields) — Structured JSON fields (object, structure, link, choices editors). [`npm`](https://www.npmjs.com/package/@bnomei/emdash-fields)
- [emdash-bento](https://github.com/bnomei/emdash-bento) — Bento grid field widget for JSON fields. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-bento)

### Content import & sync

- [@emdash-notion/sync](https://github.com/kjfsm/emdash-notion) — Sync Notion pages into EmDash as Portable Text via webhooks (ships `@emdash-notion/blocks` for Notion-style rendering). [`npm`](https://www.npmjs.com/package/@emdash-notion/sync)
- [emdash-rss-aggregator](https://github.com/emdash-cms/emdash-rss-aggregator) — RSS/Atom feed aggregator — import feed items as first-class content. [`npm`](https://www.npmjs.com/package/@dawod/emdash-rss-aggregator)
- [video-to-recipe](https://github.com/peristyle-io/video-to-recipe) — Import TikTok / Instagram posts as recipe drafts, built out with Gemini. [`npm`](https://www.npmjs.com/package/@peristyle/emdash-plugin-video-to-recipe)

### Engagement

- [emdash-social-sharing](https://github.com/masonjames/emdash-social-sharing) — Privacy-light social sharing controls for content and themes. [`npm`](https://www.npmjs.com/package/emdash-social-sharing)
- [social-share](https://github.com/drateberry/emdash-plugin-social-share) — Auto-post published posts to Bluesky, Mastodon, and X. [`npm`](https://www.npmjs.com/package/@drateberry/emdash-plugin-social-share)
- [@plugdash/heartpost](https://github.com/plugdash/plugdash) — Like button — readers heart your content. [`npm`](https://www.npmjs.com/package/@plugdash/heartpost)
- [@plugdash/sharepost](https://github.com/plugdash/plugdash) — Share buttons (Twitter/X, LinkedIn, WhatsApp, Bluesky, email) with no heavy JS. [`npm`](https://www.npmjs.com/package/@plugdash/sharepost)
- [@plugdash/engage](https://github.com/plugdash/plugdash) — Heart + share + copy engagement bundle. [`npm`](https://www.npmjs.com/package/@plugdash/engage)
- [emdash-rating](https://www.npmjs.com/package/emdash-rating) — 1–5 star ratings with live averages and an admin dashboard. [`npm`](https://www.npmjs.com/package/emdash-rating)

### Forms & contact

- [compass-forms](https://github.com/ecropolis/emdash-plugin-compass-forms) — Editor-composable form block with stored submissions, email notify, spam basics. [`npm`](https://www.npmjs.com/package/@ecropolis/emdash-plugin-compass-forms)
- [contact-inbox](https://github.com/MAV3Ndev/emdash-contact-inbox) — Contact form inbox with Turnstile. [`npm`](https://www.npmjs.com/package/@mav3ndev/emdash-contact-inbox)
- [emdash-plugin-contact-form](https://www.npmjs.com/package/emdash-plugin-contact-form) — Contact-form submissions store — public submit endpoint, Block Kit admin, dashboard widget, no build step. [`npm`](https://www.npmjs.com/package/emdash-plugin-contact-form)

### Security & bot protection

- [@dullaz/captcha](https://github.com/Dullaz/emdash-captcha) — CAPTCHA (Cloudflare Turnstile first) with pluggable providers; server-side token verification. [`npm`](https://www.npmjs.com/package/@dullaz/captcha)
- [RankShield](https://github.com/seo-elite-agency/rankshield-emdash) — Behavioral threat defense based on hardware fingerprinting rather than IP blocking. [`npm`](https://www.npmjs.com/package/@rankshield/emdash-security)

### Privacy & consent

- [emdash-plugin-cookie-consent](https://github.com/adrianoamalfi/emdash-plugin-cookie-consent) — Customizable cookie consent banner with category opt-in, theming, admin panel. [`npm`](https://www.npmjs.com/package/emdash-plugin-cookie-consent)

### AI & agents

- [InjectAI](https://github.com/muzammildafedar/emdash-injectai) — AI chatbot powered by your own content — RAG chat, file uploads, quiz/module generation. [`npm`](https://www.npmjs.com/package/@injectailabs/emdash-injectai)
- [emdash-akari](https://github.com/bnomei/emdash-akari) — Agent-focused discovery CLI — resolve content targets and query nested JSON beyond MCP search. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-akari)

### Domain-specific

- [recipes](https://www.npmjs.com/package/@peristyle/emdash-plugin-recipes) — Recipe fields, components, and timers for food blogs. [`npm`](https://www.npmjs.com/package/@peristyle/emdash-plugin-recipes)
- [grocery-cart-widget](https://www.npmjs.com/package/@peristyle/grocery-cart-widget) — Chat, recipe search, one-click ingredient ordering (Kroger/Walmart) for food blogs. [`npm`](https://www.npmjs.com/package/@peristyle/grocery-cart-widget)
- [bible](https://github.com/midvash/bible-emdash-plugin) — Auto-detect Bible references and render verse tooltips on hover. [`npm`](https://www.npmjs.com/package/@midvash/emdash-plugin-bible)
- [conference-badge-generator](https://github.com/kgittyup/conference-badge-generator) — Public `/badge` page where visitors build a shareable 1080×1080 conference badge with in-browser AI. [`npm`](https://www.npmjs.com/package/conference-badge-generator)
- [star-lite-docs](https://github.com/gruntlord5/star-lite-docs) — Starlight-style documentation theme (Astro integration + plugin in one). [`npm`](https://www.npmjs.com/package/star-lite-docs)

### Utility & ops

- [emdash-actions](https://github.com/bnomei/emdash-actions) — Native action surface for provider plugins. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-actions)
- [action-maintenance](https://github.com/bnomei/emdash-action-maintenance) — Maintenance-mode action provider. [`npm`](https://www.npmjs.com/package/@bnomei/emdash-action-maintenance)
- [@plugdash/autobuild](https://github.com/plugdash/plugdash) — Fires a Cloudflare Pages / Netlify / Vercel build hook on every publish. [`npm`](https://www.npmjs.com/package/@plugdash/autobuild)
- [@plugdash/shortlink](https://github.com/plugdash/plugdash) — Short URLs created on publish. [`npm`](https://www.npmjs.com/package/@plugdash/shortlink)
- [@plugdash/tocgen](https://github.com/plugdash/plugdash) — Auto-generated table of contents. [`npm`](https://www.npmjs.com/package/@plugdash/tocgen)
- [@plugdash/readtime](https://github.com/plugdash/plugdash) — Estimated reading time + word count. [`npm`](https://www.npmjs.com/package/@plugdash/readtime)
- [404-viewer](https://github.com/devondragon/emdash-plugins) — Admin viewer for the built-in 404 log table. [`npm`](https://www.npmjs.com/package/@devondragon/emdash-plugin-404-viewer)
- [emdash-plugin-slack](https://www.npmjs.com/package/emdash-plugin-slack) — Slack notifications when content is published. [`npm`](https://www.npmjs.com/package/emdash-plugin-slack)

## Themes & starters

- [Astroplate (emdash branch)](https://github.com/zeon-studio/astroplate/tree/emdash) — Astro + TailwindCSS + TypeScript starter template powered by EmDash, by Zeon Studio.

## Resources

- [EmDash docs](https://docs.emdashcms.com) — Official documentation.
- [Building an EmDash plugin](https://docs.emdashcms.com) — See the docs' plugin guide for hooks, storage, admin UI, API routes, and Portable Text block types.
- Find every published plugin on npm by the [`emdash-plugin` keyword](https://www.npmjs.com/search?q=keywords:emdash-plugin).

## Contributing

Found a plugin that's missing, or shipped one yourself? [Open a pull request](https://github.com/theweekendprojects/awesome-emdash/pulls) — see [CONTRIBUTING.md](CONTRIBUTING.md) for the one-line format and where it goes. Corrections and de-duplications are just as welcome.

---

<sub>Maintained by [The Weekend Projects](https://theweekendprojects.com). This is a community list and is not affiliated with or endorsed by the EmDash team.</sub>
