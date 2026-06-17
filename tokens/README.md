# CipheX Design Tokens

Machine-readable brand values — colors, typography, and opacity — so developers can consume the
CipheX brand programmatically instead of reading them off the guide.

All values are transcribed from the **CipheX Brand Design Guide** (§03 Color, §04 Typography). The
guide remains the source of truth; if anything here disagrees with it, the guide wins.

## Files

| File | Format | Use it for |
| --- | --- | --- |
| `tokens.json` | [W3C Design Tokens (DTCG)](https://www.designtokens.org/tr/drafts/format/) | The source of truth. Feed it to Style Dictionary, Tokens Studio, Figma, etc. |
| `variables.css` | CSS custom properties | Drop into any web project; `var(--cpx-*)` |
| `variables.scss` | SCSS variables | Sass build pipelines; `$cpx-*` |

`variables.css` and `variables.scss` are generated mirrors of `tokens.json` — **edit `tokens.json`
first**, then regenerate the others.

## Quick start (CSS)

```css
@import "ciphex-brand-kit/tokens/variables.css";

body            { background: var(--cpx-bg); color: var(--cpx-text); font-family: var(--cpx-font-sans); }
a               { color: var(--cpx-accent); }
.eyebrow        { font-family: var(--cpx-font-mono); text-transform: uppercase; letter-spacing: var(--cpx-tracking-mono); }
```

Add `data-theme="dark"` to a container (or `<body>`) to switch semantic variables to the dark
grounds with the cream-text opacity ramp.

## Token tiers

- **Primitive** (`--cpx-blue-primary`, `--cpx-cream`, …) — the raw palette. Don't hardcode hex; use
  these.
- **Semantic** (`--cpx-bg`, `--cpx-text`, `--cpx-accent`, …) — role-based aliases. **Prefer these in
  product code** so theming stays centralized.

## Rules baked into the tokens

- **One accent.** Blue (`--cpx-accent`) carries every emphasis. Status colors are functional /
  data-viz only — never brand accents.
- **Warm, never pure.** Grounds are cream, text is warm ink — never `#ffffff` or `#000000`.
- **Cream on dark, by opacity.** On dark grounds, text is the cream stepped down via the opacity
  ramp, never grey.

## Regenerating

There's no build tooling committed yet. To regenerate the CSS/SCSS from `tokens.json` with
[Style Dictionary](https://amzn.github.io/style-dictionary/):

```bash
npx style-dictionary build
```

(Add a `config.json` first.) Until then, keep `variables.css` / `variables.scss` in sync by hand.
