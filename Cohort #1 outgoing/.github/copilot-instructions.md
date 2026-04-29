# NIA REDI Immersion Week — Project Context

## What This Is
Self-contained HTML itinerary cards for NIA REDI fellows, Berkeley/Bay Area, July 2026.
- **Cohort 1 Outgoing** (Jul 20–26): `cohort1_week.html` — navy theme
- **Cohort 2 Incoming** (Jul 27–Aug 2): `cohort2_week.html` — green theme
- Template for all day cards: `innovation_tour.html` (Jul 21, fully built)

## Design System
- Cohort 1 header gradient: `#1a1a2e → #16213e → #0f3460` (navy)
- Cohort 2 header gradient: `#064e3b → #065f46 → #047857` (forest green)
- Transport pills: Uber = `#111` (black) · BART = `#CC0000` (red — matches Red Line) · Walk = `#16a34a` (green)

## Key Facts
- BART line: **Red Line** (Richmond–Millbrae). Never Yellow.
- Group: 10 people → Uber XL × 2 cars (seats 6 each)
- Clipper Card: load $20. Apple/Google Pay avoids the $3 physical card fee.

## Navigation Pattern
Day detail cards expand **inline** via `toggleItinerary(id)` — no new tabs.
Each day card in the week hub has an expand button + `<iframe>` pointing to the detail file.

## Adding a New Day
1. Duplicate `innovation_tour.html`, rename to `[date]_[name].html`
2. Update title, date, summary bar, stops, transport pills, section headers, cost table
3. Wire the expand button + iframe in the week hub
4. Set status chip: `status-planned` (blue) or `status-confirmed` (green)
