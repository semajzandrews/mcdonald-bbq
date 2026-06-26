# RECON — McDonald BBQ

Slug: `mcdonald-bbq`
Stage: REVIEW (no deploy). Single self-contained `index.html`.

## Verified business facts

| Field | Value | Source |
|---|---|---|
| Name | McDonald BBQ (signage also reads "McDonald's Barbeque") | Yelp, NetWaiter, Restaurantji, Tripadvisor |
| Address | 5 Main St, City of Orange, NJ 07050 | Yelp, NetWaiter, businessyab |
| Phone | (973) 266-9528 | NetWaiter, Yellowpages (tel:+19732669528) |
| Hours | Mon–Sat 11 AM to 11 PM; Sun 11 AM to 6 PM | NetWaiter, Yelp, Yahoo Local (all agree) |
| Payment | Cash only, no credit cards, no alcohol | NetWaiter ("doesn't accept credit cards or serve alcohol") |
| Service | Takeout (delivery/catering not offered) | NetWaiter |
| Rating | 3.6 Google over 512 reviews (per assigned facts) | facts kit |
| PIN | 669528 (last 6 of phone) | cluster facts |

### IMPORTANT category correction
The assigned kit labeled this "Caribbean / jerk BBQ restaurant." Research across Yelp,
Restaurantji, Tripadvisor and NetWaiter shows McDonald BBQ is actually a **Southern soul-food
barbecue institution**, not a jerk house. Verified menu signals:
- Beef and pork **ribs**, chopped BBQ, **pulled pork**
- **Smothered pork chops** and smothered chicken
- **Fried chicken**, **turkey wings**
- Sides: **collard greens, mac and cheese, candied yams, mashed potatoes, black-eye peas,
  sweet potato pie, cornbread**

The build honors the REAL business (a Black-owned Southern smokehouse / soul-food spot on lower
Main Street) rather than inventing a Caribbean jerk identity. The assigned art-direction palette
(ember + island green + charcoal) and the assigned signature (heat meter + hero smoke) suit a
smokehouse perfectly, so they were kept. The lone nod to the neighborhood's island palate is the
optional "Drag It Through Hot" house-hot-sauce option, written as a real option, not a fake jerk dish.

### Soft-rating handling (per facts note)
Rating is 3.6 but volume is very high (512). Instructed to SOFT-PEDAL the star number and lean
into the crowd/heritage. So: **no star count, no rating number, no fabricated review quotes.**
The single "voice" line is an honest neighborhood-sentiment line attributed "From the neighbors on
Main Street," not a star-rated testimonial. Lead is the smoke, the pit, and the line out the door.

## Art direction (assigned kit honored)
- Accent ember `#D6492B`, island green `#1F7A3D`, charcoal base `#140D0A`, gold `#E2A347` highlight, ash/cream text.
- Display: **Tanker** (Fontshare) for all headings — chunky, smoky, condensed personality.
- Body: **General Sans** (Fontshare).
- Mood: Caribbean/Southern smoke-house, fire-lit food on charcoal, bold bands. Generous whitespace,
  warm dark surfaces, ember micro-glows.
- `<html lang="en">` — verified English-primary soul-food spot (not Spanish-first); copy is plain,
  human, neighborhood-true.

## Signature interaction (assigned: heat-meter + hero smoke drift)
1. **Heat meter** on every menu dish — a track that fills (mild → scotch bonnet) with an
   ember gradient when the card scrolls into view; the 100% "Drag It Through Hot" bar gets a
   live pulsing ember glow at its leading edge. Values: Ribs 58, Pulled Pork 32, Chops 22,
   Turkey Wings 50, Fried Chicken 30, Hot 100.
2. **Hero smoke drift** — a lightweight canvas of rising translucent smoke puffs (screen blend,
   `prefers-reduced-motion` aware, pauses on tab hide) drifting behind the rib hero.

## Arsenal pieces fired
- Fontshare type pairing (Tanker display + General Sans body) — agency-tier, restyled to brand.
- Canvas particle technique (Magic UI "meteor/particles" lineage) re-implemented bespoke as
  rising smoke, branded ash color, blended to the hero only.
