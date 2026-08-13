# Headfirst Mobile Welding — demo site

Single-page, self-contained demo built for Wilson Innovations outreach.

- **Business:** Headfirst Mobile Welding — owner-run mobile welding &amp; metal fabrication, Bradenton, FL
- **Phone:** (941) 702-4727
- **Address:** 1315 27th Ave W B#102, Bradenton, FL 34205
- **Rating shown:** 5.0 stars, 29 Google reviews (≥4.4, shown)
- **Hours:** GBP lists "Open 24 hours" 7 days — NOT credible as a literal 24-hour storefront for an owner-run mobile welder, so presented honestly as **"mobile by appointment, 7 days"** with **"same-day when the schedule allows."** No literal 24/7 claim made; no openingHoursSpecification in the JSON-LD (avoids asserting fixed hours).
- **Owner referenced:** Cricket / Crick (one review also names him "Eric"). Kept out of body copy per the no-owner-personality-section rule; his name appears only inside verbatim customer pull-quotes ("Cricket is the man", "trust Crick and the team").
- **Tier:** 1 (Clean Slate), industrial recolor per manifest palette hint
- **Fonts:** Big Shoulders Display (display, industrial) + Public Sans (body, proportional) — approved proven pair, both Google Fonts
- **Palette:** graphite near-black (#16181b) / molten-orange spark (#ee5a13, amber #ff9247 on dark) / raw steel gray (#eef0f3 bg, #878e98 steel)
- **Live URL:** https://wilsoninnovations.net/headfirst-mobile-welding/

## Positioning — MOBILE-FORWARD (differentiation)
This is the **second welding demo** built. To stay distinct from the two existing welding sites —
**blackhawk-welding** (fixed shop, custom fabrication lane) and **kingston-auto-welding** (auto-repair +
welding lane) — Headfirst leans hard into **"mobile / we come to you."** Hero, the first feature band, and
the services all frame **on-site mobile welding** as the edge (the rig comes to your driveway, jobsite,
marina or roadside), with **trailer &amp; hitch repair**, **custom fabrication**, and **welding on all
materials** alongside. Every service and claim is grounded in the real review texts (comes-to-you /
go-to-them convenience + all materials, car-trailer save, custom-fabrication go-to, muffler weld + paint in
~1 hour, met-at-shop 1-hour repair at a fair price).

## Images (self-hosted in assets/, Unsplash sources — record for cross-wave dedup)
- `assets/hero.jpg` + `assets/og-preview.jpg` ← **photo-1508188609340-e8068b599193** (welder in helmet + overalls striking a bright arc on steel at an OUTDOOR jobsite against a sunset sky — on-site/mobile hero &amp; DM link-preview bait; og is a 1200×630 crop)
- `assets/fabrication.jpg` ← **photo-1714504904786-b6732390b206** (big fan of ORANGE sparks fountaining down as a worker cuts/welds square steel tube on a rack — on-palette money shot for the "we bring the welder to you" mobile band)
- `assets/repair.jpg` ← **photo-1455165814004-1126a7199f9b** (close-up welder joining steel, bright burst of sparks — dark "trailer, hitch &amp; repair welds" band)
- `assets/craft.jpg` ← **photo-1683470156390-703e9313dab6** (detail of a gloved welder running a bright MIG weld along a joint, blue smoke — "fast, fair, done right" craft band)

**Dedup / verification:** All four Unsplash IDs were HTTP-200-verified and dedup-checked IMMEDIATELY before
download via a global grep over `websites/*/index.html`, `websites/*/README.md`, and `templates/*/`
(1,937 unique IDs in use at build time — none of these four among them). The 8 prior welding IDs used by
**blackhawk-welding** (1466779561253-0a08336ba2ab, 1564182998523-6923112e7d6b, 1698664683348-f9f35b809821,
1716469801932-3b1b5494615c) and **kingston-auto-welding** (1744735973756-b2efa8be24c8,
1647586028042-1de4d4a935e6, 1610742805112-20134ceb40e8, 1745448797901-2a4c9d9af1c1) were all confirmed
present in the exclude list and deliberately avoided — these are different welding/fabrication shots.
Two initial candidates (photo-1526634140919-468dc3ae3870, photo-1558611997-dd5b20e08c71) hit collisions in
the grep and were dropped. All re-encoded with Pillow to ≤350 KB (hero 280 KB, fabrication 225 KB,
repair 203 KB, craft 192 KB, og 141 KB). Every image was visually inspected against its alt before use.

## Notes / facts verified
- Reviews are real Google reviews, attributed first name + last initial: Edward Y. (car-trailer save,
  "Cricket is the man", fair price), Zach F. ("genius and a master craftsman... go-to for custom fabrication"),
  and a peer-business endorsement from **Cornerstone Mobile Welding** ("know everything about welding...
  come to you or you can go to them... work with all materials"). Feature-band pull-quotes use Cornerstone
  (mobile/come-to-you), Edward Y. (car trailer), and a verbatim customer quote (muffler welded + painted to
  protect the welds in ~1 hour, "great guy with a great attitude"). The one review with an unusual display
  handle was used only for its verbatim quote content and attributed as "Google review", not by the handle.
- No founding year, email, license numbers, or pricing invented. No contact form. No fixed bottom mobile call
  bar (header call CTA is the persistent contact affordance; icon-only ≤600px, flush right; brand ≤2 lines,
  not clipped).
- JSON-LD `WeldingService` with real phone, address, Bradenton/Manatee County areaServed, and 5.0/29
  aggregateRating. No openingHoursSpecification (mobile by appointment — no fixed/24-hour claim).

## Verification
- puppeteer-core + system Edge, true 390 px and 1440 px full pages, plus 1440×900, 1366×768 and 390×844
  no-scroll fold shots.
- Zero horizontal overflow at 390 / 1366 / 1440 (scrollWidth == clientWidth at every width). Hero full stack
  (eyebrow → headline → sub → CTA pair → glass trust chip) visible with no scroll at 1440×900 AND 1366×768,
  and in the first mobile viewport at 390.
- Feature-band images confirmed rendering + matching alts (captured with lazy-load forced).

## Go-live checklist
1. Remove `<meta name="robots" content="noindex">` (see the DEMO comment at the top of `index.html`).
2. Confirm the owner's preferred name/spelling (Cricket / Crick / Eric) and how they want mobile-vs-shop
   availability described before publishing.
3. Swap the placeholder Unsplash photos for Headfirst's own rig / on-site / finished-job photos when available.
4. Point a domain at GitHub Pages.

_Website by Wilson Innovations — https://wilsoninnovations.net_
