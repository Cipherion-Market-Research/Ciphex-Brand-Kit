# Color Contrast Reference

WCAG 2.1 contrast ratios for CipheX color pairings, computed from the token values in
[`tokens.json`](tokens.json). Thresholds: **AA** ≥ 4.5 (normal text) / ≥ 3.0 (large ≥ 24px or
18.66px bold); **AAA** ≥ 7.0 (normal).

## On cream grounds (light)

| Foreground | Background | Ratio | Grade |
| --- | --- | --- | --- |
| Ink Primary `#1c1e24` | Cream `#fbfaf6` | 15.95 | AAA |
| Ink Body `#3a3528` | Cream `#fbfaf6` | 11.69 | AAA |
| Ink Muted `#6b6552` | Cream `#fbfaf6` | 5.57 | AA |
| Ink Subtle `#756f5e` | Cream `#fbfaf6` | 4.80 | AA |
| Primary Blue `#0050d6` | Cream `#fbfaf6` | 6.45 | AA |
| Deep Blue `#003fa8` | Cream `#fbfaf6` | 8.83 | AAA |
| Ink Primary `#1c1e24` | Surface `#f0ede4` | 14.23 | AAA |
| Primary Blue `#0050d6` | Surface `#f0ede4` | 5.75 | AA |

## On dark grounds

| Foreground | Background | Ratio | Grade |
| --- | --- | --- | --- |
| Cream `#fbfaf6` | Hero `#0a0c10` | 18.74 | AAA |
| Cream `#fbfaf6` | Panel `#0c0e13` | 18.48 | AAA |
| Soft Blue `#5b9dff` | Hero `#0a0c10` | 7.19 | AAA |
| Glow Blue `#4d8fff` | Hero `#0a0c10` | 6.23 | AA |
| Primary Blue `#0050d6` | Hero `#0a0c10` | 2.91 | ✗ Fail |

## Notes

- **Use Soft Blue, not Primary Blue, for blue text/links on dark grounds.** Primary Blue on dark
  fails (2.91) — which is exactly why the guide specifies Soft Blue (`#5b9dff`) for "headings on
  dark." Primary Blue remains correct on cream (6.45, AA).
- **Ink Subtle** (4.80) and **Ink Muted** (5.57) clear AA for normal text but not AAA — keep them for
  secondary/meta copy, not long-form body text.
- Ratios computed per the WCAG 2.1 relative-luminance formula. Re-run after any token change.
