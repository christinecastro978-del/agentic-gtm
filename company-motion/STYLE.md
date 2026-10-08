# Style guide (from christinecastro.com)

Source: CSS on https://christinecastro.com/work-with-me.html and https://christinecastro.com/assets/nav-core.js, read 2026-10-08. The site has no published style-guide page (none among the 85 sitemap URLs), so its live CSS is the guide.

## Colors (dark theme)
| Token | Value | Use |
|---|---|---|
| --ink | #0E141C | Page background |
| --ink-2 | #131B25 | Hero band, cards, notes |
| --ink-3 | #1B2531 | Deeper surface |
| --paper | #F3EFE7 | Headings, primary text |
| --paper-dim | #C7C2B6 | Body and card text |
| --amber | #D98F3E | Accent: eyebrows, primary button, stats, links (hover #E8A052) |
| --teal | #7BAFA6 | Secondary accent (stage labels) |
| --slate | #8A94A0 | Captions, footer, source lines |
| --line / --line-strong | rgba(243,239,231,.12 / .22) | Dividers, borders |

## Type
- Headings and wordmark: Fraunces 600, letter-spacing -.01em, line-height 1.08. Wordmark "Christine Castro" at 17px, #FEFDFB.
- Body: Inter (the site names 'IBM Plex Sans' first but loads Inter from Google Fonts).
- Labels, eyebrows, buttons, captions, footer: IBM Plex Mono. Eyebrows are 11px, .22em tracking, uppercase, amber.
- Account pages embed latin subsets of all three as base64 woff2 (SIL Open Font License), so the pages need no network requests.

## Components
- Buttons: Plex Mono 13px, padding 13px 24px, radius 2px. Primary is an amber fill with ink text; secondary is a ghost with a --line-strong border that turns amber on hover.
- Card grids: 1px gaps over a --line background (hairline grid), with ink-2 cards padded 28px 26px.
- Callouts: ink-2 background with a 3px amber left border, radius 0 3px 3px 0.
- Stats: Fraunces 600 in amber.
- Layout: 1080px max width; 32px gutters (20px at 640px and below).
