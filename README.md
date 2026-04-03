# 💍 Will You Marry Me?

A minimal, elegant proposal website built for one person, one moment.

---

## Overview

A single-file HTML website designed to propose marriage. It features bilingual content (English & Spanish), animated star backgrounds, milestone day counters, a yes/no interaction, and a hidden timeline that tells the story behind the proposal — visible only to those curious enough to find it.

---

## Pages

### Main — The Proposal
The opening screen. A floating heart, a horizontal rule, and the question: *Will you marry me? / ¿Puedo ser tu esposo?*

Two buttons sit below:
- **Yes / Sí** — leads to the celebration page
- **No** — leads to a graceful fallback message

### Yes Page
Displays a short personal message and a panel with three milestone counters — each showing the number of days since a key moment in the relationship:

| Milestone | Date |
|-----------|------|
| First Kiss | June 28, 2019 |
| Started Dating | July 19, 2019 |
| Became Official | September 14, 2019 |

Day counts update automatically based on the current date.

### No Page
A kind, bilingual response: *"That's okay — we can still enjoy life together anyway."* Includes a button to go back and reconsider.

---

## Hidden Feature — The Timeline

**Trigger:** Triple-tap / triple-click the floating heart icon on the main page.

A panel slides up from the bottom revealing a private timeline — the story of everything that happened before the proposal, unknown to Stef until this moment.

| Date | Moment |
|------|--------|
| Sep 30, 2025 | The decision — knowing she was the one |
| Oct 6, 2025 | Leo becomes the first to know |
| Dec 22, 2025 | The itinerary is mapped out with Leo |
| Jan 6, 2026 | Flight to San Pedro booked in secret |
| Jan 20, 2026 | Photo shoot and tour arranged as cover |
| Feb 16, 2026 | First quotes from jewelers with Leo |
| Feb 19, 2026 | Ring ordered at Ámbar |
| Mar 2, 2026 | Ring design shared |
| Mar 9, 2026 | Ring delivered |
| Today | The proposal |

The final entry — *Today* — always displays the current device date automatically, so it reflects the real moment whenever the page is opened.

To close the timeline: tap the backdrop, click ✕, or press `Escape`.

---

## Technical Details

- **Single file** — everything lives in `index.html`: HTML, CSS, and JavaScript
- **No dependencies** — no frameworks, no build step, no server required
- **Fonts** — Cormorant Garamond (serif, italic accents) + Montserrat (sans-serif, uppercase labels) via Google Fonts
- **Animations** — CSS keyframes for floating heart, fade-ins, and panel slide-up; canvas-based star field and sparkle particles
- **Responsive** — fully mobile-friendly with fluid typography (`clamp()`) and adaptive grid layouts
- **Day counters** — calculated live from hardcoded milestone dates; refresh every 60 seconds
- **Today's date** — injected via `new Date()` each time the timeline is opened; always current

---

## How to Use

1. Open `index.html` in any modern browser — no internet connection required after fonts load
2. Share it by sending the file directly, or host it on any static file host (GitHub Pages, Netlify, etc.)
3. For the best experience, open it on a phone and hand it to her

---

## Customization

All personal details are in the HTML source:

| What | Where |
|------|-------|
| Names | `sub-msg` div and `yes-msg` div |
| Milestone dates | `dates` array in the `<script>` block |
| Personal message | `yes-msg` div on the Yes page |
| Timeline entries | `#timeline-panel` HTML block |
| Language | Bilingual by default; remove `*-es` elements to go English-only |

---

*Made with love by Félix.*
