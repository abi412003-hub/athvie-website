# Athvie Global — Website

Landing page for **Athvie Global Private Limited** — a Bengaluru-based technology, marketing & growth firm working across ten industries.

## Highlights
- Single hand-written `index.html` — no framework, no build step, no dependencies
- Editorial layout: a typographic hero, an L-shaped services grid, a numbered sector index on native `<details>`, alternating full-width work rows, and an impact ledger
- Animated counters, a two-row client logo marquee, and scroll-reveal — all of which respect `prefers-reduced-motion`
- Keyboard-navigable throughout; a real mobile menu below 860px
- Content sourced from the official Athvie Global Profile 2025

## Design system
All tokens live in `:root` at the top of the `<style>` block:

| | |
|---|---|
| Type | 6 steps (`--fs-1`…`--fs-6`) plus one display size used only by the hero |
| Spacing | 4px base, `--sp-1`…`--sp-9`, with fluid `--gutter` and `--section` |
| Radius | `--r-1` 8px, `--r-2` 14px, `--r-3` 24px, `--r-pill` |
| Colour | `--bg*` surfaces, `--ink*` text, `--accent*`, `--line*`; one shared `--scrim` |
| Elevation | `--sh-1` / `--sh-2` — never coloured; the accent appears in no `box-shadow` |

Two fonts, four files: Sora 600/800 for headings and numerals, Inter 400/500 for everything else. Every weight is declared explicitly — an unstyled `h3` or `b` would otherwise inherit UA bold (700), which isn't loaded, and silently render at 800.

## Run locally
Open `index.html` in any browser — no build step, no server needed.

To match production (correct MIME types and range requests for the videos):

```bash
npx serve .
```

## Deploy
Static site on Vercel. Framework preset **Other**, no build command, no output directory. `vercel.json` sets cache headers for `/images`, `/logos` and `/videos`; the HTML is left on default revalidation so deploys are visible immediately.

## Contact
Athvie Global Private Limited · 873, Modi Hospital Rd, Rajajinagar, Bengaluru 560079
contact@athvie.com · +91 93538 94389
