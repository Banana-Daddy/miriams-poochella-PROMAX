# Miriam's Poochella — PRO-MAX (Vintage Atomic Poster)

## Brand Synopsis

Miriam's Poochella is an award-winning luxury dog grooming salon in Palm Springs, CA, owned by **Miriam Lenz** — originally from **Zurich, Switzerland**, formally trained in **fashion and interior design** before transitioning into grooming. **14 years grooming**, opened her own salon on South Palm Canyon Drive in **2016**, **6 employees**, by-appointment-only (no kennel waits). **6-time titled "Best Groomer in the Coachella Valley"**, **3 professional grooming awards**, 4.5★ across ~90+ reviews.

This PRO-MAX direction reframes the brand as a **mid-century Palm Springs atomic-age dog spa** — like a 1962 cocktail-party scene but every party guest is a stylized cute dog. Hot-pink-forward palette (Miriam likes pink), Shag (Josh Agle) flat-vector illustration aesthetic, atomic starbursts, kidney pools, butterfly-roof MCM architecture. The brand's existing logo (fluffy white Maltese mascot with eyelashes) becomes the recurring character across the illustrations.

## Design Decisions

### Direction: The Atomic Spa — Poochella After-Hours

- **Mood**: Confident, chic, mid-century glamour. Spoiled pets. Hot pink everything. Award-winning craft.
- **Style intelligence source**: `ui-ux-pro-max` skill (provided base pink/lavender luxury palette + Abril Fatface display recommendation) combined with original Shag/Atomic Lounge direction.
- **Fonts**:
  - **Display**: Abril Fatface (Google Fonts) — vintage poster serif, high-impact
  - **Body**: Cabin (Google Fonts) — mid-century geometric sans
  - **Accent**: Bowlby One SC (Google Fonts) — chunky atomic poster for occasional accents
  - [Google Fonts share](https://fonts.google.com/share?selection.family=Abril+Fatface|Bowlby+One+SC|Cabin:wght@400;500;600;700)
- **Colors** (strict 6-color atomic pink palette):
  - `--pink-3: #FFE0EC` — Powder Pink (canvas)
  - `--pink-2: #FBB6CE` — Bubblegum (secondary)
  - `--pink: #FF4D8C` — Cabana Pink (primary)
  - `--teal: #5BA3A3` — Pool Teal (accent)
  - `--mustard: #E8B946` — Sun Mustard (warm accent)
  - `--plum: #3D1830` — Plum Ink (text/borders)
  - + supporting `--bone: #F5EDE4` for warm section backgrounds
- **Layout style**: Geometric rectangular panels with hard 3px plum borders + 6-8px offset color-block drop shadows (cabana pink, mustard, teal). Atomic starbursts as ornaments. Color-blocked service cards alternating bubblegum / mustard / pool teal. Atomic pattern wallpaper for the "House Rule" section background.
- **Signature element**: The **full-bleed Shag-style hero illustration** — fluffy white Maltese on a hot-pink chaise beside a pink kidney pool at a Palm Springs MCM house — anchors the entire design. Plus 5 supporting illustrations (Miriam portrait, 3 service cards, VIP banner, salon exterior, atomic pattern).
- **Anti-patterns avoided**:
  1. Neon / synthwave aesthetics — palette stays warm, not electric (per skill recommendation)
  2. Modern soft UI / neumorphism — we use hard borders + flat color blocks for vintage-poster confidence
  3. Centered-everything SaaS layouts — every section has asymmetric tension (offset shadows, alternating card colors)
- **Logos used (Logo Search)**: None — used the brand's actual logo asset (`logo-original.png` from Squarespace CDN) and inline SVG icons (phone, atomic starburst mask).

### 21st.dev Component Provenance

See [`21st-sources/provenance.md`](21st-sources/provenance.md) for query log and pattern attribution. Three queries run: `hero retro atomic vintage`, `sticky pill nav rounded`, `service cards bold borders shadow`. No raw component code copy-pasted — patterns translated from React/Tailwind into vanilla HTML + Tailwind CDN. HANDOFF rebuild path: React + Tailwind on Next.js maps cleanly back.

## Content Inventory

- **Real logo** pulled from Squarespace CDN (the fluffy white Maltese face + "Miriam's POOCHELLA" wordmark) → cropped to favicon-512.png and favicon.png
- **8 generated illustrations** (see IMAGE_LOG.md): hero, miriam-portrait, service-hydrobath (cropped), service-facial, service-fullgroom, vip-banner, pattern-atomic, exterior-banner
- **8 real dog photos** hotlinked from brand's Squarespace CDN for the VIP gallery section (`/gallery-1` page)
- **Real factual content** (see ACCURACY.md): address, hours, phone, services (Hydro Bath / Blueberry Facial / Bath & Full Groom), social links
- **6 paraphrased testimonials** from public review snippets (Yelp, Google, Facebook, Nextdoor)

## Share Preview

- **OG image source**: cropped from generated `hero.jpg` (Shag Maltese poolside) → 1200×630 JPEG @ 85 quality, ~172 KB
- **OG title**: `Miriam's Poochella — Palm Springs Dog Grooming · Best in the Valley`
- **OG description**: `Six-time Best Groomer in the Coachella Valley. Zurich-trained, by-appointment only.`
- **Favicon source**: cropped left half of brand logo (the dog face), scaled to 512×512 PNG
- **Theme color**: `#FFE0EC` (powder pink canvas)
- **Sub-pages with their own OG**: none — single-page site

## Image Generation Prompts

All 8 illustrations generated via Gemini Nano Banana Pro (heroes/banners) and Nano Banana 2 (services) + Grok Standard (pattern). Full prompts and quality scores in [`IMAGE_LOG.md`](IMAGE_LOG.md).

## Suggested Next Mockups

1. **Membership / "VIP Club" landing** — frame the regulars program as a vintage members-only club (cards, perks, monthly visits)
2. **Booking flow redesign** — full online appointment booking that respects the by-appointment ethos (calendar slots, breed/coat questionnaire, photo upload)
3. **Before/After gallery page** — long-form scrolling spread of real transformations from the salon
4. **"Meet the Staff" page** — 6 groomers with Shag-style illustrated portraits in the salon's pink palette
5. **Seasonal landing** — Coachella weekend, Palm Springs Modernism Week, Holiday Bows promo pages

## Build Timing

| Phase | Duration |
|---|---|
| Step 1: READ (site + sub-pages + reviews + 2 awards sources) | ~4 min |
| Step 2: DIRECTION (ui-ux-pro-max skill + frontend-design skill for FX in parallel) | ~3 min |
| Image Generation (8 images, sequential per cost rules, 1 NB2 timeout retry) | ~13 min |
| Selection page build + publish + Zack triage | ~5 min |
| Step 3: BUILD HTML (PRO-MAX one-page site) | ~12 min |
| Step 4: VERIFY + polish (hero title clip, hydrobath palette crop) | ~5 min |
| Step 5: BRIEF + ACCURACY + IMAGE_LOG | ~5 min |
| Step 6: PUBLISH (this step) | TBD |
| **Total: prompt to live link** | ~50 min target |

## Production Notes

For production deployment, **React + Tailwind on Next.js 15** is the natural stack. The panel-grid layout and color-blocked components map cleanly to Tailwind. The 8 Shag illustrations stay as static assets; the rest of the design is CSS (atomic SVG starbursts, layered geometric shadows, alternating color-blocked cards).

Estimated rebuild: 2–3 days. Budget extra time to:
- Hook up an actual phone-call-tracking system (recommend CallRail) — current is `tel:` link
- Add a real photo CMS for the VIP gallery (current hotlinks from Squarespace CDN won't scale if Miriam ever leaves Squarespace)
- Generate 4–6 additional Shag illustrations for sub-pages (about page, before/after gallery)
- Decide on online booking integration vs phone-only (current honors phone-only by design)
- Hosting: DreamHost via SFTP would work cleanly given the static-asset nature; or Vercel for the React rebuild
