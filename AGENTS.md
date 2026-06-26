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
- **`Cohort #2 incoming/frank_residences.html`:** Frank Residences detail card (done ✅).

Each cohort hub shows all 7 days as cards with status chips. Planned days show a stop-by-stop summary with an **inline expand button** (loads detail HTML in an iframe — no new tab).

---

## File Structure

```
Immersion week planning/
└── Immersion Week, July 2026/
    ├── AGENTS.md                        ← YOU ARE HERE (AI Assistant reads this)
    ├── immersion_week.md                ← human-readable progress doc
    ├── index.html                       ← Landing hub → links to cohort week files
    ├── clipper_card_cost_breakdown.html ← Interactive Clipper presentation slide deck (talk) ✅
    ├── clipper_card_cost_breakdown.md   ← Presentation outline & speaker script (talk text) ✅
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

- **BART line: RED LINE** (Richmond–Millbrae). Downtown Berkeley BART ↔ Millbrae BART.
- **Group size: Cohort 1 = 10 travelers · Cohort 2 = 14 travelers** (updated June 2026 — do not use the old "11 travelers" or "15 travelers" figures)
- **Uber fleet-sizing rule (Milo's rule, confirmed June 2026):** fill Uber XL cars (6 seats each) first; if the remainder after filling XLs is ≤4, cover it with **one regular Uber** (4 seats); if the remainder is 5–6, add **another XL** instead.
  - 10 people → 2× Uber XL (12 seats, 2 spare) — no regular needed
  - 14 people → 2× Uber XL + 1× regular Uber (16 seats, 2 spare) — this covers the Glen Park and Millbrae legs
- **BART fares are 2026 estimates** (BART fares rose 6.2% system-wide on Jan 1, 2026 — confirmed via official BART press release). bart.gov blocks automated fetches (403 on live schedule + fare-calculator pages, including static PDFs), so exact fares could not be pulled live — **recommend a manual spot-check at bart.gov/tickets/calculator** before finalizing a budget for distribution.
  - DBRK ↔ South San Francisco: $6.15 one-way (Clipper official fare, confirmed June 2026)
  - DBRK ↔ Millbrae: $6.95 one-way (Clipper official fare, confirmed June 2026)
  - DBRK ↔ Glen Park: $5.70 outbound / $6.00 return ($11.70 round-trip Clipper official fare, confirmed June 2026)
  - DBRK ↔ Embarcadero: $5.30 one-way / $10.60 round-trip (Clipper official fare, confirmed June 2026)
- **Clipper Card budget details:** Load **$55.00** for the 10 Dual-Cohort cards and **$41.00** for the 4 Cohort-2-only cards. This leaves a **~$5.00** buffer left on each card after all planned BART trips (exactly $6.50 buffer for dual-cohort and $4.80 for Cohort-2-only). Physical card stock costs **$3.00** per card (for a grand total of **$756.00** with fees, or **$714.00** if using Apple/Google Pay mobile wallets to avoid the fee).
- **Uber per-car estimates (one-way):** Sigma House ↔ Downtown Berkeley BART (~7 min) — XL ~$11–14, regular ~$8–10. SSF BART ↔ JLABS (~10 min) — XL ~$14–17, regular ~$10–12. Glen Park BART ↔ Frank Residences (~8 min) — XL ~$11–14, regular ~$8–10. Millbrae BART ↔ Silverado Belmont Hills (~12 min) — XL ~$19–24, regular ~$14–17 (Silverado provides Uber vouchers for this leg — confirm voucher amount with Marisa Taylor to net against this cost). PresidiGo shuttle (Embarcadero → Presidio) is FREE.

---

## Jul 21 — J&J JLABS Tour (FULLY BUILT ✅)

> **Updated June 2026:** AbbVie and Eli Lilly tours **REMOVED** — not happening; exploring alternatives. **J&J / JLABS SSF is now the only stop.** Do NOT re-add AbbVie or Eli Lilly.

| Stop | Time | Address | Notes |
|---|---|---|---|
| Sigma House | Depart 9:20 AM | 2311 Prospect St, Berkeley | Home base |
| Downtown Berkeley BART | ~9:30 AM | 2160 Shattuck Ave | Red Line southbound ~9:36 AM |
| South San Francisco BART | ~10:35 AM | 1333 Mission Rd, SSF | SamTrans Route 130 bus from here (~18 min) |
| JLABS SSF (J&J) | 11:00 AM–2:00 PM | 329 Oyster Point Blvd 3rd Fl | **ANCHORED · only stop** · [jnjinnovation.com](https://jlabs.jnjinnovation.com/locations/jlabs-ssf) |
| Return to Berkeley | ~3:15 PM | — | Reverse route · South San Francisco BART → Berkeley BART |

Group cost ~$145–151 · per person ~$15.

---

## Status of All Days

### Cohort 1 (Jul 20–26)
| Day | Status | Notes |
|---|---|---|
| **Mon Jul 20** | ✅ **PLANNED** | Arrival & Orientation + **Chima Payer Group 10 AM–12 PM @ Sigma House** (no travel) |
| **Tue Jul 21** | ✅ **DONE** | innovation_tour.html (J&J JLABS only — AbbVie + Eli Lilly removed) |
| Wed Jul 22 | ⬜ TBD | No details yet |
| Thu Jul 23 | ⬜ TBD | No details yet |
| Fri Jul 24 | ⬜ TBD | No details yet |
| Sat Jul 25 | ⏳ **PENDING** | Presentations & Lunch Celebration |
| Sun Jul 26 | ⏳ **PENDING** | Lunch Celebration (Backup) |

### Cohort 2 (Jul 26–Aug 2) — site-visit dates per Milo (June 2026)
| Day | Status | Notes |
|---|---|---|
| Sun Jul 26 | ✅ PLANNED | Arrival & Orientation @ Sigma House |
| **Mon Jul 27** | ✅ **DONE** | **Frank Residences** 12 PM · frank_residences.html · BART → Glen Park + Uber XL/regular (return has Muni 52 option) |
| **Tue Jul 28** | ✅ **DONE** | **Institute on Aging Adult Day Center** 2 PM · institute_on_aging.html · BART → Embarcadero + free PresidiGo shuttle (closes 3 PM) |
| **Wed Jul 29** | ✅ **DONE** | **Silverado Belmont Hills** 9 AM · silverado_tour.html · BART → Millbrae + Uber XL/regular (vouchers avail · explicit 11:19 AM Richmond BART train) |
| Thu Jul 30 | ⬜ TBD | No details yet (Silverado MOVED off this date) |
| Fri Jul 31 | ⬜ TBD | No details yet |
| Sat Aug 1 / Sun Aug 2 | 🌤 Weekend | Departure / wrap-up |

> **Date note:** the site-visit tracking sheet listed Silverado=Jul27 / Frank=Jul28 / IOA=Jul29, but Milo confirmed the correct mapping is **Frank=Jul27, IOA=Jul28, Silverado=Jul29**. Use these.

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

- [x] ~~`frank_residences.html` departure placeholder~~ — DONE, full BART+Uber route built (Jul 27)
- [x] ~~`cohort2_week.html` header chip "All Days TBD"~~ — now "3 Site Visits Confirmed"
- [x] ~~Eli Lilly / AbbVie~~ — REMOVED from Jul 21; J&J only (do not re-add)
- [x] ~~Fill in Cohort 2 schedule details~~ — Frank/IOA/Silverado built with travel charted
- [ ] Confirm BART/Uber travel-time + cost estimates against live schedules before printing (current figures are planning estimates)
- [ ] Fill Cohort 1 Wed–Fri (Jul 22–24) and Cohort 2 Thu–Fri (Jul 30–31)
- [ ] Consider adding Google Maps links for each stop address
- [ ] `NIA-REDI-Immersion-Week-July-2026/` subfolder inside this repo is an **untracked orphan** (incomplete Copilot reorganization, never committed, missing silverado + frank files) — delete via Finder when convenient

---

---

## Site Visit Itinerary — Formatting Spec (template, reference only)

When building a new site-visit detail page or inline chat widget, follow this structure exactly.

### Title block
- Page title: `[Activity type] — [Facility name]`
- Subtitle: `[Day, Month DD, YYYY]`
- Pills: `Origin → Destination · Transport mode · # travelers · Depart [time] · Return ~[time]`

