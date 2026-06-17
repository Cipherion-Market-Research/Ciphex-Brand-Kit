# CipheX Brand Kit

The official logo and mark assets for **CipheX** — an ecosystem by Cipherion.

This repo is just the **files**. The rules for how to use them live in the **CipheX Brand Design
Guide** ([`ciphex-brand-design-guide.pdf`](ciphex-brand-design-guide.pdf)). This README maps each
asset to what it is and points you to the section of the guide that governs it.

> If you have both this kit and the guide: grab files here, follow the guide there. Route all copy
> and any non-obvious usage through `brand@ciphex.io` before publishing.

**Quick links:** [assets](assets) · [design tokens](tokens) · [design guide (PDF)](ciphex-brand-design-guide.pdf) · [preview site](https://cipherion-market-research.github.io/Ciphex-Brand-Kit/) · [brand.json](brand.json) · [llms.txt](llms.txt) · [contributing](CONTRIBUTING.md) · [changelog](CHANGELOG.md)

### Use

Everything is plain files — copy what you need from [`assets/`](assets) and [`tokens/`](tokens),
then reference them directly:

```html
<!-- web fonts + design tokens -->
<link rel="stylesheet" href="tokens/fonts.css" />
<link rel="stylesheet" href="tokens/variables.css" />
```

```css
body { background: var(--cpx-bg); color: var(--cpx-text); font-family: var(--cpx-font-sans); }
a    { color: var(--cpx-accent); }
```

Tailwind v4? `@import "tokens/tailwind.css";`. **Building with AI?** Point your tool at
[`llms.txt`](llms.txt) or [`brand.json`](brand.json) so it generates on-brand.

> A published `@ciphex/brand-kit` npm package is planned — for now, use the files directly.

---

## What's in here

Everything is under [`assets/`](assets). Each mark ships as **SVG** (vector — use this by default)
with a matching **PNG** set for tools that can't take vectors.

| Folder | What it is | When to use it | Guide section |
| --- | --- | --- | --- |
| [`logo/`](assets/logo) | Master CipheX **wordmark** — the lead mark | Default choice for almost everything | §05 Logo system |
| [`symbol/`](assets/symbol) | **X-monogram** — the standalone avatar | Social profile pictures, app icons, anywhere the wordmark is too small | §05 Logo system |
| [`badges/`](assets/badges) | **Product marks** (CPX, Alpha, Atlas) | In-context only, inside that product's surfaces — never as the master logo | §05 Logo system |
| [`cipherion/`](assets/cipherion) | **Cipherion** parent mark | Parent endorsement — corporate & legal footers, co-branding | §05 Logo system |
| [`favicon/`](assets/favicon) | X-monogram **favicons** | Browser tabs / web app icons | §05 Logo system |
| [`tokens/`](tokens) | **Design tokens** — colors, type, opacity | Building UI; consume `var(--cpx-*)` instead of hardcoding hex | §03 Color · §04 Typography |

### Picking a variant

- **Light vs. dark ground** — `logo/` ships `-black` (ink on cream, the primary form) and `-white`
  (cream on dark, the reversed form). Match the file to your background. See §03 Color.
- **SVG vs. PNG** — reach for the SVG first. Use a PNG only where vectors aren't accepted; pick the
  size at or just above your render size (PNGs are provided at 256/512/1024, and 512w/1024w/2048w
  for the wordmark).
- **Clear space & minimum sizes** are defined in §05 — when the wordmark gets too small to read,
  switch to the X-monogram from `symbol/`.

---

## File map

```
assets/
├─ logo/          Master CipheX wordmark (lead mark)
│  ├─ ciphex-wordmark-black.svg     ink on cream (primary)
│  ├─ ciphex-wordmark-white.svg     cream on dark (reversed)
│  └─ png/                          black & white · 512w · 1024w · 2048w
├─ symbol/        X-monogram (standalone avatar)
│  ├─ ciphex-symbol.svg
│  └─ png/                          256 · 512 · 1024
├─ badges/        Product marks — in-context use only
│  ├─ ciphex-badge-token.svg        CPX token mark (gold coin)
│  ├─ ciphex-badge-alpha.svg        CipheX Alpha mark (monogram)
│  ├─ ciphex-badge-atlas.svg        Atlas mark
│  └─ png/                          each mark · 256 · 512 · 1024
├─ cipherion/     Parent mark — corporate & legal footers, co-branding
│  ├─ cipherion-mark.svg            black coin + white monogram
│  └─ png/                          256 · 512 · 1024
└─ favicon/       X-monogram favicons + favicon.ico + site.webmanifest

tokens/           Design tokens (see tokens/README.md)
├─ tokens.json    W3C Design Tokens — source of truth
├─ variables.css  CSS custom properties (--cpx-*)
├─ variables.scss SCSS variables ($cpx-*)
├─ tailwind.css   Tailwind v4 @theme preset
├─ fonts.css      @font-face / web-font imports
└─ contrast.md    WCAG contrast matrix

brand.json        Machine-readable brand manifest
llms.txt          AI/LLM brand brief
index.html        Preview site (GitHub Pages)
package.json      npm packaging (planned — not yet published)
LICENSE · CONTRIBUTING.md · CHANGELOG.md
```

The product marks map to the ecosystem: **CPX** (token), **CipheX Alpha** (execution), **Atlas**
(RWA), all under the **Cipherion** parent. The guide's §01 covers who's who.

## Design tokens

For building UI, [`tokens/`](tokens) holds the brand's colors, typography, and opacity ramp as
machine-readable tokens — transcribed from §03/§04 of the guide. Use these instead of hardcoding
values:

```css
@import "tokens/variables.css";
body { background: var(--cpx-bg); color: var(--cpx-text); font-family: var(--cpx-font-sans); }
a    { color: var(--cpx-accent); }
```

`tokens.json` is the source of truth (DTCG format); the CSS/SCSS files are generated mirrors. See
[`tokens/README.md`](tokens/README.md) for the full reference and theming.

---

## Before you ship

The guide is the source of truth for color, typography, clear space, misuse, co-branding, imagery,
and compliance — don't reverse-engineer them from these files. If a format you need isn't here, or
you're unsure whether a use is on-brand, ask first.

- **Brand & compliance review / asset requests:** `brand@ciphex.io`
- **Living reference for the current look:** ciphex.io

---

## License

Copyright © 2026 Cipherion Capital SA, CipheX Capital Ecosystem

These logos, marks, and brand assets (the "Assets") are the proprietary property of Ciphex and are
protected by trademark and copyright law.

Permission is granted to use the Assets solely to reference, link to, or describe Ciphex in
accordance with the CipheX Brand Design Guide. You may **not**:

- Modify, distort, recolor, or recreate the Assets;
- Use the Assets to imply endorsement, sponsorship, or affiliation without prior written permission;
- Use the Assets as part of your own product, service, or company name, logo, or branding.

All other rights are reserved. See [`LICENSE`](LICENSE) for the full terms. For licensing requests
beyond this scope, contact the Ciphex brand team at `brand@ciphex.io`.
