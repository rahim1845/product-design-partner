# AI Product UX & Ethics

Load for: LLM/agent features, AI trust design, hallucination handling, dark patterns, consent, addictive design, algorithmic fairness.

## Contents
1. The three AI UX jobs
2. Trust signals
3. Hallucination defense in depth
4. AI anti-patterns
5. Prompt design as interface design
6. Ethics: consent & data minimization
7. Ethics: habit-forming design
8. Ethics: algorithmic transparency
9. AI-specific legal/ethical floor

---

## 1. The three AI UX jobs

1. **Communicate uncertainty.** Model confidence varies; never imply precision the system doesn't have.
2. **Make verification cheap.** Check, correct, override — without friction.
3. **Preserve agency.** The model suggests; the user decides. Automation is earned through demonstrated reliability, not assumed.

## 2. Trust signals (illustrative targets — adapt per product; LLMs do not emit calibrated confidence scores, so "confidence" here means designed proxies: retrieval hit quality, self-consistency checks, eval-derived reliability tiers)

| Signal | How | Target (illustrative) |
|---|---|---|
| Source attribution | Link every factual claim or say "no source" | All factual claims cited or flagged |
| Uncertainty indication | Tiered language/visuals for low/med/high reliability | Low-tier outputs always carry a caveat |
| Provenance | "AI-generated" / "human-reviewed" labels | Required for AI content shown to third parties |
| Reversibility | Undo, versions, edit-before-accept | Every AI action reversible in ≤1 step |

## 3. Hallucination — defense in depth

1. **Prevent:** RAG with cited sources; constrained output formats; explicit permission to say "I don't know" in the prompt.
2. **Detect:** schema validation, fact-check passes, human review gates on high-impact output.
3. **Recover:** easy correction, retry, report path that feeds back into improvement.

## 4. AI anti-patterns

- **False authority** — confident answer, no uncertainty signal. A plausible wrong answer is worse than none.
- **Chat as the only interface** — for most tasks direct UI is faster; chat is fallback or expert mode.
- **Infinite loading** — stream tokens, show steps or estimates.
- **Stolen agency** — auto-applying high-impact changes without review.
- **Magic without explanation** — recommendations with no rationale breed distrust.

## 5. Prompt design as interface design

Every user-facing AI feature has a prompt behind it; that prompt IS part of the UX. Treat prompt edits as design decisions: version them, test them, review them. System prompts for persistent rules (tone, scope, refusals); user prompts for task input. Injection resistance: delimit user input, treat it as data not instructions.

Sources: NN/g generative-UI research; Google PAIR guidebook; Microsoft HAX toolkit; Anthropic documentation.

---

## 6. Consent & data minimization

Collect the minimum needed to deliver the value; default to not collecting. Consent must be specific, informed (plain language), freely given, and revocable without burial. Heuristic (directional): if withdrawing consent takes meaningfully more effort than granting it, the design is manipulative — aim for parity. Regulatory floor varies: GDPR (EU), CCPA (CA), DPDP Act (India), LGPD (Brazil), PIPL (China) — check jurisdiction before shipping.

## 7. Habit-forming design, honestly

Eyal's Hook Model (trigger → action → variable reward → investment) works — which is exactly why it needs guardrails:

- Does the habit serve the user's *stated* goals, or only the business?
- **Regret test:** in 6 months, will users be glad they formed this habit? (Duolingo streak: mostly yes. Slot-machine feeds: mostly no.)
- Real off-ramps: pause, mute, frequency controls — findable within a couple of taps, not buried.

## 8. Algorithmic transparency & bias

- Personalization that affects **opportunity** (jobs, credit, housing, matches) must be explainable; if you can't explain why a user saw something, reconsider shipping it.
- Test outputs across race, gender, age, ability, geography; document and fix representational failures before launch.
- Click-trained feedback loops amplify bias — log, audit, rebalance.

## 9. AI-specific floor

- Label AI-generated content visibly, not in tooltips.
- No imitating specific humans (voice, style, likeness) without explicit consent.
- No claiming human status — legally mandated in several jurisdictions (e.g. California SB 1001).

## Go deeper
Zuboff *The Age of Surveillance Capitalism* · Benjamin *Race After Technology* · Gebru et al. on model documentation · Cavoukian, Privacy by Design · Google PAIR · Microsoft HAX.
