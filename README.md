# razorpay-ai-research

My research + strategy notes for the Razorpay AI Buildathon 2026.

## what's in here

### v2 (current) — Track 5 (Open) — Vulcan-Ready SME Underwriting Agent

Pivoted from Track 3 to Track 5 after cross-verified competitor research (25+ repos across all 5 tracks analyzed). Zero competitors are doing underwriting; Razorpay's CEO publicly said Vulcan will enable real-time underwriting "in the coming months."

- `vulcan-underwriting-strategy.pdf` — 64-page strategy doc. Calibrated PD (Brier, ECE, bootstrap CI), Fairlearn per-language fairness audit across 7 Indian languages, multilingual LLM-explained decisions, AST-enforced decision gate where the LLM never approves loans.
- `uw_diagrams/` — 5 PNG diagrams (underwriting architecture, 9-day Gantt, decision tree, dashboard mockup, video storyboard).
- `uw_cover/` — cover source (HTML + standalone PDF).

### v1 (archived) — Track 3 — Hinglish Revenue Recovery Engine

Original Track 3 strategy, now superseded by the Track 5 pivot. Kept for reference.

- `razorpay-strategy.pdf` — 62-page Track 3 strategy doc (Hinglish Revenue Recovery Engine).
- `diagrams/` — 5 PNG diagrams (architecture flow, 9-day Gantt, decision tree, dashboard mockup, video storyboard).
- `cover/` — cover source (HTML + standalone PDF).

## tl;dr

building a vulcan-aligned sme underwriting agent for track 5 (open). 4 pillars:

1. **vulcan alignment** — razorpay's ceo harshil mathur publicly said vulcan will enable real-time underwriting in coming months. this prototype is that layer. zero competitors in any track have this alignment.
2. **calibrated pd** — xgboost + isotonic calibration. brier < 0.15, ece < 0.05, bootstrap 95% ci. zero competitors ship the calibrated-honesty triad.
3. **fairlearn fairness audit** — per-language, per-segment, per-region parity across 7 indian languages. zero competitors report fairness metrics.
4. **ast-enforced decision gate with multilingual explanations** — llm bounded to explanation rendering; ast test verifies llm never approves loans. 7 languages, slot-validated.

positioning sentence (memorize this for the pitch):
> the only buildathon submission aligned with razorpay's vulcan lending roadmap: a calibrated probability-of-default model (brier, ece, bootstrap ci), per-language fairness audit (fairlearn across 7 indian languages), multilingual llm-explained decisions, and an ast-enforced decision gate where the llm never approves loans — prototyping what responsible real-time sme lending should look like.

## why this track (not the others)

cross-verified competitor research across 25+ repos:

- **track 2 (risk manager)** — 2 gold-standard competitors (prahari-ai with 905 tests, yvssshubam with bootstrap ci). 1v2 fight. discarded.
- **track 3 (revenue recovery)** — 15+ serious competitors (lokeshwar2005 with live deployed sites, seagull28 with linucb bandit, omgitcode with bayesian + hinglish, daksha1611 with gold-standard bounded ai). every pillar of my original plan is now claimed. discarded.
- **track 4 (finance controller)** — 5-6 serious competitors including shivamshukla02/reconai which is already doing multilingual ledger matching (killed my option A). discarded.
- **track 5 (open) — vulcan-aligned underwriting** — zero competitors. only priyanshu singh's "ai candidate authenticity" entry found, which is generic ai not razorpay-relevant. chosen.

## verified facts

- vulcan launched august 18, 2026 (aws press release, 30+ press sources)
- ceo harshil mathur quote: "real-time underwriting and credit evaluation in the coming months"
- track 2 defense-only rule confirmed verbatim
- solo-build-only NOT confirmed (team size unspecified)
- 4-pillar rubric partially confirmed (spirit yes, verbatim no)

## status

strategy doc done (64 pages). actual build starts now.
