# Design Craft — Phase 4

Load for: flows, IA, wireframes, visual design, interaction, platform guidelines, accessibility, internationalization.

## Contents
1. Fidelity & flows
2. Information architecture
3. Visual & interaction design
4. Platform guidelines
5. Accessibility (WCAG 2.2 AA)
6. Internationalization

---

## 1. Fidelity & flows

Sketch → lo-fi → mid-fi → hi-fi; fidelity matches the question (table in SKILL.md decision trees). Going hi-fi too early makes stakeholders argue about color instead of structure. Draw the task flow (single sequence, one task) before user flows and IA. Every screen ships with empty, loading, error, success — and where relevant partial-data, offline, slow-network — states.

## 2. Information architecture

Sitemap = structure; user flow = one user's path; task flow first, IA follows. Match the user's mental model, validated by tree testing (see validation-and-math §8). Don't invent navigation unless existing patterns demonstrably fail — Jakob's Law.

## 3. Visual & interaction design

- **Typography & rhythm:** ≤2 typefaces; modular scale (1.25 or 1.333); 4/8px spacing grid; hierarchy from contrast in size, weight, color, space.
- **Gestalt in practice:** group form fields by proximity not borders; figure/ground for focus.
- **Design systems:** tokens (color, space, type, radius) → components → patterns → templates, with usage AND anti-usage documented. Worth it the moment a product expects to outlive v1.
- **Microinteractions (Saffer):** trigger → rules → feedback → loops/modes. Motion communicates causality and hierarchy, never decoration; Disney's 12 principles (anticipation, follow-through, easing) apply to UI; always respect `prefers-reduced-motion`.

## 4. Platform guidelines

- **Apple HIG:** clarity, deference (content above chrome), depth. 44px touch minimum.
- **Material (m3):** material metaphor, intentional color/type, motion as meaning, elevation for hierarchy.
- **Fluent:** light, depth, motion, material, scale across form factors; pairs with Microsoft Inclusive Design.

Match the platform's conventions before inventing; users carry platform muscle memory across apps.

## 5. Accessibility — WCAG 2.2 AA as the floor

POUR: perceivable, operable, understandable, robust. Minimum checks for every UI artifact:

- Contrast **4.5:1** body, **3:1** large text & non-text UI
- Visible focus states; logical tab order; full keyboard operability
- Semantic HTML + accessible names (screen-reader announceable)
- Alt text for meaningful images, empty alt for decorative
- Captions/transcripts for AV
- Never color alone for information (pair icon/text/pattern)
- `prefers-reduced-motion` respected
- Targets ≥ **24×24px** (2.2 addition)

**Inclusive design (Microsoft):** disability = mismatch between person and environment. Design for permanent (one arm) / temporary (broken arm) / situational (holding a baby); solve for one, extend to many.

**Cognitive accessibility:** plain language (default ~grade 7–8 for general products — see narrative-and-writing for the reading-level table), predictable patterns, chunking past 4–5 items, no untimed-extendable interactions.

Bolted-on accessibility is expensive, incomplete, and visible. Design it in at wireframe stage; audit before ship.

## 6. Internationalization & localization

English-only US-default design serves a small fraction of the world. i18n = the architecture (externalized strings, locale-aware formats, RTL-ready layouts); l10n = the per-locale adaptation.

**Text expansion vs English (plan layouts to flex +40%):** German +30–40% · Russian +20–30% · French +15–25% · Spanish +10–20% · Japanese −20–30% · Chinese −30–40% · Arabic up to +25% and RTL.

**RTL:** whole layout mirrors — back arrows, progress bars, navigation, not just text. `dir="rtl"` plus logical CSS properties (`margin-inline-start`). Test mirrored before claiming readiness.

**Never assume formats:** dates (21/04 EU, ISO JP), 24-hour time, decimal separators (1.000,50 EU), currency display, name order (family-first JP/CN/KR; single names ID/MM), address order, phone formats.

**Beyond translation:** color semantics differ by culture (red: luck in China, warning in US); imagery inclusivity; legal layers (EU consent, age gates); **local payment methods** — UPI in India, Alipay/WeChat in China, iDEAL in NL. Card-only checkout is a revenue leak.

## Go deeper
Norman *The Design of Everyday Things* · Saffer *Microinteractions* · W3C WCAG 2.2 & i18n WG · Apple HIG · Material m3 · Microsoft Inclusive Design Toolkit.
