# §5 programme metric — measurement plan (to be filled from internship data)

*The paper's §5 currently states that the internship programme "produces
measurable data". A claim of measurability is stronger when it names the exact
quantities and how each is counted. This file is the definitions sheet: fill
the right-hand column from the record files, then move one summary line into
the paper.*

## Why this matters for the deposit

One real, honestly-scoped number — even a single cohort — changes the paper
from "we run this" to "we measured this". It also gives the reviewer something
concrete to verify. Keep the numbers **aggregated and anonymised**: counts and
rates only, never intern names, never individual performance.

## Definitions (count from the record files, not from memory)

| Metric | Source of truth | Definition | Value |
|---|---|---|---|
| I — interns in cohort | `PROGRESS.md` M0/onboarding entries | distinct interns who completed onboarding | *[FILL]* |
| P — projects | one per intern workspace | projects under LDD for the full cohort | *[FILL]* |
| D — deviations logged | `git log --grep '^DEV:'` per project | total `DEV:` commits across all projects | *[FILL]* |
| De / Dc / Dx — by class | commit tag suffix | `DEV:enhancement` / `correction` / `experiment` counts | *[FILL]* |
| R — revert events | `git` history | deviations individually reverted (`git revert`) | *[FILL]* |
| G — gate refusals | `PROGRESS.md` M4 gate entries | direction changes refused or deferred to owner | *[FILL]* |
| C — CAPA opened | `CAPA.md` | nonconformities raised | *[FILL]* |
| Cc — CAPA closed | `CAPA.md` status | nonconformities closed with verification | *[FILL]* |
| Cr — CAPA recurring | `CAPA.md` root cause | closed CAPA whose root cause reappeared (the key honesty metric) | *[FILL]* |
| S — spec-sync breaches | `PROGRESS.md` M3 entries | drift found after the fact (target: → 0 over the cohort) | *[FILL]* |

## Reporting note for §5

Suggested one-line insertion once the table is filled (replace bracketed parts):

> Across [I] interns and [P] projects, the cohort logged [D] deviations
> ([De] enhancements, [Dc] corrections, [Dx] experiments), reverted [R] of them
> individually, and closed [Cc] of [C] CAPA entries — with [Cr] recurring. No
> drift was found after the fact in [S] cases once the drift rule was adopted.

## Honest scoping

- Report the **cohort size** plainly. A 3-intern pilot is a legitimate pilot;
  present it as one, and state that the design is a single-arm case series, not
  a controlled trial.
- Do **not** infer productivity gains from these counts. They measure the
  *ledger*, not developer speed. Saying so protects the paper's credibility.
- If a number is embarrassing (e.g. a high CAPA recurrence), publish it anyway.
  A single honest negative result is worth more than a set of suspiciously clean
  ones — and it is exactly the data the method claims to make visible.
