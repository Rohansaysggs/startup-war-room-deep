# startup-war-room-deep (big)

The exhaustive version of the `startup-war-room` skill: a named team of 8 expert personas evaluates a business idea, researches real competitors on the web, scores it against a 6-dimension rubric, and climbs through up to **10 full rounds** — each with a full written vignette of how a startup at that score would actually play out, and a real revision made in response — toward an honest final verdict. It will not inflate a score the idea hasn't earned.

**This is the expensive sibling.** It costs noticeably more tokens and time than [`startup-war-room`](../startup-war-room/) (the small/lean version). Use this one when you actually want maximum rigor — otherwise use the small version, which does the same core exercise in a fraction of the cost.

## What you get (on top of the small version)

- Up to 10 rounds instead of 6, following a finer-grained tier ladder (0.5 → 1.5 → 3 → 4.5 → 6 → 7.2 → 8.3 → 9.1 → final push).
- A full written "simulated run" vignette every round — a concrete story of how a real startup at that score would survive or die in year 1-2, grounded in real comparable companies.
- A complete round-by-round log in the final report (not just a progression table + key pivots).
- Uncapped research (still batched sensibly) rather than a fixed search budget.

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
