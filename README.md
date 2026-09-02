# razorpay-ai-research

My research + strategy notes for the Razorpay AI Buildathon 2026 (Track 3 — AI Revenue Recovery).

## what's in here

- `razorpay-strategy.pdf` — the main 62-page strategy doc. covers everything: competitor teardown of 14 repos, the 4-pillar differentiation strategy, full architecture, synthetic dataset schema, ML model code, Hinglish sample scripts, failure modes, pitch video script, README template, the works.
- `diagrams/` — the 5 PNG diagrams used in the doc (architecture, 9-day Gantt, decision tree, dashboard mockup, video storyboard). felt like keeping them separate so they're easy to drop into the pitch video later.
- `cover/` — the cover page source (HTML + standalone PDF) in case i want to tweak the design later without rebuilding the whole doc.

## tl;dr

building a payment-failure recovery pipeline on razorpay test mode. 4 pillars: real closed-loop webhooks, measured P(recovery) on a holdout (not heuristics like every other competitor), decline-code-aware routing, and multilingual comms in 7 indian languages — all under an AST-enforced policy gate so the LLM literally cannot make decisions.

positioning sentence (memorize this for the pitch):
> the only Track 3 submission with real Razorpay test-mode closed-loop recovery, measured P(recovery) on a held-out batch with baselines and bootstrap CI, decline-code-aware routing, and multilingual customer comms — under an AST-enforced policy gate with a replayable audit ledger.

## status

strategy doc done. actual build starts now — 9 days to deadline.
