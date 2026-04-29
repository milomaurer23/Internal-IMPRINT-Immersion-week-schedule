# 🧠 AGENTS.md — Copilot Persistent Context
## NIA REDI · Immersion Week Planning · July 2026

> This file is automatically read by GitHub Copilot CLI at session start.
> It gives Copilot full context on this project so no re-explanation is needed.

---

## Who is the user?
Milo — organizing NIA REDI immersion week programming for two cohorts in Berkeley/Bay Area, July 2026. Prefers clean, modern HTML itinerary cards. Is working out of the folder structure below.

## Project: What are we building?
A set of **self-contained HTML itinerary files** for a two-week immersion program:
- **Week 1 (Jul 20–26):** Cohort 1 — Outgoing
- **Week 2 (Jul 27–Aug 2):** Cohort 2 — Incoming

Each week has a **hub file** (`cohort1_week.html` / `cohort2_week.html`) showing all 7 days as cards with status chips. Planned days show a stop-by-stop summary with an **inline expand button** that loads the full detail card inside an iframe — no new tab needed.

Full detail cards (like `innovation_tour.html`) are **boarding-pass style** vertical timeline cards with:
- Transport pills (Uber = black, BART = dark blue #003DA5, Walk = green)
- Duration badges, anchored/pending callouts
- Group cost summary table (10 travelers, Uber XL × 2 cars)
- Clipper Card recommendation
- Pro tip footer
- Hyperlinks on venue names

---

## File Structure

```
Immersion week planning/
└── Immersion Week #2, July 2026/       ← parent folder (may still be named without #2 if rename failed)
    ├── AGENTS.md                        ← YOU ARE HERE (Copilot auto-reads this)
    ├── immersion_week.md                ← human-readable progress doc
    ├── Cohort #1 outgoing/
    │   ├── cohort1_week.html            ← Week hub Jul 20–26 (dark navy theme)
    │   └── innovation_tour.html         ← Jul 21 full detail: Innovation Labs Tour ✅
    └── Cohort #2 incoming/
        └── cohort2_week.html            ← Week hub Jul 27–Aug 2 (forest green theme)
```

---

## Design System (always follow these)

| Element | Spec |
|---|---|
| Card background | `#ffffff` on `#f0f2f5` page |
| Header gradient (Cohort 1) | `#1a1a2e → #16213e → #0f3460` (dark navy) |
| Header gradient (Cohort 2) | `#064e3b → #065f46 → #047857` (forest green) |
| Uber pill | `background: #111111` |
| BART pill | `background: #003DA5` |
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
| Sat Jul 25 | 🌤 Weekend | Placeholder |
| Sun Jul 26 | 🌤 Weekend | Placeholder |

### Cohort 2 (Jul 27–Aug 2)
| Day | Status | Notes |
|---|---|---|
| Sun Jul 27 | ⬜ TBD | Possible arrival/orientation |
| Mon Jul 28 | ⬜ TBD | No details yet |
| Tue Jul 29 | ⬜ TBD | No details yet |
| Wed Jul 30 | ⬜ TBD | No details yet |
| Thu Jul 31 | ⬜ TBD | No details yet |
| Fri Aug 1 | ⬜ TBD | No details yet |
| Sat Aug 2 | ⬜ TBD | Possible departure day |

---

## How to Add a New Day

When Milo gives you details for a new day, here is the workflow:

1. **Create a new detail HTML file** (e.g. `july22_tour.html`) modeled after `innovation_tour.html`
   - Copy the full structure: header, summary bar, timeline, transport pills, cost summary, pro tip, footer
   - Update BART line to **Red Line** if BART is used
   - Add hyperlinks to all venue names
   - Add group cost table for 10 people / Uber XL × 2 cars

2. **Update `cohort1_week.html`** (or cohort2) for that day's card:
   - Replace the placeholder block with a stop-list summary
   - Change status chip from `status-tbd` → `status-planned`
   - Add transport micro-pills
   - Add the expand button pointing to the new detail file:
     ```html
     <button class="expand-btn" id="expand-btn-DAYID" onclick="toggleItinerary('DAYID')">
       <span id="expand-arrow-DAYID">▼</span> Expand Full Itinerary
     </button>
     <div id="itinerary-expand-DAYID" class="itinerary-expand">
       <iframe src="FILENAME.html" class="itinerary-frame" title="DAY TITLE"></iframe>
     </div>
     ```
   - Update the week summary footer counts

3. **Update this AGENTS.md** — mark the day as ✅ DONE in the status table

---

## Known Issues / TODOs

- [ ] Folder rename: "Immersion Week, July 2026" → "Immersion Week #2, July 2026" (bash was broken at time of creation — do manually in Finder or retry next session)
- [ ] cohort1_week.html summary bar still says "3 Labs Confirmed" / "1 of 5" — update as days are filled in
- [ ] cohort2_week.html header chip says "⬜ All Days TBD" — update as days are confirmed
- [ ] Verify Eli Lilly Gateway Lab appointment once confirmed
- [ ] Consider adding a Google Maps link for each stop address

---

## Copilot CLI Tips for This Project

- **`/init`** — initializes instruction files for a repo (useful if this becomes a git repo)
- **`/skills`** — check available skills that could help (e.g. PDF export)
- **`/share`** — export this session to markdown or HTML gist
- **`@ mention`** files directly: e.g. `@innovation_tour.html` to bring a file into context
- **`! shell command`** — run a quick shell command inline (e.g. `! open cohort1_week.html`)
- **AGENTS.md is auto-loaded** from cwd — keep this file updated as the project evolves
- The `$HOME/.copilot/copilot-instructions.md` file sets *global* instructions across all projects

---

*Last updated: April 28, 2026 · Built with GitHub Copilot CLI (Claude Sonnet 4.6)*
