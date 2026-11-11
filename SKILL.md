---
name: startup-war-room-deep
description: Runs the exhaustive, maximum-rigor "startup war room" on an idea — a named virtual team of 8 expert personas (market, competitive intelligence, product, finance, growth, legal/risk, domain) debates it in full, researches real competitors on the web, rates it on a 0-10 scale, simulates how a startup at that quality level would actually succeed or fail in a written vignette, revises it, and re-rates across up to 10 full rounds, climbing toward an honest final verdict (it will not inflate a score the idea hasn't earned). This is the BIG, expensive sibling of the "startup-war-room" skill — it costs far more tokens/time than that one. Only use this one when the user explicitly asks for maximum depth/rigor, "all 10 rounds", "the full/deep version", "don't hold back", or says the quick version wasn't thorough enough. For an ordinary "rate my startup idea" request, use "startup-war-room" (the small one) instead.
---

# Startup War Room (deep)

A full idea goes in; a battle-tested, research-backed idea comes out. This isn't a single pass of pros/cons — it's a bounded loop: score honestly, find out why the score is low, fix that specific thing, re-research, re-score. Each round must leave the idea measurably different, not just more confidently described.

This is the **exhaustive** sibling of this skill pair — full per-round write-ups, a full round-by-round log in the final report, up to 10 rounds, uncapped research. It costs substantially more tokens and time than the small version. If the user just wants a reasonably rigorous evaluation on a normal budget, point them at the **startup-war-room** skill instead — only run this one when they've actually asked for the deep treatment.

**Why this works the way it does:** a single-shot "rate my idea 1-10" is mostly vibes. Forcing a *climb* through many rounds, with real competitor research and a short "how would this actually play out" vignette each round, makes each score earn its place: you can't jump from 2 to 9 without the intermediate rounds exposing what actually breaks at 2, 4, 6... The named team with fixed roles exists so nothing gets silently skipped — if there's no line attributable to the legal/risk person, legal risk didn't get checked.

## 0. Before you start

Read `references/rubric.md` now — it has the scoring dimensions, the 10-round tier ladder, and the exact round-record template to fill in each round. Don't skip this; reproducing it from memory drifts.

Get the idea from the user. If the core concept, target customer, or geography is genuinely unclear, ask one tight clarifying question — but don't stall on details the team can reasonably assume and state ("assuming US B2B SMB market unless told otherwise"). State every assumption you make out loud in the report; a wrong assumption the user can correct beats silence.

## 1. The team

Use these names and lanes every time, so the report reads as one consistent team across many idea evaluations, not a reshuffled cast:

| Name | Role | Lens |
|---|---|---|
| **Jordan Blake** | Managing Partner (facilitator) | Runs the room, synthesizes, assigns and defends the final score each round, decides if a round needs another pass |
| **Priya Anand** | Market & Timing Lead | TAM/SAM/SOM, is now the right time, growth trajectory of the category |
| **Marcus Webb** | Competitive Intelligence Lead | Finds real competitors (web research, not memory), builds the comparison table, flags "this already exists and dominates" |
| **Elena Voss** | Product & Positioning Lead | What's actually being built, differentiation, why a user switches to this |
| **David Chen** | Financial Analyst | Unit economics (CAC/LTV ballpark), pricing/business model, capital intensity |
| **Aisha Okafor** | Growth & GTM Lead | How the first 100, 10,000, 1M customers actually get acquired |
| **Tom Reyes** | Risk, Legal & Regulatory Analyst | Regulatory exposure, legal liability, platform/distribution risk |
| **Dr. Sam Whitfield** | Domain Expert (floating) | State explicitly which domain they're standing in for this idea (e.g. "Dr. Whitfield, fintech compliance background" vs "...veterinary medicine background") — pick whatever real expertise the idea actually needs |

Each member speaks in the report under their own name on things in their lane. Jordan Blake writes the round's score and justification. This isn't cosmetic — if you catch yourself writing a round where only one or two people "spoke," go back and fill in the others; that's the sign a dimension got skipped.

## 2. The loop

Follow the tier ladder in `references/rubric.md` (roughly 0.5 → 1.5 → 3 → 4.5 → 6 → 7.2 → 8.3 → 9.1 → final push). Each round:

1. **State the current idea version** (verbatim strategy as of this round — round 1 is the user's idea as given).
2. **Research** — Marcus Webb runs real web searches for competitors/alternatives relevant to *this version* of the idea (not the original — the competitive set shifts as the idea narrows or pivots). Use actual company names, actual pricing/positioning where findable, not invented ones. Re-check this every round the positioning changes meaningfully; don't reuse round 1's competitor list unchanged for 8 rounds. Still batch related queries (one search covering several names at once) rather than firing one search per competitor.
3. **Score each dimension** (rubric file) and let Jordan Blake compute and justify the composite.
4. **Simulate the run** — write a short (3-6 sentence), concrete vignette of how a real startup at *this* score would actually play out over its first 1-2 years: where it gets traction, where it stalls or dies, grounded in patterns from real comparable companies (cite one or two by name). This is the mechanism that generates the *next* fix — the vignette should point directly at the weakest dimension.
5. **Extract the lesson and revise** — change something real about the idea/strategy (positioning, pricing, GTM channel, target segment, moat, legal structure) to address what the vignette exposed. Write exactly what changed and why.
6. **Record the round** using the template in the rubric file, then move to the next tier.

**Stopping conditions** — stop and move to the final report when either:
- The composite score clears 9.5/10, or
- You hit 10 rounds without clearing it.

If you hit the round cap without clearing 9.5, **say so plainly and report the real ceiling** — do not inflate the final number to look like a success. A capped-out 7.8 with an honest explanation of the structural blocker (e.g. "this is a feature, not a company — no defensible moat exists at any price point") is a correct and useful result. The whole point is rigor, not a guaranteed 10.

If at any point the team concludes the idea is fundamentally non-viable (illegal, no addressable market, a solved problem with no wedge), say so immediately rather than grinding through 10 rounds of cosmetic fixes — report that verdict with the reasoning, same as a normal stop.

**Hard override:** if Tom Reyes finds the core idea is illegal or regulatorily unworkable as described, the composite caps at 2/10 regardless of other dimensions until the structure changes to address it — don't average away a real blocker.

## 3. Producing the deliverable

Default to a **Claude Doc** (a living, shareable document) for the final report — this is long-form, evolving, multi-section content that benefits from being revisitable and shareable, not a one-shot answer.

- Check whether this session has a Claude Docs connector / `docs` skill available. If so, invoke it and follow **its own instructions exactly** for creating and updating the document — most such tools expect you to create the doc skeleton (title + section placeholders) *before* you start researching, then fill sections in as you go, not write the whole thing at the end. This run is long enough that the progressive-build pattern is worth the extra calls — unlike the small skill, don't skip it.
- If no Docs connector is available in this session, fall back in this order: (a) an HTML Artifact (if an Artifact tool is available), then (b) a plain Markdown file saved to disk, then (c) just the full report in your reply. Whichever you use, **tell the user explicitly which output you produced and where it is**.

### Report structure (use this regardless of output format)

```
# [Idea name/one-liner]

## Team
(the roster table from section 1, once)

## Executive summary
Final verdict in 3-5 sentences: final score, the single biggest thing that changed
between round 1 and the final round, and the one thing most likely to still break this.

## Rating progression
| Round | Score | What changed and why |
(one row per round — keep this scannable; detail lives in the per-round sections below)

## Round-by-round log
(one subsection per round: idea version, competitor findings, dimension scores,
the simulated vignette, the lesson, the revision — per the rubric template)

## Final competitor comparison
(a table: competitor | what they do | strength | weakness | how the final idea beats or loses to them —
this should reflect the FINAL idea's competitive set, not round 1's)

## Final strategy
(the fully revised idea: positioning, product, pricing/business model, GTM plan, moat, who it's for)

## Final score and justification
(dimension-by-dimension breakdown from Jordan Blake, composite, and — if capped out below 9.5 —
an explicit statement of the ceiling and why)

## Assumptions and open risks
(anything you assumed about the idea, and anything the team flagged but couldn't fully resolve)
```

## 4. Things that go wrong if you rush this

- **Skipping real research and inventing plausible-sounding competitors.** The whole value of this exercise is that it's grounded. If web search isn't available for some reason, say so explicitly in the report rather than presenting invented companies as real findings.
- **Treating the score as a vibe instead of the rubric sum.** Always show the dimension breakdown — a bare "7/10" with no rubric underneath is exactly the shallow single-shot output this skill exists to avoid.
- **Rounds that don't actually change anything.** If round 4's idea is textually identical to round 3's, the loop has stalled — the revision step is mandatory, not optional, every round.
- **Grade inflation at the end to hit 9.5+.** The last round is not exempt from the same rubric and research rigor as round 1.
- **Using this skill for a casual "quick rate my idea" ask.** That's what the small `startup-war-room` skill is for — if the user didn't ask for maximum depth, running this one instead just burns their budget for no real benefit.
