# Templates

Default artifact formats. Adapt fields to context. Loaded on demand when producing a deliverable.

## Contents
1. decisions.md (project memory)
2. Persona (incl. proxy variant)
3. JTBD statement
4. Journey map
5. Empathy map
6. HMW question set
7. Opportunity solution tree
8. Assumption map
9. Hypothesis statement
10. Research discussion guide
11. Usability test plan
12. Heuristic evaluation scorecard
13. RICE matrix
14. PR/FAQ (Working Backwards)
15. Positioning one-pager

---

## 1. decisions.md — project memory

```markdown
# [Product] — decisions log
Updated: [date] · Phase: [worth-it / discovery / define / ideate / design / validate / ship / measure / grow]

## Problem statement
[Current best version — evidenced, specific, measurable]

## Target segment
[Who, chosen over what alternatives, why — pain × willingness × reachability scores if used]

## Riskiest assumption
[Statement] — status: [untested / testing via X / supported / busted on DATE]

## Decisions
| Date | Decision | Rationale | Evidence |
|---|---|---|---|

## Rejected options (and why)
- [Option] — rejected because [reason]. Revisit if [condition].

## Next bet
[One sentence + the signal that would confirm/kill it]
```

## 2. Persona

```markdown
# Persona: [Behavioral name, never demographic]
**Evidence type:** [Primary (N interviews) | Proxy (reviews/forums/public research) | Mixed]
**Evidence base:** [e.g. "8 interviews Mar 2026; 47 app store reviews"]
**Primary JTBD:** When [situation], I want to [motivation], so I can [outcome].
**Current workaround:** [...]
**Top 3 frustrations (cited to evidence):** 1. … 2. … 3. …
**Success criteria:** [...]
**Behavioral trigger:** [event that starts the search for a solution]
**Verbatim quote:** "[Real, with source link or transcript line. Never invented.]"
**Anti-persona:** [who this is NOT for]
```

## 3. JTBD statement

> When **[situation/trigger]**, I want to **[motivation]**, so I can **[expected outcome]**.

Example: *When I finish a workout exhausted, I want to log it in under 10 seconds, so I can keep my streak without disrupting my routine.*

## 4. Journey map

Emotion on 1–7 (1 = abandoning, 4 = neutral, 7 = advocating). Stages ≤3 = priority opportunities; 6–7 = peaks to protect.

| Stage | Actions | Thoughts | Emotion 1–7 | Touchpoints | Pains | Opportunities |
|---|---|---|---|---|---|---|

## 5. Empathy map

| Says (real quotes) | Thinks (inferred) |
|---|---|
| **Does** (observed) | **Feels** (1–7) |

## 6. HMW set

```markdown
Context: [problem statement] · User: [persona] · Outcome: [measurable change]
1. HMW help [user] [job] without [friction]?
2. HMW turn [pain] into [delighter]?
3. HMW reduce [load/steps/time] for [task]?
(Generate 5–10, keep the 3 most generative.)
```

## 7. Opportunity solution tree

```
            [Desired Outcome]
        ┌─────────┼─────────┐
   [Opportunity] [Opp]  [Opp]      ← evidenced user needs
     ┌───┴───┐
 [Solution] [Solution]
     │
 [Assumption] → [Experiment]
```

## 8. Assumption map

```
Important ↑ │ TEST FIRST      │ defer (known)
            │─────────────────┼──────────────
            │ test later      │ ignore for now
            └─────────────────┴──────────────→ Unknown
```
Tag each assumption D/F/V (desirability/feasibility/viability). Top-right: define the cheapest disproving experiment.

## 9. Hypothesis statement

> We believe **[change]** for **[segment]** will result in **[outcome]**.
> We'll know we're right when we see **[signal]** within **[timeframe]**.

Example (illustrative): *replacing the empty home screen with a 3-step checklist for new signups → week-1 activation 34% → ≥42% over 4 weeks at p<0.05, without week-4 retention dropping >3 pp.*

## 10. Research discussion guide

```markdown
# Discussion guide — [study]
Goal: [one sentence] · Decision informed: [specific] · Participants: [segment, N] · Length: [30/45/60]

Warm-up (5m): typical [context] walkthrough.
Behavior (15m): "Walk me through the last time you [specific past behavior]."
  What were you trying to do? What got in the way? What did you do instead?
Task/prototype (20m, if applicable): "[task], think aloud."
Wrap (5m): magic wand; anything I should've asked?

NOT to ask: "Would you use this?" · "Do you like it?"
```

## 11. Usability test plan

```markdown
# Test plan — [flow]
Hypothesis: [users complete X because Y]
Success: [completion ≥ Z%; time ≤ T; SEQ ≥ 5.5/7]
Participants: 5/segment (Nielsen) · Method: [moderated/unmoderated, remote/in-person]
Tasks (scenarios, not instructions): "You want to [goal]. Show me how."
Collected: success, time, errors, SEQ, verbatims
Severity: Nielsen 0–4 · Readout: findings severity-ranked with clips
```

## 12. Heuristic evaluation scorecard

| # | Heuristic | Issue | Location | Severity 0–4 | Recommendation |
|---|---|---|---|---|---|

(0 not a problem · 1 cosmetic · 2 minor · 3 major · 4 catastrophe. ≥2 independent evaluators = finding; 1 = candidate.)

## 13. RICE matrix

| Idea | Reach | Impact (.25/.5/1/2/3) | Confidence % | Effort (p-w) | Score |
|---|---|---|---|---|---|
| A | 10,000 | 1 | 80% | 4 | 2,000 |

Scores are structured opinion — use as conversation, not verdict.

## 14. PR/FAQ

```markdown
# Press release — [product]
Headline: [User] can now [outcome they care about]
Subhead: [who it's for, one line]
P1 — Problem as the user lives it. No jargon.
P2 — The solution, plain language, outcome over mechanism.
P3 — Customer quote (hypothetical, labeled as such): "Before X I [workaround]. Now I [easier path]. Saves me [measurable]."
P4 — How to get started.

# Internal FAQ
What problem does this solve? · Who is it for (and explicitly not for)? ·
Riskiest assumption? · What must be true to succeed (top 3–5)? ·
How will we measure success (metric, threshold, timeframe)? · What will we NOT do in v1?
```

## 15. Positioning one-pager (Dunford chain)

```markdown
Competitive alternatives: [what they'd do without you]
Unique attributes: [what you have that they don't]
Value: [what those attributes enable]
Who cares most: [beachhead segment + why]
Category: [the frame that makes value obvious]
One-sentence test: [say it to 5 target users; can they repeat who it's for and why it beats their alternative?]
```
