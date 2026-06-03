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

### `silverado_tour.html` — July 30, Cohort 2
Specialized memory care visit. Features:
- **Innovation Spotlight:** Dedicated card for the Nexus Program (Therapy Animals & Behavioral Health).
- **Hyperlinks:** Direct links to the official Silverado Belmont Hills website.
- **Logistics:** Optimized BART-to-Uber route via Millbrae Station to bypass bridge traffic.

### `index.html` — Unified Master Hub
- **Tabbed Interface:** Toggle between Cohort 1 (Navy) and Cohort 2 (Green) seamlessly.
- **Agnostic Architecture:** Model-neutral `AGENTS.md` context for use with Gemini, Claude, or Copilot.

---

## 📂 File Structure

```
Immersion week planning/
└── Immersion Week, July 2026/
    ├── AGENTS.md                    ← Persistent Context (AI Assistant reads this)
    ├── immersion_week.md            ← This file (Human-readable progress)
    ├── index.html                   ← Unified Master Itinerary (MAIN HUB)
    ├── Cohort #1 outgoing/
    │   └── innovation_tour.html     ← Jul 21 full detail
    └── Cohort #2 incoming/
        └── silverado_tour.html      ← Jul 30 full detail
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
| Sat Jul 25 | Presentations & Lunch | ⏳ Pending | — |
| Sun Jul 26 | Lunch Celebration | ⏳ Pending | — |

### Cohort 2 — Incoming (Jul 27–Aug 2)

| Day | Title | Status | File |
|---|---|---|---|
| Sun Jul 26 | Arrival & Orientation | ✅ Planned | — |
| Mon Jul 27 | TBD | ⬜ Empty | — |
| Tue Jul 28 | TBD | ⬜ Empty | — |
| Wed Jul 29 | TBD | ⬜ Empty | — |
| Thu Jul 30 | Silverado Belmont Hills | ✅ Complete | `silverado_tour.html` |
| Fri Jul 31 | TBD | ⬜ Empty | — |
| Sat Aug 1 | Weekend | 🌤 Placeholder | — |
| Sun Aug 2 | Weekend | 🌤 Placeholder | — |

---

## 🔜 Next Steps (in priority order)

1. **Fill in remaining Cohort 1 days** — Milo to provide stop details for Mon, Wed, Thu, Fri
2. **Fill in remaining Cohort 2 days** — Milo to provide details for Mon, Tue, Wed, Fri
3. **Build detail HTML files** for each new confirmed day
4. **Clean up directory** — Optionally delete `cohort1_week.html` and `cohort2_week.html` (now deprecated by `index.html`)
5. **Rename parent folder** to "Immersion Week #2, July 2026"
6. **Optional:** Add Google Maps links to each stop address

---

## 🧠 Key Decisions Made

| Decision | Choice | Reason |
|---|---|---|
| Architecture | **Unified Tabbed index.html** | Easier navigation; reduced file duplication |
| AI Context | **Model-Agnostic AGENTS.md** | Ensures portability between Gemini, Claude, and Copilot |
| BART line | **Red Line** (Richmond–Millbrae) | Verified on bart.gov |
| Group transport | **Uber XL × 2 cars** | 10 people total |

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
| Silverado Belmont Hills | 1301 Ralston Ave, Belmont, CA | [Link](https://www.silverado.com/locations/belmont-hills/) |

---

*Last updated: April 29, 2026*
