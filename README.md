# startup-war-room-deep (big)

**Maximum rigor, before you quit your job.** The exhaustive version: 8 expert personas, real competitor research, and 10 full rounds — each with a written simulation of how a startup at that score would actually live or die — ending in an honest, defensible score.

The exhaustive version of the `startup-war-room` skill: a named team of 8 expert personas evaluates a business idea, researches real competitors on the web, scores it against a 6-dimension rubric, and climbs through up to **10 full rounds** — each with a full written vignette of how a startup at that score would actually play out, and a real revision made in response — toward an honest final verdict. It will not inflate a score the idea hasn't earned.

**This is the expensive sibling.** It costs noticeably more tokens and time than [`startup-war-room`](../startup-war-room/) (the small/lean version). Use this one when you actually want maximum rigor — otherwise use the small version, which does the same core exercise in a fraction of the cost.

## What you get (on top of the small version)

- Up to 10 rounds instead of 6, following a finer-grained tier ladder (0.5 → 1.5 → 3 → 4.5 → 6 → 7.2 → 8.3 → 9.1 → final push).
- A full written "simulated run" vignette every round — a concrete story of how a real startup at that score would survive or die in year 1-2, grounded in real comparable companies.
- A complete round-by-round log in the final report (not just a progression table + key pivots).
- Uncapped research (still batched sensibly) rather than a fixed search budget.

## Example output (abridged)

```
Run my idea through the full war room: a P2P car rental insurance add-on.

Round 1 — Score 0.9/10 → Round 4 — Score 4.6/10 → Round 7 — Score 7.4/10
→ Round 10 — FINAL: 7.8/10

Round 7 simulated run: "Year one, the team signs two mid-size P2P rental
platforms as pilot partners. Underwriting costs eat the first six months
of margin before volume-based pricing kicks in — survivable, but it's a
capital question, not a product one..."

FINAL VERDICT: 7.8/10 — a real, fundable business with a genuine
insurance/regulatory moat, not a feature. Biggest open risk: state-by-
state insurance licensing timelines, not the product itself.
```

Illustrative excerpt of the report format, not a verbatim transcript — real output depends on live web research and the specific idea.

## Install

```bash
cp -r startup-war-room-deep ~/.claude/skills/
```

(project-level: copy into `.claude/skills/` inside your repo instead). On Windows, the user-level path is `%USERPROFILE%\.claude\skills\`.

## Use it

```
Run my idea through the full/deep startup war room — don't hold back: [your idea]
```

or

```
/startup-war-room-deep
```

If you just want a normal-rigor pass, use `/startup-war-room` instead — this one is deliberately the expensive option.

## License

MIT.