### Travel legs (outbound and return)
Each leg:
```
[Time]
[Location name]
[Full street address, City, State ZIP]
[Mode badge] [Transport description] · [duration] · [cost if applicable]
```
- Never skip the full address on any leg
- Every mode change (BART → Uber, Muni → walk) is its own leg — never combine two modes in one entry
- Badge colors: BART = blue · Uber/rideshare = amber · Walk = gray · Muni/bus = green
- BART badges show exact Clipper fare per person AND group total (fare × # travelers)
- Uber badges show vehicle config (e.g. 2 XL + 1 regular), estimated duration, estimated group cost range
- Walk badges show estimated minutes
- If there's an alternate return mode (Muni OR Uber), show both badges on the same leg
- Every leg shows both depart AND arrive times

### Visit card
- Facility name
- Time range + duration (e.g. `12:00 PM – 2:30 PM · 2.5 hrs`)
- Full address
- Confirmed / Unconfirmed status badge
- 2–3 sentence description of what scholars will observe
- Contacts: [Name(s)]

### Budget table — exactly three sections
1. **BART fares** — one row per direction; columns: Leg · Mode · Rate (per person) · Total (rate × # travelers); show subtotal
2. **Uber fares** — one row per leg (outbound + return separately); columns: Leg · Vehicle config · Rate per car · Total range; label "surge not included"; show subtotal
3. **Optional legs** (e.g. walk-or-Uber segments) — show the Uber cost if taken and note that walking is free

Then two Grand Total rows: walking-optional-leg scenario, and Uber-all-legs scenario.
Footer note: what walking saves, that Clipper fares are exact (not estimates), Uber estimates may vary ±20%.

### Summary cells (3 across)
Per-person cost (walking scenario) · Per-person cost (Uber all legs) · BART round trip per person

### General rules
- Every location needs a full street address — never just a neighborhood/station name
- Never write "TBD" without a follow-up note on what's pending and who owns it
- Flag unconfirmed items with a visible warning badge
- All fares must be sourced or labeled as estimates — never present a guess as confirmed
- BART fares: official published Clipper rates, not estimates. Uber fares: always a range (e.g. $30–38), never a single number
- Group size stated once at the top, carried through every calculation
- Walking alternatives always called out explicitly — never assume everyone Ubers

### Input needed to format a new visit
Facility name + address · visit date + time window · depart location + address · group size · transport mode(s) · confirmed contacts · known fare/cost data (or flag unknown)

---

*Last updated: June 25, 2026 · Cohort sizes corrected (10/14); SamTrans bus on July 21; Muni 52 and Millbrae 11:19 AM return routed.*
