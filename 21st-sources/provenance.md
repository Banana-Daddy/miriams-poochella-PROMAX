# 21st.dev Component Provenance — Miriam's Poochella PRO-MAX

Queries run during DIRECTION (2026-05-15):

| Query | Selected pattern | What we borrowed |
|---|---|---|
| `hero retro atomic vintage` | "Hero 03" (Ali Imam) | Giant cropped-type display + icon embedded inside the headline — translated into our Anton/Abril display with the "POOCHELLA" wordmark wrapped around the dog-face mascot. |
| `sticky pill nav rounded` | "3D Adaptive Navigation Bar" (PillBase) | Single floating pill with sticky scroll behavior — simplified into a sticky pill with offset color-block shadow on scroll. We do NOT use the 3D illumination layers (too soft for atomic poster aesthetic); we use hard plum borders + offset cabana-pink shadow instead. |
| `service cards bold borders shadow` | "Service Card" (Thiings-style) | Number-prefixed service cards (001/002/003) with colored backgrounds, mascot-image bottom-right composition, "LEARN MORE →" CTAs. Translated into our atomic-blocked service cards with the Shag illustrations as the foreground subject. |

No raw component code was directly copy-pasted. Patterns translated from React/Tailwind into vanilla HTML + Tailwind CDN. HANDOFF rebuild path: React + Tailwind on Next.js maps cleanly back to the original 21st.dev components if needed.
