---
name: account-page
description: Build one local, unpublished account page that pitches Christine Castro to a target company's leadership, with every factual claim tied to an exact official source excerpt, then check desktop and phone layouts. Use for each target in company-motion/TARGETS.md.
---

# Account page

Builds `company-motion/pages/<domain>/index.html` for one target company. Worked example that passed review: `company-motion/pages/aisle.com/` (page, `SOURCES.md`, screenshots) and `company-motion/PAGE-REVIEW.md`.

This skill creates local files only. It does not publish, upload, send or contact anyone. Read `company-motion/AUTHORITY.md` first. Outreach and spending stay paused.

## 1. Read these inputs (stop if one is missing)

| Input | Use |
|---|---|
| `company-motion/COMPANY.md` | Seller, offer, lead path, proof, next-step link |
| `company-motion/targets/<domain>.md` | Target facts with source URL, exact excerpt and read date |
| `company-motion/TARGETS.md` | The sourced reason the offer fits this target |
| `company-motion/AUTHORITY.md`, `company-motion/AGENTS.md` | Limits |

If `targets/<domain>.md` is missing or names another company, stop and ask the owner to run target research first. Do not research inside this skill.

Fixed values from COMPANY.md (recheck them each run):
- Seller: Christine Castro. Lead path: full-time CMO / VP of Marketing (owner decision, 2026-10-08).
- Primary button: "Discuss a leadership role" → https://calendly.com/christinecastro978/meetme
- Secondary: https://christinecastro.com/resume.html and mailto:christine@christinecastro.com

## 2. Build the page

Output: one file, `company-motion/pages/<domain>/index.html`.
- Style: follow `company-motion/STYLE.md` (christinecastro.com tokens, Fraunces / Inter / IBM Plex Mono, amber accent, hairline card grids, 2px buttons). Copy the full `<style>` block from `pages/aisle.com/index.html`; it already embeds the fonts.
- Standalone: inline CSS and base64-embedded fonts. No external scripts, font links or images. No target logos.
- Responsive: `<meta name="viewport" content="width=device-width,initial-scale=1">`, with grids collapsing to one column on phones. The site is dark-only; do not add a light theme.
- Add `<meta name="robots" content="noindex,nofollow">`.

Sections, in order (use the AISLE page as the template):
1. Header: "Christine Castro" and "Prepared for the <Target> leadership team".
2. Hero: one headline that uses a sourced target fact and frames the rest as Christine's intent ("Here is how I would…"), never as a promised result. A sourced one-line introduction and the two buttons.
3. "What <Target> already publishes": 2–3 cards, each a quoted or closely paraphrased target fact with a visible source link.
4. "An idea for <Target>": a box tagged **Suggestion**, ending with "This is a proposal, not a description of <Target>'s current marketing." Build it from Christine's sourced method in COMPANY.md, linked to the fit reason in TARGETS.md.
5. "What I have built before": proof from COMPANY.md, with a source link.
6. "The first 90 days" (Observe / Analyze / Execute).
7. "When I am not the right hire," then the buttons again.
8. Footer: "Prepared by Christine Castro. Not affiliated with or endorsed by <Target>. Facts about <Target> come from <domain>, read <date>."

## 3. Claim rules

- Every factual claim (headings, buttons, captions and footer included) needs an exact excerpt from an official source in the inputs.
- **Missing source:** if a claim has no exact excerpt, remove it or rewrite it as a labeled suggestion. Never fill the gap with an invented fact. If a whole section has no supported proof, use sourced product facts instead or omit the section, and list the omission in `SOURCES.md`.
- **Conflicting sources:** show both URLs and excerpts to the owner and ask which is current. Do not pick one.
- Never use: invented testimonials, logos, demo lengths, outcomes, recency words ("new", "just launched", "regular"), funding stage, or judgment words presented as fact ("clear", "leading").
- Keep out the target's competitive claims (for example "10x… than <competitor>"), and any of Christine's claims with no named company or issuer ("3x ARR YoY", "Top 50").
- Owner-pasted text counts as an official source. Label it "owner-pasted" with the URL and read date.

Save `company-motion/pages/<domain>/SOURCES.md` as a table: page text | source | exact excerpt. Add a "Deliberately left out" line.

## 4. Check the page

Run every check and record actual results. Repair failures, then rerun.

1. **Consistency:** read the headline and the suggestion box together; they must not contradict each other.
2. **Claim ledger:** walk the HTML top to bottom. Each claim maps to a `SOURCES.md` row, or it is fixed.
3. **Desktop:** open the page in a browser at a 1440 × 900 viewport. Read `window.innerWidth` and `window.innerHeight` first; resizing a window is not proof.
4. **Phone:** 390 × 844 viewport (mobile emulation). If the browser cannot reach 390px, mark phone as UNVERIFIED and do not report clipping.
5. **Overflow**, in each viewport:
   ```js
   ({w: innerWidth, h: innerHeight, scroll: document.documentElement.scrollWidth,
     over: [...document.querySelectorAll('body *')].filter(e => {const r=e.getBoundingClientRect(); return r.right > innerWidth + .5 || r.left < -.5}).length})
   ```
   Pass when `scroll == w` and `over == 0`.
6. **Look at it:** take screenshots to `company-motion/pages/<domain>/screenshots/desktop-1440x900.png` and `phone-390x844.png`, and view the images. Only claim visual inspection after an image or browser tool showed the page.
7. **Network:** the page makes zero non-`file:`/`data:` requests, and `document.fonts.check()` is true for Fraunces, Inter and IBM Plex Mono.
8. **Links:** list every `<a href>`. The booking buttons must equal the COMPANY.md next-step link. Open it if the network allows; otherwise mark it UNVERIFIED.
9. If a `file://` URL is blocked, serve only the page folder on an unused `127.0.0.1` port, check it, then stop the server.

In this cloud workspace, the AISLE review ran Playwright from `/opt/node22/lib/node_modules/playwright` with Chromium at `/opt/pw-browsers/chromium`. For Python scripts, use the interpreter in `company-motion/.runtime.json`.

## 5. Record

- Add a section for this page to `company-motion/PAGE-REVIEW.md`: claim ledger, measured viewports, screenshots, link results and unresolved checks.
- Append the step, artifact paths, PASS/FAIL/UNVERIFIED checks and the next task to `company-motion/PROGRESS.md`. Keep earlier entries.
- Show the page to the owner and stop. Do not edit an already-reviewed page while building another.
