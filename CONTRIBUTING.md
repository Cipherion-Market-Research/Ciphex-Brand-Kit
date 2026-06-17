# Contributing to the CipheX Brand Kit

This repo is the source of truth for CipheX brand **assets and tokens**. The brand *rules* live in
the CipheX Brand Design Guide — changes here should follow it, not reinterpret it.

## Requesting assets or formats

Need a mark, size, or format that isn't here (e.g. a specific export, a partner lockup)? Don't
recreate it yourself — email **`brand@ciphex.io`**. Modifying or rebuilding the marks is not
permitted under the [LICENSE](LICENSE).

## Proposing a change

1. Branch from `main`.
2. Make the change. If you touch color/type values, edit **`tokens/tokens.json` first** (the source
   of truth), then regenerate the consumables (below) — don't hand-edit `variables.css` only.
3. Update [`CHANGELOG.md`](CHANGELOG.md) under "Unreleased."
4. Open a PR. Brand-affecting changes are reviewed by the CipheX brand team before merge.

## Regenerating tokens

`variables.css`, `variables.scss`, and the Tailwind preset derive from `tokens.json`:

```bash
npm install
npm run build:tokens   # style-dictionary build
```

After regenerating, re-check [`tokens/contrast.md`](tokens/contrast.md) if any color changed.

## Versioning

Semantic versioning, tagged as GitHub Releases:

- **major** — a mark changes or is removed, or a token is renamed/removed (breaking for consumers).
- **minor** — new assets, tokens, or formats added.
- **patch** — fixes, docs, non-breaking corrections.

Bump `version` in `package.json` and tag the release so partners can pin a version.

## What lives where

- `assets/` — logos, marks, favicons (SVG + PNG). See [README](README.md).
- `tokens/` — design tokens (DTCG + CSS/SCSS/Tailwind) and the contrast reference.
- `brand.json` / `llms.txt` — machine- and AI-readable brand manifest.
