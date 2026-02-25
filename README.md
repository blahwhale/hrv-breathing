# HRV 呼吸训练 / HRV Breathing Trainer

A single-file web app for Heart Rate Variability (HRV) breathing training, based on the Lehrer (2000/2013) resonant frequency biofeedback protocol.

**→ Open `index.html` directly in any browser. No server or dependencies needed.**

---

## What It Does

HRV biofeedback training involves breathing at your personal *resonant frequency* — the rate (typically 4.5–6.5 breaths/min) at which your heart rate variability is maximized, creating a state of cardiovascular coherence. Regular practice improves stress resilience, emotion regulation, focus, and sleep quality.

---

## Features

- **10-session structured program** following the Lehrer protocol
- **Session 1 RF Discovery** — guides you through 5 frequencies (6.5 / 6.0 / 5.5 / 5.0 / 4.5 bpm), 2.5 min each, with star-rating to find your resonant frequency
- **Animated breathing circle** — smooth easeInOutSine animation, scales 0.7→1.0 on inhale, reverses on exhale
- **Audio cues** — 440 Hz (inhale) / 330 Hz (exhale) sine tones via Web Audio API
- **20-minute session timer** with cycle counter and progress bar
- **Minimal-guidance mode** (Sessions 8–10) — fades visuals to build internal rhythm
- **91-day calendar heatmap** — GitHub-style practice log
- **LocalStorage persistence** — saves resonant frequency, session progress, and full training history
- **Responsive layout** — works on desktop and mobile

---

## Breathing Timing

| RF | Period | Inhale | Exhale |
|----|--------|--------|--------|
| 6.5 bpm | 9.23 s | 3.69 s | 5.54 s |
| 6.0 bpm | 10.0 s | 4.0 s | 6.0 s |
| 5.5 bpm | 10.91 s | 4.36 s | 6.55 s |
| 5.0 bpm | 12.0 s | 4.8 s | 7.2 s |
| 4.5 bpm | 13.33 s | 5.33 s | 8.0 s |

Inhale : Exhale = 4 : 6 (fixed ratio)

---

## Session Overview

| Session | Focus | Mode |
|---------|-------|------|
| 1 | Resonant Frequency Discovery (RF test) | RF Test |
| 2 | Foundation breathing at your RF | Standard |
| 3 | Smooth, continuous breathing coherence | Standard |
| 4 | Body awareness integration | Standard |
| 5 | Extended reinforcement | Standard |
| 6 | Stress-context application | Standard |
| 7 | Performance & cognitive optimization | Standard |
| 8 | Reduced visual guidance (part 1) | Minimal |
| 9 | Reduced visual guidance (part 2) | Minimal |
| 10 | Independent practice | Minimal |

**Recommended schedule:** 2 sessions/day, 5 weeks (14 sessions/week goal shown in stats).

---

## Tech Stack

- Vanilla HTML5 / CSS3 / JavaScript (ES6+)
- Web Audio API
- `requestAnimationFrame` animation loop
- `localStorage` for persistence
- Zero dependencies, zero build step

---

## Progress Summary

**Status: v1.0 — Complete**

Built in a single session. All 7 implementation phases delivered:

| Phase | Deliverable | Status |
|-------|-------------|--------|
| 1 | HTML skeleton, CSS variables, dark theme, responsive layout | ✅ |
| 2 | Breathing engine — rAF loop, easeInOutSine, 20-min timer | ✅ |
| 3 | 10-session data, teaching cards, session selector | ✅ |
| 4 | Session 1 RF test flow — 5 frequencies, star ratings, result/confirm UI | ✅ |
| 5 | Training log, 91-day calendar heatmap, stats panel | ✅ |
| 6 | Web Audio cues, Session 8–10 minimal-guide mode, hyperventilation warning | ✅ |
| 7 | Animation tuning, mobile layout, references footer | ✅ |

**Single file:** `index.html` — 1,331 lines, ~46 KB

---

## References

- Lehrer, P.M., Vaschillo, E., & Vaschillo, B. (2000). Resonant frequency biofeedback training to increase cardiac variability. *Applied Psychophysiology and Biofeedback*, 25(3), 177–191.
- Lehrer, P.M., et al. (2013). Protocol for Heart Rate Variability Biofeedback Training. *Biofeedback*, 41(3), 98–109.
- Lehrer, P.M. & Gevirtz, R. (2014). Heart rate variability biofeedback: how and why does it work? *Frontiers in Psychology*, 5, 756.
