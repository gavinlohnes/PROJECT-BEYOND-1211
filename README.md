# PROJECT BEYOND

A personal training, nutrition, and health tracker built for one user — me. Designed to fit a specific life: night-shift work, irregular eating windows, narcolepsy, pre-diabetes, an upcoming Zepbound regimen, and a 210 → 165 lb cut.

It's a single-page web app, fully offline-capable, with all data stored locally on the device. No accounts. No servers. No analytics.

🔗 **Live app:** [open here](https://gavinlohnes.github.io/PROJECT-BEYOND-1211/)

---

## What it does

**Daily tab**
- Calorie / protein / step / sleep rings with auto-switching duty-aware targets (off-duty vs on-shift)
- Fasting protocol with a "// JUST ATE" timestamp button and configurable fast duration
- Energy & sleepiness log (1–10 scale + dedicated "sleepy now" button) for narcolepsy tracking
- Body weight and reflection fields tied to the current week

**Push / Pull / Upper tabs**
- Three-day weekly training split with editable exercise lists
- Per-exercise weight / reps / rest / notes
- Auto-suggested next session weight based on whether you hit your rep targets
- Live PR detection with optional synth-blip alert
- One-tap "// FILL FROM LAST" to pre-populate every exercise from the previous matching session
- Built-in plate calculator and 1RM estimator

**Summary tab**
- Weekly weigh-in tracker with running total
- Body weight trend chart (Chart.js)
- Reflection prompts: improvement, hardest part, biggest win, free-form notes
- Week-type tagging (Build / Test / Deload / Recovery) that affects progressive overload logic

**History tab**
- Every saved week, viewable and editable
- Full session detail per week
- CSV export, JSON backup/restore

**Settings ([BC] button in header)**
- Off-duty + on-shift calorie and protein targets
- Fast duration, weight increment, target reps per set
- Optional streak counter, optional PR alert sound

---

## Stack

- Plain HTML, CSS, JavaScript — no build step, no framework
- Chart.js for trend graphs (loaded from CDN, cached by service worker)
- localStorage for all persistence
- Service worker for offline support
- Inline SVG icon, inline web app manif
