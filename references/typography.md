# Typography Reference for Super Skill

## Primary Recommendations (free, contemporary, production-ready)

| Rank | Face | Role | Why | Pair with |
| --- | --- | --- | --- | --- |
| 1 | Geist | Product / tech UI | Clean, modern, SF-adjacent, excellent metrics | Geist Mono |
| 2 | Inter | Universal UI / dense data | Designed for screens, variable, tabular nums | Any good mono |
| 3 | Satoshi | Marketing + product | Warm geometric, versatile personality | Inter or Geist for body |
| 4 | Plus Jakarta Sans | Friendly contemporary | Geometric with character | — |
| 5 | DM Sans | Small labels / dense UI | Outstanding small-size legibility | — |
| 6 | Public Sans | Neutral / serious | Highly readable, government-grade | — |
| 7 | Space Grotesk | Distinctive headlines | More personality | Neutral body |

Other solid free options: Manrope, Figtree, Urbanist, Mona Sans, Hubot Sans.

Source quality filter: faces that feel at home on uncut.wtf (contemporary, well-drawn, free/open). Always confirm commercial license (most listed are OFL or equivalent).

## Quick Decision Guide

- Tech product / dashboard / dense UI → **Geist** or **Inter**
- Marketing site with personality → **Satoshi** or **Plus Jakarta Sans**
- Need mono for code/terminal → **Geist Mono**
- Maximum neutrality → **Inter** or **Public Sans**
- Small UI chrome / labels → **DM Sans** or Inter

## Optical & Metric Rules

- `font-optical-sizing: auto` (or explicit opsz axis)
- Tracking: slight negative for display (−0.01 to −0.03em); neutral or slightly open for tiny UI text
- Leading: labels 1.2–1.35 · body 1.45–1.6 · data tables ~1.25
- Always enable tabular figures for changing numbers: `font-variant-numeric: tabular-nums`
- Prefer variable fonts
- Fallback: `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`

## CSS Skeleton

```css
:root {
  --font-sans: "Geist", "Inter", system-ui, -apple-system, sans-serif;
  --font-mono: "Geist Mono", ui-monospace, "Cascadia Code", monospace;
}

html {
  font-family: var(--font-sans);
  font-optical-sizing: auto;
  -webkit-font-smoothing: antialiased;
}

.numeric {
  font-variant-numeric: tabular-nums;
}
```

## Pairing Anti-patterns

- Two strong geometric faces together
- Highly decorative face as body text
- Ignoring tabular numbers in data-heavy UIs
- Over-tracking body copy
- Using display optical size at 12–14px UI sizes without adjustment
