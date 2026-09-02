# Current understanding

> The best current model of VinceCam. Overwrite freely — this describes what is true
> now, not the history of what we thought. History belongs in `DECISIONS.md` and `LOG.md`.

**Last updated:** 2026-09-01

## What the system does

**VinceCam** is a Career Decision Intelligence platform for early-career users, currently
beachheading on US college business students. It's explicitly *not* a one-shot career quiz
or resume-to-job matcher: it builds a living, versioned profile from resume evidence, stated
preferences, work-activity enjoyment, and career-trajectory priorities, then walks the user
through four stages — career ranking, employer comparison, location/office/posting fit, and
"what should I do next" — updating the profile as real internship/job experience comes in.

Full spec, competitive analysis (vs. CareerExplorer, general AI, LinkedIn, etc.), scoring
formulas, data sources, and business model: see [`overall/BASE_IDEA.md`](overall/BASE_IDEA.md)
— that is the canonical source of truth; this section is a summary only.

**Target:** the 2026-2027 Duquesne New Venture Challenge — see
[`overall/DUQUESNE_TIMELINE.md`](overall/DUQUESNE_TIMELINE.md). Stage I (short description +
1-minute video) is due 2026-11-15.

## How it's built

**Stack:** _TBD_ — `overall/BASE_IDEA.md` specifies the product/data/scoring model in
detail but doesn't commit to an implementation stack yet.

**Key components:** the four profile dimensions from `overall/BASE_IDEA.md` §6 (Readiness,
Work Fit/Enjoyment, Conditions Fit, Trajectory Fit) plus the Stage 1/2/3 decision logic map
onto the six `src/` modules as follows:

| Component | Responsibility | Where |
| --- | --- | --- |
| Resume extract | Parse resume into normalized capability evidence (§8–11) — feeds Readiness | `src/resume-extract/` |
| Preferences | Conditions Fit inputs: hours, travel, pay, work mode, location, etc. (§12–13) | `src/preferences/` |
| Enjoyment | Work Fit: which recurring work activities the user likes/dislikes (§14) | `src/enjoyment/` |
| Trajectory | Long-term priorities: optionality, pay growth, specialization, etc. (§17–18) | `src/trajectory/` |
| Scoring engine | Stage 1 math: Readiness/Coverage/Adjusted Readiness/Work Fit/Conditions/Trajectory → Overall Career Fit (§26–35) | `src/scoring-engine/` |
| Job logic | Stage 2/3: company × career comparison, entry difficulty, career signal, specialized experience, location/posting overrides (§37–45) | `src/job-logic/` |

## How to run it

```
# TBD
```

## Data and state

_Where data lives, what shape it's in, what's persistent vs. ephemeral._

## Open questions

- What platform does it target (web app? mobile?) — not specified in `overall/BASE_IDEA.md`.
- Implementation stack — not yet decided.
- The 22 open design questions in `overall/BASE_IDEA.md` §77 (final scoring weights, MVP
  career/employer count, pricing model, etc.) — unresolved by design, need validation.

## Known rough edges

_Things that are broken, hacky, or deliberately deferred._
