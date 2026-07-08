# Product Design Partner

**A senior product design partner inside Claude — from raw idea to validated, shipped, measured, growing product.**

🌐 **Website:** https://rahim1845.github.io/product-design-partner/

An open-source [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) for Claude that prevents the three failure modes that kill most products:

1. **Building something nobody wants**
2. **Building something people want in a way that fails them**
3. **Building something people like that no business can sustain**

## What it does

- **Diagnoses your phase first** — nine lifecycle phases from `0 · Worth-it` to `8 · Grow`, each with objectives and honest exit criteria
- **Loads only the expertise you need** — ten expert modes routing to a nine-file reference library (strategy, research, design craft, validation math, shipping, growth, narrative, AI ethics, portfolio)
- **Produces concrete artifacts** — ranked assumption maps, Mom-Test interview guides, usability test plans with real sample-size math, positioning statements. Never generic advice.
- **Carries sourced numbers** — Nielsen-Landauer usability math, WCAG 2.2 contrast ratios, Sean Ellis PMF thresholds, A/B sample-size formulas. Real citations, or explicitly labeled illustrative.

## Install

```bash
# 1 — get the skill
git clone https://github.com/rahim1845/product-design-partner.git

# 2 — install it for Claude
cp -r product-design-partner/skill ~/.claude/skills/product-design-partner
```

Then just talk to Claude about your product — the skill triggers on phrases like *"validate my idea"*, *"is this worth building"*, *"usability test"*, *"review this flow"* — or invoke it directly:

```
/product-design-partner I have an app idea — help me figure out if it's worth building
```

Works in Claude Code, the Claude desktop app, and anywhere Agent Skills are supported.

## Structure

```
skill/
├── SKILL.md                        # Core routing: modes, phases, principles, edge cases
├── CHANGELOG.md
└── references/
    ├── product-strategy.md         # Worth-it, positioning, growth loops, unit economics
    ├── discovery-and-research.md   # Interviews, synthesis, personas, journeys
    ├── design-craft.md             # Flows, IA, interaction, a11y, i18n
    ├── validation-and-math.md      # Usability testing, A/B math, heuristics, PMF
    ├── shipping-and-measurement.md # Handoff, rollout, metrics, retention
    ├── narrative-and-writing.md    # Copy, value props, launches
    ├── ai-ux-and-ethics.md         # AI product UX, trust, failure states
    ├── portfolio-and-career.md     # Case studies, design storytelling
    └── templates.md                # Every artifact template
index.html                          # The website (GitHub Pages)
```

## The ten modes

| Mode | When |
|---|---|
| Worth-it | "Should I build this?", new idea, pivot decision |
| Discovery partner | Research, interviews, synthesis, personas, journeys |
| Design partner | Flows, IA, UI, interaction, accessibility, i18n |
| Validator | Testing, experiments, A/B, PMF, heuristic eval |
| Critic | "Review this design/flow/copy/strategy" |
| Shipper / measurer | Handoff, rollout, metrics, post-launch, retention |
| Growth & positioning | GTM, segments, growth loops, pricing, north star |
| Storyteller | Copy, value props, decks, launches, naming |
| AI product | Any feature that generates, predicts, or decides |
| Portfolio | Case studies, job applications, design storytelling |

## Contributing

Issues and PRs welcome. Keep the skill's principles intact: evidence over opinion, real sources only, artifacts over advice.

## License

[MIT](LICENSE) — free to use, modify, and distribute.
