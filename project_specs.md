# project_specs.md — Aurelle Beauty & Wellness — Featured Work Tile + Demo

## What the change does

Add a second featured work tile to the `#work` section of the main site,
sitting next to the existing VANTA Energy tile. Tile size matches VANTA
exactly (full-width, 21:9 aspect ratio on desktop). Clicking the tile
opens a full-screen demo overlay (mirroring the `#vanta-demo` pattern)
that walks through the Aurelle brand — homepage hero, trust strip,
best-sellers grid, two-column wellness section, stats strip, footer.

## Who uses it

The same visitor who clicked through VANTA. This is a portfolio piece
demonstrating range: VANTA is bold/Gen-Z/sports, Aurelle is luxe/clean/
editorial. Two opposite ends of the design spectrum, both built well.

## Tech stack

Same as the rest of the project: HTML + CSS + JS inside `index.html`.
No new dependencies. New image assets go in the repo root.

## Brand system (from the mockup)

| Token | Value | Use |
|---|---|---|
| `--aur-cream` | `#F2EBE0` | Page background, soft surfaces |
| `--aur-cream-2` | `#E8DFD0` | Alt card backgrounds |
| `--aur-black` | `#0F0F0F` | Hero, primary text |
| `--aur-text` | `#2A2520` | Body text on cream |
| `--aur-mute` | `#7A7066` | Muted text |
| `--aur-gold` | `#C9A876` | Accent (italic emphasis words, hover) |
| `--aur-gold-d` | `#A88654` | Darker gold for buttons |

Typography:
- Display headlines: **Cormorant Garamond** (serif, italic for emphasis)
- Brand mark / body: **Manrope** (clean modern sans)
- Eyebrows: tracked-out uppercase in Manrope 500

## Tile (what's visible in `#work`)

- Class: `.aurelle-card` (mirrors `.vanta-card` sizing + behaviour)
- Background: `aurelle-hero.jpg` (the dark hero shot — model + serum)
- Subtle dark→warm gradient overlay
- Badge: "Beauty & Wellness" in gold
- Category: "Skincare & Lifestyle"
- Brand mark: "AURELLE" (Cormorant or Manrope, weight chosen to match
  the brand logo in the mockup)
- CTA button: "View Live Demo" in gold pill
- Same aspect ratio responsiveness: 21/9 → 16/9 (≤1024px) → 4/3 (≤540px)

## Demo overlay (sections in order)

1. Nav — AURELLE logo + nav links + search/cart icons (black bg)
2. Hero — full-width split: dark left with "Radiate / Confidence." + sub
   + buttons; right side full-bleed image (model + serum)
3. Trust strip — 4 icons: Clean / Cruelty Free / Dermatologist / Sustainable
4. Best-sellers — heading + 4-product grid (Radiance Serum, Hydra-Luxe
   Moisturizer, Detox Clay Cleanser, Wellness Glow)
5. Two-column "Nourish Your Skin. Elevate Your Life." — image left,
   copy + CTA right
6. Stats strip — 10K+ Happy Customers / 4.9 Rating / 30-day guarantee /
   Free shipping
7. Footer — logo + tagline + Join community + 4 column links + payment
   icons

Close behaviour: same as VANTA — `X` button top-right, ESC key, scroll-lock
while open.

## Data / images / where stored

All in repo root. User to save:

| Filename | Image |
|---|---|
| `aurelle-hero.jpg` | Reference image 2 — model holding serum, dark bg |
| `aurelle-wellness.jpg` | Reference image 3 — model with sunlight |
| `aurelle-moisturizer.jpg` | Reference image 4 — Hydra-Luxe jar |
| `aurelle-serum.jpg` | Reference image 5 — Radiance Glow Serum |

User to save **separately**. I cannot save chat images to disk.

## Third-party services

None new. Site stays static.

## Done = the following all true

- [ ] Aurelle tile visible in `#work`, next to VANTA, identical size
- [ ] Tile click + Enter/Space open the demo
- [ ] Demo matches the mockup visually (palette, type, structure)
- [ ] All 4 images render correctly
- [ ] Close button + ESC + scroll-lock work
- [ ] GSAP entrance animation on the tile (matches existing pattern)
- [ ] Motion hover-lift on the tile (matches existing pattern)
- [ ] No console errors
- [ ] Mobile responsive (≤540px tile becomes 4/3, demo stacks)

## Open questions for user

- Confirm filenames (or rename if preferred).
- Should the Best-sellers grid in the demo use placeholder product cards
  for the 2 products NOT shown in the references (Detox Clay Cleanser,
  Wellness Glow)? Or skip them and show only the 2 we have?
