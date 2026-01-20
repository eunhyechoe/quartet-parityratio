# Quartet Parity Ratio

This script estimates an individual's quartet parity ratio (horizontal/vertical distance ratio for perceptual equality) using a psychophysics experiment with two phases (Genc et al., 2011). All quartet elements are positioned on an iso-eccentric circle, ensuring constant eccentricity across conditions while varying the horizontal-to-vertical distance ratio (Choe et al., *in prep*).

Reference:
Choe, Cavanagh, &amp; Tse (*in preparation*). Increasing within-hemifield matching with eccentricity in quartets apparent motion.
Associated abstract: VSS 2025 (https://doi.org/10.1167/jov.25.9.2364)

---

## Phase 1: Method of Limits

Aim to identify the threshold at which the perceived motion direction changes as the quartet aspect ratio is incrementally varied, with all elements positioned on an iso-eccentric circle. Participants fixate on a central dot throughout the trial, and press the **space bar** as soon as a change in perceived motion direction is detected.

- Practice trials: 4
- Runs: 2
- Trials per run: 10 (total 20 trials)
- Two sweep directions are used:
  - Ascending (vertical to horizontal)
  - Descending (horizontal to vertical)

## Phase 2: Method of Constant Stimuli

Aim to measure perceptual responses across fixed aspect ratios centered on the Phase 1 threshold and estimate a psychometric function, the point of subjective equality (PSE). In contrast to Phase 1, each trial presents a single quartet stimulus with a fixed aspect ratio. Participants maintain fixation during stimulus presentation. After stimulus offset, report perceived motion direction: **V** = vertical motion, **H** = horizontal motion.

- Runs: 4
- Trials per run: 80 (total 320 trials)

---

## Global / Screen Configuration

- **Stimulus geometry**
  - Circle diameter: `6 dva`
  - Square size: `1.0 dva`
  - Fixation dot radius: `0.1 dva`
 
- **Colors**
  - Background: `[-0.5, -0.5, -0.5]` (dark gray)
  - Square: `[0.5, 0.5, 0.5]` (light gray)
  - Fixation: red (feedback: green overlay)

- **Monitor presets**
  - should specify `viewing distance (cm)`, `width (cm)`, `pixel resolution`, `refresh rate (Hz)`, `screen index`.

---

## Data Output and Logging

- Creates a subject folder: `{participant}_SubjData/{expName}/`
- Subfolders:
  - `Logging/` : `.log`
  - `Output/` : phase CSV outputs + figures + summary `.md` and `.html`

- Output files:
  - Phase 1 CSV: `{outFileName}_p1.csv`
  - Phase 2 CSV: `{outFileName}_p2.csv`
  - Summary:
    - Markdown: `{baseFileName}_summary.md`
    - HTML: `{baseFileName}_summary.html`
    - Figures: density plots (Phase 1) and psychometric curves (Phase 2)

---