- Marquee strip (Magic UI marquee technique) restyled as an ember "menu ticker" band, JS-duplicated for a seamless loop.
- Scroll-reveal via IntersectionObserver (motion-primitives in-view technique), bespoke easing.
- Google **keyless Maps embed (Ramos pattern)**: `https://www.google.com/maps?q=5+Main+St,+City+of+Orange,+NJ+07050&z=16&output=embed`,
  with a flat low-opacity brand overlay (no CSS filter on the iframe). Verified blank-in-preview is the
  documented sandbox artifact; iframe element/src verified correct for real-browser render.
- Live **Open now / Closed** pill computed in `America/New_York` via `Intl.DateTimeFormat`, with
  graceful fallback, plus today's hours row auto-highlighted in gold.

## Hard rules check
- [x] Real per-brand nav (flame mark + The Pit / The Plate / Find Us / Hours + persistent call pill).
      Mobile collapses the call control to a single 46px phone icon; verified nothing scrolls past 375px
      (docW === 375, body overflow-x hidden, hero + strip clip at 375).
- [x] Footer: name, real address, real phone, 12-hour hours, call CTA, and a brand-styled
      "Built by bysemaj.com" credit linking https://bysemaj.com (ember spark, not a pasted block).
- [x] 12-hour time everywhere ("11 AM to 11 PM", "11 AM to 6 PM"). No 24-hour anywhere (verified).
- [x] No em dashes in any copy (verified 0 in file, including `<title>`).
- [x] Imagery: 11 images, every one unique (verified no duplicate base URL). Category reads instantly
      (ribs hero, smoked rib meat, chopped pork, pork chop, turkey/saucy wings, fried chicken on banana
      leaf, chili peppers for heat, collards, mac and cheese, loaded plate banner). Fried-chicken-on-
      banana-leaf chosen to read true to a Black + Caribbean clientele. All slugs load-tested 200 OK.
- [x] Keyless Google Maps embed (Ramos pattern), brand-tinted, taller portrait min-height on mobile.
- [x] Mobile-first flawless at 375px AND strong desktop; real smooth scroll (CSS + anchor), no
      scroll-snap, no autoplay-video pileups.
- [x] Socials: none shown (no verified exact-business handle found — omitted per rule 8).
- [x] Signature implemented = assigned heat-meter + hero smoke (NOT a horizontal-scroll section).

## Images used (Unsplash slugs — all unique, all load-verified)
- Hero: `photo-1529193591184-b1d58069ecdd` (rack of ribs)
- Story: `photo-1544025162-d76694265947` (pit/grill), `photo-1432139509613-5c4255815697` (collard greens),
  `photo-1604908176997-125f25cc6f3d` (baked mac and cheese)
- Menu: `photo-1558030006-450675393462` (rib meat), `photo-1594041680534-e8c8cdebd659` (chopped pork),
  `photo-1432139555190-58524dae6a55` (pork chop), `photo-1567620832903-9fc6debc209f` (saucy wings),
  `photo-1569058242253-92a9c755a0ec` (fried chicken on banana leaf), `photo-1526346698789-22fd84314424` (hot chili peppers)
- Banner: `photo-1555939594-58d7cb561ad1` (loaded plate)

Note for go-live: swap stock for McDonald BBQ's real food photos before publishing (Arsenal doctrine 9).

## Sources
- Yelp: https://www.yelp.com/biz/mcdonalds-barbeque-orange
- NetWaiter: https://mcdonaldsbarbeque.netwaiter.com/orange/about/
- Restaurantji: https://www.restaurantji.com/nj/city-of-orange/mcdonald-bbq-/
- Tripadvisor: https://www.tripadvisor.com/Restaurant_Review-g46707-d5019024-Reviews-McDonald_s_BBQ-Orange_New_Jersey.html
- businessyab: https://www.businessyab.com/explore/.../5/mcdonald_bbq_58066
