# 🧠 AGENTS.md — Persistent Project Context
## NIA REDI · Immersion Week Planning · July 2026

> This file is intended to be read by AI assistants (Gemini, Copilot, Claude, etc.) at session start.
> It provides full context on this project to ensure consistency across different platforms and models.

---

## Who is the user?
Milo — organizing NIA REDI immersion week programming for two cohorts in Berkeley/Bay Area, July 2026. Prefers clean, modern HTML itinerary cards.

## Project: What are we building?
A set of **self-contained HTML itinerary files** for a two-week immersion program:
- **index.html:** The unified week hub featuring both Cohort 1 and Cohort 2 itineraries with a tabbed interface.
- **innovation_tour.html:** Full detail for July 21 (Cohort 1).
- **silverado_tour.html:** Full detail for July 30 (Cohort 2).

Each cohort has a **tabbed view** in `index.html` showing all 7 days as cards with status chips. Planned days show a stop-by-stop summary with a link to the full detail card.

---

## File Structure

```
Immersion week planning/
└── Immersion Week, July 2026/
    ├── AGENTS.md                        ← YOU ARE HERE (AI Assistant reads this)
    ├── immersion_week.md                ← human-readable progress doc
    ├── index.html                       ← Unified Hub for both cohorts
    ├── Cohort #1 outgoing/
    │   ├── innovation_tour.html         ← Jul 21 full detail: Innovation Labs Tour ✅
    │   └── cohort1_week.html            ← (DEPRECATED)
    └── Cohort #2 incoming/
        ├── silverado_tour.html          ← Jul 30 full detail: Silverado Belmont ✅
        └── cohort2_week.html            ← (DEPRECATED)
```

---

## Design System (always follow these)

| Element | Spec |
|---|---|
| Card background | `#ffffff` on `#f0f2f5` page |
| Header gradient (Cohort 1) | `#1a1a2e → #16213e → #0f3460` (dark navy) |
| Header gradient (Cohort 2) | `#064e3b → #065f46 → #047857` (forest green) |
| Uber pill | `background: #111111` |
| BART pill | background: #CC0000 (Red Line) |
| Walk pill | `background: #16a34a` |
| Anchored callout | green `#f0fdf4` border `#22c55e` |
| Pending callout | red `#fff1f2` border `#f43f5e` |
| Font | `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif` |
| Border radius (cards) | `20px` outer, `12px` inner elements |

---

## Confirmed Facts (verified, do not change)

- **BART line: RED LINE** (Richmond–Millbrae). Downtown Berkeley BART → South San Francisco BART. Confirmed via bart.gov live schedule. NOT Yellow Line.
- **Group size:** 10 travelers
- **Transport:** Uber XL (seats 6) → need **2 cars** for 10 people
- **BART fare:** ~$6–7 per person one-way, ~$12–14 round trip
- **Clipper Card recommendation:** Load $20/card. Physical card costs ~$3 at station. Suggest Apple/Google Pay to avoid the fee.
- **Uber XL estimates:** Berkeley → Berkeley BART ~$20–25, SSF BART → AbbVie ~$18–22, JLABS → Eli Lilly ~$20–26

---

## Jul 21 — Innovation Labs Tour (FULLY BUILT ✅)

| Stop | Time | Address | Notes |
|---|---|---|---|
| Sigma House | Depart 7:50 AM | 2311 Prospect St, Berkeley | Home base |
| Downtown Berkeley BART | ~7:57 AM | 2160 Shattuck Ave | Red Line southbound ~8:00 AM |
| SSF BART | ~8:48 AM | 1333 Mission Rd, SSF | Uber from here |
| AbbVie | 9:00–10:45 AM | 1000 Gateway Blvd, SSF | 1h 45min · [abbvie.com](https://www.abbvie.com) |
| JLABS SSF | 11:00 AM–2:00 PM | 329 Oyster Point Blvd 3rd Fl | **ANCHORED** · [jnjinnovation.com](https://jlabs.jnjinnovation.com/locations/jlabs-ssf) |
| Eli Lilly Gateway Lab | 2:15–5:00 PM | 201 Haskins Way, SSF | **PENDING CONFIRMATION** · [lilly.com](https://www.lilly.com/gateway-labs) |

---

## Status of All Days

### Cohort 1 (Jul 20–26)
| Day | Status | Notes |
|---|---|---|
| Mon Jul 20 | ⬜ TBD | No details yet |
| **Tue Jul 21** | ✅ **DONE** | innovation_tour.html fully built |
| Wed Jul 22 | ⬜ TBD | No details yet |
| Thu Jul 23 | ⬜ TBD | No details yet |
| Fri Jul 24 | ⬜ TBD | No details yet |
| Sat Jul 25 | ⏳ **PENDING** | Presentations & Lunch Celebration |
| Sun Jul 26 | ⏳ **PENDING** | Lunch Celebration (Backup) |

### Cohort 2 (Jul 27–Aug 2)
| Day | Status | Notes |
|---|---|---|
| Sun Jul 26 | ✅ **DONE** | Arrival & Orientation |
| Mon Jul 27 | ⬜ TBD | No details yet |
| Tue Jul 28 | ⬜ TBD | No details yet |
| Wed Jul 29 | ⬜ TBD | No details yet |
| Thu Jul 30 | ✅ **DONE** | silverado_tour.html fully built |
| Fri Jul 31 | ⬜ TBD | No details yet |
| Sat Aug 1 | ⬜ TBD | Possible departure day |
| Sun Aug 2 | ⬜ TBD | Possible departure day |

---

## How to Add a New Day

When Milo gives you details for a new day, here is the workflow:

1. **Create a new detail HTML file** (e.g. `july22_tour.html`) modeled after `innovation_tour.html`
   - Copy the full structure: header, summary bar, timeline, transport pills, cost summary, pro tip, footer
   - Update BART line to **Red Line** if BART is used
   - Add hyperlinks to all venue names
   - Add group cost table for 10 people / Uber XL × 2 cars

2. **Update index.html** for that day's card:
   - Replace the placeholder block with a stop-list summary
   - Change status chip from `status-tbd` → `status-planned`
   - Add transport micro-pills
   - Update the week summary footer counts

3. **Update this AGENTS.md** — mark the day as ✅ DONE in the status table

---

## Known Issues / TODOs

- [ ] Folder rename: "Immersion Week, July 2026" → "Immersion Week #2, July 2026" (bash was broken at time of creation — do manually in Finder or retry next session)
- [ ] index.html summary bar still says "3 Labs Confirmed" / "1 of 5" — update as days are filled in
- [ ] index.html cohort 2 header chip says "⬜ All Days TBD" — update as days are confirmed
- [ ] Verify Eli Lilly Gateway Lab appointment once confirmed
- [ ] Consider adding a Google Maps link for each stop address

---

*Last updated: April 29, 2026 · Built with AI Collaboration*
