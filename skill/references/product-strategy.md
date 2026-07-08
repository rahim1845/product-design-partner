# Product Strategy — Worth-It, Positioning, Growth

Load for: "should I build this", segment choice, positioning, GTM, growth loops, pricing direction, north star, OKRs, prioritization, business viability.

## Contents
1. Phase 0: Worth-it (DVF, segment selection, kill criteria)
2. Positioning (Dunford method)
3. North Star & input metrics
4. OKRs
5. Kano Model + survey
6. Prioritization frameworks
7. Growth loops vs funnels
8. Retention before growth
9. Unit economics quick reference
10. Monetization & willingness to pay
11. Vision, strategy narrative, BMC/VPC

---

## 1. Phase 0 — Worth-it

Before discovery effort, rank the idea's assumptions across three lenses (IDEO's DVF):

| Lens | Question | Typical riskiest assumption |
|---|---|---|
| **Desirability** | Does a specific segment feel this pain often and intensely? | "People want this" |
| **Feasibility** | Can we build it with our actual constraints? | "The tech/data exists" |
| **Viability** | Can a business sustain it? | "Someone will pay / CAC < LTV" |

Method: list every assumption the idea embeds, tag each D/F/V, plot on **Important × Unknown** (Bland). Test the top-right quadrant first with the cheapest possible experiment (see validation-and-math experiment table). Most consumer ideas die on desirability; most B2B ideas die on viability (real pain, nobody budgets for it).

**Segment selection** — when multiple segments could work, score each 1–5 on:
- **Pain severity** (do they describe it unprompted, with emotion, with workarounds?)
- **Willingness to pay** (do they already spend money or meaningful time on workarounds?)
- **Reachability** (can you find and talk to 10 of them this month?)

Pick the highest product of the three. A medium-pain segment you can reach beats a high-pain segment you can't. This is the beachhead — win it before generalizing (crossing-the-chasm logic).

**Kill criteria, written in advance.** Before investing a month, write: "We stop if ___." E.g., "if fewer than 4 of 10 interviewees describe the problem unprompted" or "if the smoke test converts under 2%." Pre-committed kill criteria are the antidote to sunk-cost drift. Revisit honestly; pivoting on evidence is a win, not a failure.

---

## 2. Positioning (April Dunford, *Obviously Awesome*)

Positioning is an input to everything downstream (copy, pricing, roadmap), not a marketing afterthought. Work the chain in order:

1. **Competitive alternatives** — what would users do if you didn't exist? (Often: spreadsheet, intern, nothing.)
2. **Unique attributes** — what do you have that alternatives don't?
3. **Value** — what do those attributes *enable* for the customer? (Attribute → benefit → value.)
4. **Who cares most** — which segment feels that value most acutely? (Feeds back into beachhead.)
5. **Market category** — what frame makes the value obvious? (Category choice sets expectations and comparison set.)

Pitfall: positioning against the market leader's frame when you'd win in a different category. Test: describe the product in one sentence to five target users; if they can't say back who it's for and why it beats their current alternative, the positioning isn't done.

---

## 3. North Star metric & input metrics

North Star = the single metric that best captures delivered user value over time. Input metrics = the 3–5 levers that move it.

Canonical examples: Airbnb nights booked · Spotify time listening · Slack messages in teams that return · Dropbox files synced across devices.

**Construction test:** if the metric goes up, did a user definitely get value? Yes → candidate. "Maybe" → vanity. (MAU without activation qualifier; time-on-site that could mean engaged *or* lost.)

Source: Amplitude North Star Framework; Sean Ellis on activation.

---

## 4. OKRs — outcomes, not outputs

Objective = qualitative ambitious direction. KRs = 3–5 measurable **outcomes**, never shipped features.

- Bad KR: "Ship new onboarding flow by Q2."
- Good KR: "Week-1 activation from 34% → 45%."

Google's 0.7 calibration: KRs should feel like a 70% shot. All hit = sandbagged; all missed = fantasy.

Source: Doerr, *Measure What Matters*; Seiden, *Outcomes Over Output*; Cagan.

---

## 5. Kano Model

Classify candidate features: **Must-haves** (invisible when present, painful when absent) · **Performance** (more is better) · **Delighters** (unexpected joy). You cannot delight your way out of a missing must-have.

Coffee-app example: must-have = order status + accurate ETA; performance = fewer taps to order; delighter = handwritten note on the cup.

**Kano survey:** per feature, two questions on a 5-point scale (like / expect / neutral / tolerate / dislike):
1. Functional: "If the product HAD [feature], how would you feel?"
2. Dysfunctional: "If it did NOT have it, how would you feel?"

