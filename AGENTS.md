# 🧠 AGENTS.md — Persistent Project Context
## NIA REDI · Immersion Week Planning · July 2026

> This file is intended to be read by AI assistants (Gemini, Copilot, Claude, etc.) at session start.
> It provides full context on this project to ensure consistency across different platforms and models.

---

## Who is the user?
Milo — organizing NIA REDI immersion week programming for two cohorts in Berkeley/Bay Area, July 2026. Prefers clean, modern HTML itinerary cards.

## Project: What are we building?
A set of **self-contained HTML itinerary files** for a two-week immersion program:
- **`index.html`:** Landing hub linking to both cohort week files.
- **`Cohort #1 outgoing/cohort1_week.html`:** Week hub for Jul 20–26 (dark navy theme), 7-day card layout.
- **`Cohort #2 incoming/cohort2_week.html`:** Week hub for Jul 27–31 (forest green theme), 7-day card layout.
- **`Cohort #1 outgoing/innovation_tour.html`:** Full detail for July 21 (Innovation Labs Tour ✅).
- **`Cohort #2 incoming/silverado_tour.html`:** Full detail for July 30 (Silverado Belmont Hills ✅).
- **`Cohort #2 incoming/frank_residences.html`:** Frank Residences detail card (in progress).

Each cohort hub shows all 7 days as cards with status chips. Planned days show a stop-by-stop summary with an **inline expand button** (loads detail HTML in an iframe — no new tab).

---

## File Structure

```
Immersion week planning/
└── Immersion Week, July 2026/
    ├── AGENTS.md                        ← YOU ARE HERE (AI Assistant reads this)
    ├── immersion_week.md                ← human-readable progress doc
    ├── index.html                       ← Landing hub → links to cohort week files
    ├── Cohort #1 outgoing/
    │   ├── cohort1_week.html            ← Week hub Jul 20–26 (dark navy)
    │   └── innovation_tour.html         ← Jul 21 full detail: Innovation Labs Tour ✅
    └── Cohort #2 incoming/
        ├── cohort2_week.html            ← Week hub Jul 27–31 (forest green)
        ├── silverado_tour.html          ← Jul 30 full detail: Silverado Belmont Hills ✅
        └── frank_residences.html        ← Frank Residences detail (in progress)
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

### Cohort 2 (Jul 27–31)
| Day | Status | Notes |
|---|---|---|
| Sun Jul 27 | ⬜ TBD | Possible arrival/orientation |
| Mon Jul 28 | ⬜ TBD | No details yet |
| Tue Jul 29 | ⬜ TBD | No details yet |
| Wed Jul 30 | ⬜ TBD | No details yet |
| Thu Jul 31 | ✅ **DONE** | silverado_tour.html fully built |
| Fri Aug 1 | 🔧 WIP | frank_residences.html (departure placeholder) |

---

## How to Add a New Day

When Milo gives you details for a new day, here is the workflow:

1. **Create a new detail HTML file** (e.g. `july22_tour.html`) modeled after `innovation_tour.html`
   - Copy the full structure: header, summary bar, timeline, transport pills, cost summary, pro tip, footer
   - Update BART line to **Red Line** if BART is used
   - Add hyperlinks to all venue names
   - Add group cost table for 10 people / Uber XL × 2 cars

2. **Update `cohort1_week.html`** (or `cohort2_week.html`) for that day's card:
   - Replace the placeholder block with a stop-list summary
   - Change status chip from `status-tbd` → `status-planned`
   - Add transport micro-pills
   - Add inline expand button pointing to the new detail file:
     ```html
     <button class="expand-btn" onclick="toggleItinerary('DAYID')">▼ Expand Full Itinerary</button>
     <div id="itinerary-expand-DAYID" class="itinerary-expand">
       <iframe src="../Cohort #N cohortname/FILENAME.html" class="itinerary-frame"></iframe>
     </div>
     ```
   - Update the week summary footer counts

3. **Update this AGENTS.md** — mark the day as ✅ DONE in the status table

---

## Known Issues / TODOs

- [ ] `frank_residences.html` — departure placeholder, needs full detail filled in
- [ ] `cohort1_week.html` summary bar: update "1 of 5" count as days are confirmed
- [ ] `cohort2_week.html` header chip: update "⬜ All Days TBD" as days are confirmed
- [ ] Verify Eli Lilly Gateway Lab appointment — update pending callout once confirmed
- [ ] Fill in Cohort 2 schedule details (Mon–Wed, Jul 28–30)
- [ ] Consider adding Google Maps links for each stop address
- [ ] `NIA-REDI-Immersion-Week-July-2026/` subfolder inside this repo is an **untracked orphan** (incomplete Copilot reorganization, never committed, missing silverado + frank files) — delete via Finder when convenient

---

*Last updated: June 11, 2026 · Merged from fork by Copilot CLI*
