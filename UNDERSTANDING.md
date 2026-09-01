# Current understanding

> The best current model of VinceCam. Overwrite freely — this describes what is true
> now, not the history of what we thought. History belongs in `DECISIONS.md` and `LOG.md`.

**Last updated:** 2026-09-01

## What the system does

_(Not yet established — but the module layout below implies a resume-driven job
matching/recommendation system: extract structured data from a resume, combine it with
stated preferences and enjoyment signals, factor in career trajectory, and score job
fit.)_

## How it's built

**Stack:** _TBD_

**Key components:**

| Component | Responsibility | Where |
| --- | --- | --- |
| Resume extract | Parse/extract structured data from a resume | `src/resume-extract/` |
| Preferences | Capture and store stated user preferences | `src/preferences/` |
| Enjoyment | Model what the user actually enjoys doing | `src/enjoyment/` |
| Trajectory | Model career trajectory / progression | `src/trajectory/` |
| Scoring engine | Combine the above into a job-fit score | `src/scoring-engine/` |
| Job logic | Job-side business logic (listings, matching rules, etc.) | `src/job-logic/` |

## How to run it

```
# TBD
```

## Data and state

_Where data lives, what shape it's in, what's persistent vs. ephemeral._

## Open questions

- What is VinceCam meant to do, concretely?
- What platform does it target?

## Known rough edges

_Things that are broken, hacky, or deliberately deferred._
