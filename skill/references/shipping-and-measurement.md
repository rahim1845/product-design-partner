# Shipping & Measurement — Phases 6–7

Load for: handoff, design QA, rollout, guardrails, post-launch measurement, retention analysis, readouts.

## Contents
1. Handoff & design QA
2. Rollout strategy & guardrails
3. Measurement frameworks (HEART, retention)
4. Post-launch readout (worked example)
5. Closing the research loop

---

## 1. Handoff & design QA

- **Partnership over throw-over-the-wall:** pair-review during build, not after; one source of truth (Figma or code — pick one).
- **Spec per flow, in one linked doc:** tokens, components, all states (default/empty/loading/error/success/partial/offline/slow), interactions, copy, a11y notes, analytics events.
- **Annotated redlines** on edge-case screens specifically.
- **Design QA** against the built product, ticketed with Nielsen severity 0–4 (see validation-and-math §4). Done = shipped *and accepted*.
- **Figma hygiene:** named layers, variant components, auto-layout where structure matters, tokens not hard-coded values.

## 2. Rollout strategy & guardrails

Pick by risk: internal dogfood → closed beta (opt-in, ~100 users) → percentage rollout (1 → 5 → 25 → 100%) → full. **Feature flags for kill-switch on any major change — non-negotiable.** Dark launch (shipped but hidden) validates infra before exposure.

**Guardrails: define numeric thresholds BEFORE rollout, never after.** Illustrative defaults to adapt per product — these are starting points, not industry standards:

- Activation: no worse than baseline −2 pp
- Week-1 retention: no worse than −3 pp
- Error rate / p95 latency: no worse than +20%
- Support volume: no spike >50% over 7-day trailing mean

Exit criteria for ship: design QA passes; a11y audit passes (WCAG 2.2 AA); analytics instrumented *before* launch, not "fast-follow"; rollback triggers written with numbers.

## 3. Measurement frameworks

**Google HEART (Rodden et al.):**

| Dimension | Example metric |
|---|---|
| Happiness | CSAT, SUS, NPS (with caveats) |
| Engagement | Core-action frequency, sessions/user |
| Adoption | New users activating a feature |
| Retention | Week-N curves |
| Task success | Completion rate, error rate, time on task |

Pair each with Goals → Signals → Metrics to keep vanity out.

**SUS** (System Usability Scale, Brooke): 10-item questionnaire, 0–100; ~68 is the published average across studies (Sauro). **SEQ** (Single Ease Question): 1–7 post-task; ~5.5 is the common benchmark for "easy enough."

**Activation:** define as the specific moment of first core value (sent first message, invited a teammate). Track time-to-activation; if time-to-first-value is long relative to category peers, activation is usually the most leveraged fix.

**Retention windows:** D1 (next-day return), D7 (catches tried-it-once), D30 (curve flattening above zero = PMF signal; flat at zero = no PMF). **Lness (e.g. L28):** distribution of days-active out of the last 28 — shows intensity, not just survival; a shift toward higher buckets means deepening habit.

**Category benchmarks** (directional, from public Mixpanel/Amplitude/Lenny Rachitsky reports — per SKILL.md principle 10, search for current data before using these in a real decision):

| Category | D1 | D7 | D30 |
|---|---|---|---|
| B2B SaaS | 30–50% | 15–25% | 10–20% |
| Consumer social | 30–60% | 15–30% | 8–15% |
| E-commerce | 10–25% | 5–15% | 3–10% |
| Mobile games | 25–40% | 10–20% | 3–8% |
| Fintech | 20–40% | 15–25% | 10–20% |

## 4. Post-launch readout — worked example (numbers illustrative)

> **Change:** replaced blank dashboard with 3-step starter checklist for new signups.
> **Hypothesis:** week-1 activation 34% → ≥42% at p<0.05.
> **Result:** 34% → 41.3% (p=0.02, n=1,180/arm). Below target, statistically significant.
> **Guardrails:** week-4 retention 22% → 20% (−2 pp, inside −3 pp tolerance). Tickets flat.
> **Verdict:** partial win. Investigate whether checklist users complete fewer high-value first actions than organic explorers.
> **Next bet:** single-goal starter ("invite one teammate") vs 3-step checklist.
> **Won't do:** roll back — the lift is real, the slip tolerable.

The readout's honesty matters more than its outcome. "It didn't move and here's what we learned" is a complete, respectable readout.

## 5. Closing the loop

Every research/measurement round ends with: what we learned / what we'll do / what we won't do and why — shared where the team actually reads. Update decisions.md. This separates learning organizations from research theater.

## Go deeper
Rodden et al. (HEART) · Sauro & Lewis · Croll & Yoskovitz *Lean Analytics* · Amplitude/Mixpanel public benchmark reports.