| Functional | Dysfunctional | Category |
|---|---|---|
| Like | Dislike | Performance |
| Like | Neutral/Tolerate | Delighter |
| Expect/Neutral | Dislike | Must-have |
| Neutral | Neutral | Indifferent (cut) |
| Like | Like | Questionable (re-ask) |

Sample: 20+ per segment directional; 100+ for confidence. Source: Noriaki Kano (1984).

**Products users love, operationally:** must-haves flawless → friction lowest at the moments of highest intent → one or two deliberate delighters placed at peaks and endings (Peak-End Rule) → never at the cost of trust.

---

## 6. Prioritization frameworks

| Framework | Method | Best for |
|---|---|---|
| RICE | (Reach × Impact × Confidence) ÷ Effort | Quantified tradeoffs |
| ICE | Impact × Confidence × Ease | Fast triage |
| MoSCoW | Must/Should/Could/Won't | Scoping a release |
| Impact/Effort | 2×2 | Whiteboard speed |
| WSJF | Cost of Delay ÷ Job Size | Scaled agile |

All scores are opinion-in-disguise; use them as conversation structure, not truth. Template in templates.md.

---

## 7. Growth loops vs funnels

Funnels leak; loops compound. A growth loop is a closed cycle where output of one cohort becomes input acquiring the next:

- **Viral/word-of-mouth loop:** user gets value → tells/invites others → new users. Works when value is visible or collaborative (Figma, WhatsApp). Measure: invites sent per user × acceptance rate (a directional "viral factor").
- **Content/SEO loop:** users create or generate content → content indexes → searchers become users (Pinterest, Stack Overflow, UGC marketplaces).
- **Paid loop:** revenue from cohort → buys ads → acquires next cohort. Only compounds if payback period is short enough to recycle capital.
- **Sales loop:** B2B — customer success stories → references → pipeline.

Pick the loop the product's *usage* naturally feeds; bolted-on loops (referral bribes on a product nobody mentions) decay. Source: Reforge growth-loop material; Casey Winters / Brian Balfour public writing.

---

## 8. Retention before growth

Acquisition into a product that doesn't retain is paying to fill a leaky bucket. Order of operations: **activation → retention → then acquisition → then monetization tuning** (sequence varies by model, but retention nearly always precedes scaling spend).

A retention curve that flattens above zero = a core of users who'd genuinely miss it; flat-at-zero = no PMF, fix the product not the funnel. Benchmarks by category live in shipping-and-measurement.md — treat as directional, and per SKILL.md principle 10, search for current data when the decision is consequential.

---

## 9. Unit economics quick reference (directional definitions, not financial advice)

| Term | Definition | Rule-of-thumb signal |
|---|---|---|
| **CAC** | Fully-loaded cost to acquire one customer | — |
| **LTV** | Gross-margin profit expected over a customer's life | LTV:CAC ≥ ~3:1 commonly cited as healthy for SaaS (directional) |
| **Payback period** | Months for a customer's margin to repay CAC | <12 months commonly targeted in SaaS (directional) |
| **Churn / NRR** | % lost per period / net revenue retention incl. expansion | NRR >100% = the base grows without new logos |
| **ARPU, MRR/ARR** | Avg revenue per user; monthly/annual recurring revenue | — |

Designers who can read these earn a seat in roadmap conversations: a design that lifts activation shortens payback; one that lifts expansion lifts NRR. Connect design work to one of these levers when pitching it.

---

## 10. Monetization & willingness to pay (early signals)

- **Best signal:** they already pay for a workaround (tool, service, intern hours). Second best: they spend significant recurring *time* on it.
- **Van Westendorp price-sensitivity questions** (directional, small-N friendly): too cheap / bargain / getting expensive / too expensive — plots an acceptable range.
- **Smoke-test pricing:** put a price on the landing page before the product exists; measure click-through to "buy." Tells you more than any survey.
- Pitfall: asking "would you pay for this?" — Mom Test rules apply; hypothetical yes is worthless.

---

## 11. Vision, strategy narrative, canvases

**Strategy narrative** (Cagan; Amazon working-backwards): who is this for, what job, why now, how is it different, what does the world look like if we win. One page. If the team can't retell it, it isn't a strategy yet.

**Business Model Canvas / Value Proposition Canvas** (Osterwalder): hypothesis-capture tools — every cell must be testable, none filled from imagination. VPC zooms into fit between customer jobs/pains/gains and pain relievers/gain creators.

**PR/FAQ** (Amazon): write the press release before building. Template in templates.md.

---

## Go deeper
Cagan *Inspired/Empowered* · Osterwalder *Testing Business Ideas* · Dunford *Obviously Awesome* · Doerr *Measure What Matters* · Ellis & Brown *Hacking Growth* · Moore *Crossing the Chasm* · Reforge/Winters/Balfour on loops · Bryar & Carr *Working Backwards*.
