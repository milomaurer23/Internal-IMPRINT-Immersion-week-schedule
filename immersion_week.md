# Immersion Week Planning — Progress & Next Steps
## NIA REDI · July 2026 · Berkeley, CA

---

## 📌 What This File Is

A human-readable progress doc for the immersion week HTML itinerary project.
The companion `AGENTS.md` file (same folder) is the machine-readable version that
GitHub Copilot CLI automatically loads at session start for persistent AI context.

---

## ✅ What's Been Built

### `innovation_tour.html` — July 21, Cohort 1
The flagship detail card. Fully complete. Features:
- Vertical timeline with 6 stops (Sigma House → Berkeley BART → SSF BART → AbbVie → JLABS → Eli Lilly)
- Transport pills: Uber XL (black), BART Red Line (dark blue), Walk (green)
- 3 timeline sections: Berkeley / South San Francisco / Return to Berkeley
- Duration badges, anchored callout (JLABS), pending callout (Eli Lilly)
- Group cost summary table: 10 travelers, Uber XL × 2 cars, ~$272–330 total, ~$27–33/person
- Clipper Card recommendation: load $20/card (~$23 if buying fresh with $3 card fee)
- Hyperlinks on AbbVie, JLABS SSF, Eli Lilly Gateway Lab
- Pro tip footer about Clipper Card / Apple Pay

### `cohort1_week.html` — Week Hub, Jul 20–26
- 7-day card layout (Mon–Sun)
- Jul 21 is pre-filled with stop summary + inline expand button (loads innovation_tour.html in iframe)
- All other days have skeleton placeholders
- Week nav tabs linking to Cohort 2
- Week summary footer

### `cohort2_week.html` — Week Hub, Jul 27–Aug 2
- 7-day card layout (Sun–Sat)
- All days placeholder — ready for content
- Forest green theme (vs. navy for Cohort 1)
- Week nav tabs linking back to Cohort 1

---

## 📂 File Structure

```
Immersion week planning/
└── Immersion Week #2, July 2026/
    ├── AGENTS.md                    ← Copilot auto-context file
    ├── immersion_week.md            ← This file
    ├── Cohort #1 outgoing/
    │   ├── cohort1_week.html
    │   └── innovation_tour.html
    └── Cohort #2 incoming/
        └── cohort2_week.html
```

---

## 🗓 Day-by-Day Status

### Cohort 1 — Outgoing (Jul 20–26)

| Day | Title | Status | File |
|---|---|---|---|
| Mon Jul 20 | TBD | ⬜ Empty | — |
| **Tue Jul 21** | **Innovation Labs Tour** | ✅ **Complete** | `innovation_tour.html` |
| Wed Jul 22 | TBD | ⬜ Empty | — |
| Thu Jul 23 | TBD | ⬜ Empty | — |
| Fri Jul 24 | TBD | ⬜ Empty | — |
| Sat Jul 25 | Weekend | 🌤 Placeholder | — |
| Sun Jul 26 | Weekend | 🌤 Placeholder | — |

### Cohort 2 — Incoming (Jul 27–Aug 2)

| Day | Title | Status | File |
|---|---|---|---|
| Sun Jul 27 | TBD | ⬜ Empty | — |
| Mon Jul 28 | TBD | ⬜ Empty | — |
| Tue Jul 29 | TBD | ⬜ Empty | — |
| Wed Jul 30 | TBD | ⬜ Empty | — |
| Thu Jul 31 | TBD | ⬜ Empty | — |
| Fri Aug 1 | TBD | ⬜ Empty | — |
| Sat Aug 2 | TBD | ⬜ Empty | — |

---

## 🔜 Next Steps (in priority order)

1. **Fill in remaining Cohort 1 days** — Milo to provide stop details for Mon, Wed, Thu, Fri
2. **Build detail HTML files** for each new day (same pattern as `innovation_tour.html`)
3. **Wire up expand buttons** in `cohort1_week.html` for each new day
4. **Fill in Cohort 2 days** — once Milo has the Cohort 2 schedule
5. **Confirm Eli Lilly appointment** — update pending callout to confirmed once locked
6. **Rename parent folder** to "Immersion Week #2, July 2026" (bash was broken — do in Finder)
7. **Optional:** Add Google Maps links to each stop address
8. **Optional:** Add a master index/landing page that links to both cohort hubs

---

## 🧠 Key Decisions Made

| Decision | Choice | Reason |
|---|---|---|
| BART line | **Red Line** (Richmond–Millbrae) | Verified on bart.gov — Berkeley → SSF is Red, not Yellow |
| Group transport | **Uber XL × 2 cars** | 10 people; XL seats 6, need 2 for full group |
| Itinerary interaction | **Inline iframe expand** | Better UX than new tab; keeps user in the week hub |
| Clipper Card load | **$20/card** | ~$12–14 round trip + buffer; $23 if buying fresh card |
| Per-person cost | **~$27–33** | Uber XL group share + BART round trip |
| File structure | **Separate folders per cohort** | Clean separation, easy to navigate |

---

## 📎 Confirmed Venue Info

| Venue | Address | Website |
|---|---|---|
| Sigma House | 2311 Prospect St, Berkeley, CA | — |
| Downtown Berkeley BART | 2160 Shattuck Ave, Berkeley | bart.gov |
| South San Francisco BART | 1333 Mission Rd, SSF | bart.gov |
| AbbVie | 1000 Gateway Blvd, SSF | abbvie.com |
| JLABS SSF | 329 Oyster Point Blvd, 3rd Fl, SSF | jlabs.jnjinnovation.com |
| Eli Lilly Gateway Lab | 201 Haskins Way, SSF | lilly.com/gateway-labs |

---

## 🔧 Known Issues

- [ ] Folder rename pending (Finder workaround needed while bash is down)
- [ ] Week summary stat "1 of 5 planned" needs updating as days are added
- [ ] Cohort 2 header chip "All Days TBD" needs updating as confirmed

---

*Last updated: April 28, 2026*
