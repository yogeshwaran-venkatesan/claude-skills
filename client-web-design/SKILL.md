---
name: "client-web-design"
description: "ALWAYS use for any web design request: website, web page, landing page, homepage, mockup, redesign, site rebuild, UI or pitch site for a client — builds a custom, non-generic design and verifies it."
---

# Client Web Design (no AI slop)

> Apply this skill automatically to EVERY web design request (website, page, landing page, homepage, mockup, redesign, rebuild, pitch site) — the user does not need to name it.

Build client websites that look like a real agency made them: opinionated design, real copy, clean code, checked in a real browser before handover.

## Step 0 — Ask, never assume
Before writing any code, confirm (ask only for what is missing):
- Stack: plain HTML/CSS/JS, Angular, React/Next.js, or WordPress/Elementor.
- Business: name (exact spelling), industry, city, services/products, target customer.
- Real assets: logo, photos, project list, contact numbers, WhatsApp, address, Google Maps link, Google rating, social links.
- Languages (e.g. English + Tamil/Kannada) — never guess.
- Main goal of the site: calls, WhatsApp enquiries, quote requests, bookings, or online orders.
If assets are missing, use clearly marked TODO slots — never stock people photos or made-up facts.

## Step 1 — Design spec first (no components yet)
Write a short spec and get approval:
1. **Aesthetic direction** — commit to ONE: editorial, luxury, industrial, warm-local, brutalist, minimal-premium. One sentence on why it fits this business.
2. **Typography** — one distinctive display font + one clean body font. Fluid sizes with clamp() on a strict modular scale (e.g. 1.25). Never default Inter/Roboto/Arial as the display font.
3. **Colour (60-30-10)** — 60% base (e.g. warm off-white #F7F6F2 or charcoal #111214), 30% structural surface, 10% one strong brand accent. Define as CSS variables / design tokens.
4. **Grid & layout** — 12-col grid, at least one asymmetric/editorial split section, hairline 1px borders, generous whitespace.
5. **Page list + real copy** — headline and body copy for every section, written for this industry and city.

### Direction presets (starting points, adjust per client)
- **Jewellery / gold:** luxury-editorial; serif display (e.g. Cormorant, Instrument Serif); ivory + deep maroon/green + gold accent used sparingly; large product photography; gold-rate block with date/time; savings-scheme section; BIS hallmark trust strip.
- **Industrial / manufacturing / B2B:** industrial-precise; grotesk display (e.g. Space Grotesk, Archivo); charcoal + steel grey + one safety accent (orange/yellow); spec tables, project case studies (client, location, area, timeline), brochure download, detailed quote form.
- **Hotel / hospitality:** warm-editorial; room cards with real photos, rates/amenities, location & nearby attractions, booking/WhatsApp CTA.
- **Photography / creative:** minimal gallery-first; image-led asymmetric masonry, minimal chrome, strong typography for names/categories.

## Step 2 — Hard bans (AI clichés)
NEVER:
- Purple/indigo/blue-violet gradients, glassmorphism blobs, floating gradient orbs.
- Generic icons inside coloured circles in a 3-column centred feature grid.
- Placeholder copy: "Transform your workflow", "Empowering businesses", "Unlock your potential", "Elevate your experience", Lorem Ipsum, "Example Title".
- Stock photos of smiling people unrelated to the business.
- Fake stats, fake testimonials, or animated counters that can show "0+".
- Emoji as icons, centred everything, identical card heights everywhere.
- Links to "#" in the finished site.

## Step 3 — Build rules
- Components are small and composable (e.g. Card with Header/Body/Footer parts), not one giant prop-heavy component.
- Mobile-first; test widths 390px and 1440px.
- Images: real alt text, width/height set (no layout shift), lazy-load below the fold, WebP/AVIF where possible.
- Motion: subtle and purposeful (fade/slide on scroll, real hover states); respect prefers-reduced-motion.
- Accessibility: WCAG AA contrast, visible focus states, semantic headings (one H1 per page), descriptive link text (not "Know More" alone).
- Angular + TranslateModule: always generate i18n key files for every project language.
- If output will be long, propose a batch plan first and generate each batch fully — never truncate a file.

### Local business essentials (Indian SMB clients)
- Sticky WhatsApp button and click-to-call (tel:) link.
- Address + embedded Google Map + opening hours.
- Google rating/reviews (real, linked to the profile).
- Contact/quote form that actually sends (email and/or WhatsApp alert) with spam protection.
- SEO: page title = "Service in City | Brand"; meta description per page; LocalBusiness JSON-LD schema; Open Graph image; sitemap.xml; robots.txt.
- Privacy policy page; correct current copyright year.

## Step 4 — Verify in a real browser
Use Playwright (headless Chromium):
1. Screenshot every page at 1440px and 390px; look at the screenshots.
2. Check for horizontal overflow, overlapping text, broken images, tiny tap targets (<44px).
3. Check console errors and failed network requests.
4. Fix and re-screenshot until clean.

## Step 5 — Pre-handover checklist (must all pass)
- [ ] No Lorem Ipsum / "Example" / TODO text left visible.
- [ ] No href="#" or dead links; all social links go to real profiles.
- [ ] No admin/login links on public pages; no developer emails or internal paths in meta tags or source.
- [ ] Business name, client names and addresses spelled correctly and consistently.
- [ ] Counters, sliders, rate tickers and forms render real values and work.
- [ ] Every image has meaningful alt text; titles and meta descriptions are unique per page.
- [ ] Mobile and desktop screenshots reviewed.
- [ ] Lighthouse: Performance, Accessibility, SEO each 90+ (or explain why not).

End with a short summary: design direction chosen, pages built, checklist results, and anything still waiting on the client (photos, content, credentials).