# Scoring rubric and round template (deep skill)

## Dimensions (each scored 0-10, composite = unweighted mean unless one dimension is a hard blocker)

- **Market & Timing** (Priya Anand) — real TAM/SAM/SOM, whether the category is growing or shrinking, why now and not 3 years ago or 3 years from now.
- **Differentiation & Moat** (Elena Voss) — why a customer switches to this specifically, and what stops a well-funded incumbent or fast-follower from copying it in a quarter.
- **Competitive Position** (Marcus Webb) — given the *actual* researched competitive set, is there real white space or is this a crowded commodity fight. This dimension's score should visibly track the competitor table — don't score this well while the table shows 4 dominant well-funded players doing the same thing.
- **Unit Economics & Capital Intensity** (David Chen) — plausible CAC/LTV relationship, gross margin profile, how much capital it takes to find out if this works.
- **Go-to-Market Feasibility** (Aisha Okafor) — is there a believable, specific channel to the first 100 customers (not "marketing and sales"), and does it get cheaper or more expensive at scale.
- **Risk & Regulatory Exposure** (Tom Reyes) — legal/regulatory surface area, platform dependency risk (e.g. living entirely inside someone else's API/App Store terms), liability.

One hard override: if Tom Reyes finds the core idea is illegal or regulatorily unworkable as described, the composite caps at 2/10 regardless of other dimensions until the structure changes to address it — don't average away a real blocker.

## Tier ladder (target composite at each round, roughly — use judgment, these are checkpoints not hard gates)

1. Round 1: ~0.5 — the raw idea exactly as given, scored honestly and usually harshly.
2. Round 2: ~1.5
3. Round 3: ~3
4. Round 4: ~4.5
5. Round 5: ~6
6. Round 6: ~7.2
7. Round 7: ~8.3
8. Round 8: ~9.1
9. Rounds 9-10 (only if needed): final push past 9.5, or the honest ceiling.

Rounds can move faster than this ladder if the fixes are genuinely that effective, or stall below it if a dimension is structurally capped (e.g. regulatory override above) — the ladder is a pacing guide so the exercise doesn't balloon past 10 rounds, not a script to force-fit.

## Research budget

No hard cap, but still batch related queries — one query covering several competitor/angle names at once is both cheaper and usually returns better comparative context than several narrow ones. Re-research whenever a round's positioning shift is big enough to plausibly change the competitive set; say "unchanged from round N-1" otherwise rather than re-describing the same findings.

If no web search tool is available at all in this session, say so explicitly in the report's "Assumptions and open risks" section, and rely only on well-established facts you're genuinely confident about — flag anything else as general knowledge, not verified research, rather than presenting it with false precision.

## Per-round record template

Fill this in for every round, in the report's "Round-by-round log" section:

```
### Round N — score ~X/10

**Idea version:** (one paragraph — what's being proposed this round; for round 1 this is the
user's original idea verbatim/summarized; later rounds state exactly what changed from the prior round)

**Research (Marcus Webb):** (named real competitors/alternatives found this round, with a
one-line strength and one-line weakness each — only re-run this if the positioning shifted
enough to change who the competitors even are; say "unchanged from round N-1" if not)

**Dimension scores:**
| Dimension | Score | One-line reason |
|---|---|---|
| Market & Timing (Priya) | | |
| Differentiation & Moat (Elena) | | |
| Competitive Position (Marcus) | | |
| Unit Economics (David) | | |
| GTM Feasibility (Aisha) | | |
| Risk & Regulatory (Tom) | | |

**Composite (Jordan Blake):** X/10 — (one or two sentences on how it was computed, including whether
the hard-override cap applied)

**Simulated run:** (3-6 sentences — concretely, how a real startup at this score plays out in year 1-2;
name a real comparable company's actual trajectory if it clarifies the failure/success mode)

**Lesson → revision:** (what the vignette exposed, and the specific change made to the idea/strategy
for the next round — must be a real, material change, not a rephrasing)
```

## If the user actually just wants a normal-rigor pass

This skill is deliberately the expensive, exhaustive option. If it turns out the user didn't really need maximum depth — they just said "rate my idea" without asking for the full treatment — the small **startup-war-room** skill does the same core exercise in a fraction of the tokens and time. Don't hesitate to suggest it for a lighter-weight follow-up idea.
