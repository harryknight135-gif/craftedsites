# craftedsites — Repo CLAUDE.md

This file overrides the global CLAUDE.md for this specific project, because
craftedsites was built as a single-file static HTML site (predates the
Next.js stack rule). Keep the spirit of the global rules (read first,
define before build, look before create, test before respond, do exactly
what is asked) — but adapt the tech specifics to this project.

## Tech stack (actual)

- **Single file**: `index.html` (all CSS + JS inline, ~3400 lines)
- **No build step**, no framework, no package manager
- **Fonts**: Google Fonts (Syne, DM Sans, Playfair Display, Bebas Neue,
  Permanent Marker, Anton)
- **Animations**: GSAP 3 + ScrollTrigger (CDN), Motion vanilla (CDN ESM)
- **Form backend**: Formspree (`https://formspree.io/f/xgoqkndw`)
- **Hosting**: GitHub (`harryknight135-gif/craftedsites`) → Cloudflare
  Pages (`craftedsites.pages.dev`), auto-deploy on push to `main`
- **Local dev**: `python -m http.server 8765` (see `.claude/launch.json`)

## How to make changes

1. Edit `index.html` (everything lives there)
2. Save image assets in the repo root (`vanta-can.png`, `harry.png`, etc.)
3. Commit + push to GitHub — Cloudflare deploys automatically
4. Verify on `craftedsites.pages.dev` (hard reload to bypass cache)

## File map

- `index.html` — the whole site
- `harry.png` — founder photo (contact section avatar)
- `vanta-can.png`, `vanta-flavor.png` — VANTA demo background images
- `Hyper_realistic_cinematic_luxu.mp4` — VANTA hero video
- `.gitignore` — excludes `.claude/`, `*.bak`
- `project_specs.md` — current task spec (defined before every change)

## Rules that still apply

- **Look before you create** — read existing patterns before adding new
  ones. The VANTA card + demo is the canonical pattern for featured work.
- **Do exactly what is asked** — no scope creep.
- **Explain like to a 15-year-old** — every reply uses the format from
  the global CLAUDE.md (What I did / What you need to do / Why / Next /
  Errors).
- **Test before responding** — at minimum, verify the site loads in the
  preview server (`python -m http.server 8765`) and no console errors
  appear.
- **Define before you build** — update `project_specs.md` for any
  non-trivial change, show it, wait for approval.
