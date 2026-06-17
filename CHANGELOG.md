# Changelog

All notable changes to the CipheX Brand Kit are documented here. This project follows
[Semantic Versioning](https://semver.org/) and [Keep a Changelog](https://keepachangelog.com/).

## [1.0.0] — 2026-06-17

First structured release of the brand kit.

### Added
- **Assets** — master wordmark (`logo/`), X-monogram (`symbol/`), product marks for CPX / CipheX
  Alpha / Atlas (`badges/`), the **Cipherion** parent mark (`cipherion/`), and favicons
  (`favicon/`), each as SVG plus a PNG set.
- **Brand Design Guide** — `ciphex-brand-design-guide.pdf` at the repo root, linked from the README
  and the preview site.
- **Design tokens** — `tokens/tokens.json` (W3C DTCG format) as the source of truth, with generated
  `variables.css`, `variables.scss`, a Tailwind v4 `tailwind.css` preset, and `fonts.css`.
- **Machine/AI readability** — `brand.json` manifest and `llms.txt` so tools and agents can generate
  on-brand output.
- **Developer package** — `package.json` (`@ciphex/brand-kit`) with subpath exports and a
  `build:tokens` script (Style Dictionary config).
- **Preview site** — a polished multi-section `index.html` for GitHub Pages (sticky nav, hero,
  logo/color/type/voice sections, a developer "Build" section, compliance footer) with a
  click-to-copy palette.
- **Accessibility** — `tokens/contrast.md`, a computed WCAG contrast matrix for brand pairings.
- **Governance** — `LICENSE` (proprietary brand-asset terms), `CONTRIBUTING.md`, and this changelog.
- **Web app icons** — `favicon.ico` and `site.webmanifest`.

### Changed
- Rewrote `README.md` as an asset index that links each asset to the relevant section of the Brand
  Design Guide.
- Replaced the legacy `CPX-Logo-200` files with the structured `assets/` tree.

### Fixed
- Corrected a mislabel: `badges/ciphex-badge-alpha.svg` previously held the Cipherion coin artwork.
  It now contains the actual CipheX Alpha mark (the monogram), with PNGs regenerated, and the
  Cipherion coin moved to `assets/cipherion/`.

[1.0.0]: https://github.com/Cipherion-Market-Research/Ciphex-Brand-Kit/releases/tag/v1.0.0
