# Validation & Math — Phase 5, Critique Mode

Load for: usability testing, experiments, A/B, PMF measurement, heuristic evaluation, design critique, all statistics.

## Contents
1. Usability testing + the 5-user math
2. Quick tests (5-second, first-click, preference)
3. A/B testing with sample-size math
4. Heuristic evaluation & cognitive walkthrough
5. Usability laws (critique vocabulary)
6. Hypothesis-driven experiments
7. PMF signal (Sean Ellis)
8. IA validation (card sorting, tree testing)

---

## 1. Usability testing

5 users per segment per round (Nielsen). Tasks as scenarios, not instructions. Think-aloud. Moderated for *why*, unmoderated for scale. Never test your own team. "They said they liked it" is not success.

**The math (Nielsen & Landauer, 1993):** P(found) = 1 − (1 − L)^N, with L ≈ 0.31 empirically.

| N users | % of problems found |
|---|---|
| 1 | 31% |
| 3 | 67% |
| 5 | **~85%** |
| 10 | ~97% |
| 15 | ~99% |

Takeaway: 5 is the diminishing-returns inflection. More rounds with fewer users beats fewer rounds with more. Test plan template in templates.md.

---

## 2. Quick tests

- **5-second test:** show a screen 5s; ask what it is and what they'd do. Measures clarity.
- **First-click test:** first click predicts task success ~87% of the time (Bob Bailey's research, popularized by NN/g).
- **Preference test:** use cautiously — preference ≠ usability.

---

## 3. A/B testing (honest version)

One hypothesis, one primary metric, predefined guardrails, predefined sample and duration, no peeking.

**Sample size (two proportions, two-sided):**
`n per arm ≈ (z_{α/2} + z_β)² × [p₁(1−p₁) + p₂(1−p₂)] / (p₁ − p₂)²`
At α=0.05, power=0.80: (1.96 + 0.84)² = 7.84.

Worked example — baseline 34%, target 42% (+8 pp): n ≈ 7.84 × (0.2244 + 0.2436) / 0.0064 ≈ **~575 per arm**. A +2 pp lift needs ~9,000 per arm. Effect size matters: report Cohen's d (0.2 small / 0.5 medium / 0.8 large) alongside p — significance without effect size is noise.

Anti-pattern: A/B theater on a product with 50 weekly users. Go qualitative.

---

## 4. Heuristic evaluation & cognitive walkthrough

3–5 evaluators score independently against Nielsen's 10, then merge. Issues found by ≥2 evaluators independently are high-confidence; single-evaluator finds are candidates.

**Severity (Nielsen's scale):** **0** = not a usability problem · **1** = cosmetic · **2** = minor (workaround exists) · **3** = major (blocks, hard to work around) · **4** = catastrophe (data loss / legal / must fix before release).

**Cognitive walkthrough:** per step — will the user try this action? notice the control? understand the feedback? Scorecard template in templates.md.

**Nielsen's 10 (default critique lens):**

| # | Heuristic | Practical test |
|---|---|---|
| 1 | Visibility of system status | Told what's happening, quickly? |
| 2 | Match system ↔ real world | User's language, not engineering's? |
| 3 | User control & freedom | Easy undo/back? |
| 4 | Consistency & standards | Same words/patterns mean the same thing? |
| 5 | Error prevention | Error made impossible, not just handled? |
| 6 | Recognition over recall | Needed info visible, not memorized? |
| 7 | Flexibility & efficiency | Expert shortcuts without blocking novices? |
| 8 | Aesthetic & minimalist | Only what's needed? |
| 9 | Error recovery | Plain language + path forward? |
| 10 | Help & documentation | Searchable, task-oriented, short? |

---

## 5. Usability laws (apply by name when critiquing)

- **Fitts's Law** (1954): MT = a + b·log₂(1 + D/W). Primary targets big and close. ≥24px (WCAG 2.2) / 44px (Apple touch).
- **Hick's Law** (1952): RT = b·log₂(n+1). Fewer options; progressive disclosure.
- **Jakob's Law** (Nielsen): users prefer your site to work like everyone else's. Deviate only with evidence.
- **Miller 7±2 (1956), revised by Cowan (2001) to 4±1** working-memory chunks. Chunk lists beyond 4–5.
- **Tesler's Law:** complexity can be moved, not eliminated — decide who carries it. Smart defaults move it to the system.
- **Postel's Law** (RFC 761): liberal in what you accept (forgive input formats), conservative in what you send.
- **Peak-End Rule** (Kahneman & Fredrickson 1993): experiences judged by peak + ending. Design both deliberately.
- **Serial Position Effect** (Ebbinghaus 1885): edges of lists are remembered; middles vanish.
- **Aesthetic-Usability Effect** (Kurosu & Kashimura 1995): beauty delays detection of usability problems — useful for first impressions, dangerous as a testing substitute.
- **Gestalt proximity:** group with whitespace, not borders.

---

## 6. Hypothesis-driven experiments

| Experiment | Answers | Rough cost (illustrative) |
|---|---|---|
| **Smoke test** (landing + signup) | Is there demand? | $20–500 ads, 3–7 days |
| **Fake door** | Want this specific feature? | Hours on a live product |
| **Wizard of Oz** (manual backend) | Would they use it if it worked? | 1–2 weeks, 5–20 users |
| **Concierge** (deliver by hand) | What does the job really involve? | 2–4 weeks, 3–10 customers |

Hypothesis form: *We believe [change] for [segment] will produce [outcome]; we'll know within [timeframe] when we see [signal].* Template in templates.md. Source: Ries; Bland & Osterwalder, *Testing Business Ideas*.

---

## 7. PMF signal (Sean Ellis)

"How would you feel if you could no longer use this product?" — Very / Somewhat / Not disappointed.
**≥40% "very disappointed" among users who've used it ≥2 times** = strong signal. <~25% = keep iterating. 25–40% = building toward it. Run on *activated* users only; including never-activated signups dilutes the signal.

---

## 8. IA validation

- **Card sorting** (open/closed/hybrid): 15–20 participants per segment (Tullis & Wood 2004). Anti-pattern: shipping the org chart as navigation.
- **Tree testing:** task success on a text-only tree. Common practitioner benchmark (directional, via Optimal Workshop): ≥70% success and ≥60% directness before visual design; below that, restructure.

## Go deeper
Krug *Don't Make Me Think* · Nielsen/NN/g · Ries *The Lean Startup* · Bland & Osterwalder · Sauro & Lewis *Quantifying the User Experience* (for deeper stats).
