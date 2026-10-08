# Page review: pages/aisle.com/index.html

Review date: 2026-10-08. Reviewer: Claude Code (checks run in this session).
Sources: S1 = https://christinecastro.com/work-with-me.html; S2 = https://aisle.com/. Both are owner-pasted official text read 2026-10-08 (sites blocked from this environment).

## Claim ledger

| Page location | Claim | Source | Supporting excerpt | Result |
|---|---|---|---|---|
| Header | "Prepared for the AISLE leadership team" | — | Framing, not a factual claim | OK |
| Eyebrow | "AI-native vulnerability management" | S2 | "AI-native vulnerability management for Enterprise" | OK |
| H1 | "AISLE has the research proof." | S2 | "475+ CVEs discovered by AISLE – and independently validated" | OK |
| H1 | "Here is how I would turn it into pipeline." | — | Labeled intent; was "A marketing leader turns it into pipeline" (an unsupported promise) | REWRITTEN |
| Hero | Full-time CMO or VP of Marketing; B2B cybersecurity marketing executive | S1 | "I am a B2B cybersecurity marketing executive looking for a full-time CMO or VP of Marketing role" | OK |
| Hero | "build marketing engines from zero" | S1 | "Two decades building marketing engines from zero" | OK |
| Hero | "report against company ARR, not lead volume" | S1 | "Marketing plans and reports against overall company ARR, not siloed marketing quotas." | OK |
| Card 1 | Category: "AI-native vulnerability management for Enterprise," discovery to verified fix | S2 | same; "From discovery to verified fix, autonomously" | OK; heading "A clear category" changed to "Category" (removed judgment) |
| Card 2 | 475+ CVEs, independently validated | S2 | "475+ CVEs discovered by AISLE – and independently validated – in widely used codebases." | OK |
| Card 3 | Posts on CVEs AISLE found in curl, Wireshark, FFmpeg | S2 | "AISLE Discovered Six curl CVEs…", "AISLE Discovers 16 CVEs in Wireshark…", "AISLE Discovers 6 High and Critical CVEs in FFmpeg" | OK; "Regular" and "Research-led content" removed (frequency not sourced) |
| Suggestion box | Proposed approach | S1 (method) | "Board reporting ties pipeline and program metrics directly to the ARR target." / "Selling to a CISO, a security architect and a procurement team at the same time" / "Reverse-funnel modeling from the ARR target" | OK; labeled "Suggestion" plus disclaimer |
| Proof | 21% → 73% | S1 | "marketing-influenced pipeline from 21% to 73% at a data access security startup" | OK |
| Proof | $4.2M · 2 → 20, Series B IAM | S1 | "a $4.2M budget and a team scaled from 2 to 20 at a Series B IAM company" | OK |
| Proof | 750K → 4M+ in 18 months | S1 | "protected endpoints from 750K to 4M+ in 18 months at a hyper-growth endpoint security company" | OK |
| Proof | 1,112% ROI, inaugural conference | S1 | "1,112% ROI on a user conference built from nothing" / "1,112%ROI, inaugural conference" | OK |
| 90 days | Observe / Analyze / Execute steps | S1 | "Days 1 to 30 map every stakeholder…", "Days 31 to 60 turn that into a funnel model…", "Days 61 to 90 install the dashboards…" | OK |
| Not the right hire | Two conditions | S1 | "When the mandate is lead volume rather than pipeline and ARR." / "When the company wants a brand caretaker rather than an operator who will rebuild the funnel math." | OK |
| Footer | "Not affiliated with or endorsed by AISLE." | — | Disclaimer | OK |

No testimonials, logos, demo lengths, recency claims ("just launched", "new") or AISLE funding-stage claims appear.

## Viewports (measured in headless Chromium via Playwright)

| Check | window.innerWidth × innerHeight | scrollWidth | Elements past the viewport edge | Screenshot |
|---|---|---|---|---|
| Desktop | 1440 × 900 | 1440 | none | pages/aisle.com/screenshots/desktop-1440x900.png |
| Phone (mobile emulation) | 390 × 844 | 390 | none | pages/aisle.com/screenshots/phone-390x844.png |

The desktop full page and phone viewport crops (top and middle) were viewed as images. No clipping, overlap or horizontal scroll.

## Links

| Text | Target | Result |
|---|---|---|
| Discuss a leadership role / Book a conversation | https://calendly.com/christinecastro978/meetme | Matches COMPANY.md. UNVERIFIED live: the request was blocked by this environment's network policy (HTTP 000). |
| Resume and one-pager | https://christinecastro.com/resume.html | Matches source. UNVERIFIED live (blocked). |
| Email me | mailto:christine@christinecastro.com | Matches source. |
| Source links | https://aisle.com/, christinecastro.com work-with-me and observe-analyze-execute | Match sources. UNVERIFIED live (blocked). |

## Unresolved
- Open the Calendly link on your own device and confirm it loads your booking page.
- On a real phone: the emulated 390px check passed, but no physical-device check was run.
- Brand colors and fonts are not confirmed; the page uses a neutral style.

---

# Page review: pages/botcity.dev/index.html

Review date: 2026-10-08. Built with skills/account-page/SKILL.md. Claim ledger: pages/botcity.dev/SOURCES.md (every heading, card, button and footer mapped).

Repairs made during review:
- A suggestion bullet said the buyer "does not yet have a name for the problem," which contradicted the H1 (BotCity already uses "Shadow Python"). Rewritten to "teach buyers to use the name Shadow Python."
- Carry-over scan for "AISLE", "CVE" and "research": none found.

| Check | window.innerWidth × innerHeight | scrollWidth | Overflow | Screenshot |
|---|---|---|---|---|
| Desktop | 1440 × 900 | 1440 | none | pages/botcity.dev/screenshots/desktop-1440x900.png |
| Phone (mobile emulation) | 390 × 844 | 390 | none | pages/botcity.dev/screenshots/phone-390x844.png |

Viewed: the desktop full page and phone viewport crops (top and middle). No clipping or horizontal scroll.
Links: booking buttons → https://calendly.com/christinecastro978/meetme (matches COMPANY.md; live test UNVERIFIED, blocked). Source links → https://botcity.dev/sentinel.
Unresolved: live link test; real-device phone check; brand colors; BotCity's funding stage (fit marked REVIEW in TARGETS.md).

---

# Restyle: both pages (2026-10-08)
Applied company-motion/STYLE.md (christinecastro.com CSS). Wording and claims are unchanged; only the `<style>` block, the hero wrapper and the stat tags changed.

| Check | aisle.com | botcity.dev |
|---|---|---|
| HTML structure (parser: no unclosed or mismatched tags) | PASS after fixing one mismatched `</div>` on the "475+ CVEs" card | PASS |
| Desktop 1440 × 900: scrollWidth, overflow | 1440, none | 1440, none |
| Phone 390 × 844: scrollWidth, overflow | 390, none | 390, none |
| External requests | 0 | 0 |
| Fonts loaded (Fraunces, Inter, IBM Plex Mono) | all true | all true |
| Viewed | desktop full page | desktop full page and phone top |

Found and fixed after viewing: the suggestion disclaimer rendered at body size (CSS specificity), and "$4.2M · 2 → 20" wrapped in the 4-up grid. Checks rerun; both PASS.

Links (domain now allowed): resume.html, work-with-me.html and observe-analyze-execute.html return 200. The Calendly link returns 200, but its content is rendered by JavaScript, so the booking page itself was not viewed.
Live source recheck: the proof sentence on the live work-with-me.html matches the owner-pasted text.
Still open: real-device phone check.
