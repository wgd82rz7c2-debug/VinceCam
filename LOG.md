# Work log

Newest entry at the top. Short entries: what changed, what it revealed, what's next.

---

## 2026-09-01 — Filled in overall/BASE_IDEA.md with full canonical spec

Replaced the placeholder with the full "Camvince — Current Canonical Product Idea"
document (career decision-intelligence platform, 4-dimension profile, 3-stage
career→employer→location flow, CareerExplorer competitive analysis, scoring formulas,
business model, contradiction audit). Updated `UNDERSTANDING.md` to summarize it and map
the six `src/` modules to the relevant spec sections.

**Flagged, not resolved:** the spec consistently names the product "Camvince" while the
project/repo is "VinceCam" — noted in `UNDERSTANDING.md` open questions, not renamed.

**Next:** resolve the naming question; start implementation stack decisions.

## 2026-09-01 — Added overall/ for the base idea

Created `overall/BASE_IDEA.md` as the source-of-truth concept doc, sitting alongside
`src/` rather than inside it (it's not application code). Intent: once filled in, a
validation agent checks each module's supporting info against this file for drift.
Content is still TBD — placeholder only.

**Next:** Fill in `overall/BASE_IDEA.md` with what VinceCam actually is, then scope the
validation agent (what "supporting info" means per module, how it runs, how drift is
reported).

## 2026-09-01 — Removed unused scaffold folders

Removed `docs/`, `files/`, `scratch/` — all empty, not needed. Updated `CLAUDE.md`'s
layout table and dropped the working agreement that referenced them.

## 2026-09-01 — Module layout added under src/

Created six module folders under `src/`: `resume-extract/`, `preferences/`,
`enjoyment/`, `trajectory/`, `scoring-engine/`, `job-logic/`. Updated
`UNDERSTANDING.md`'s component table to match. All folders are currently empty.

**Next:** Fill in what each module actually owns and start implementing, beginning
wherever the data pipeline naturally starts (likely `resume-extract/`).

## 2026-09-01 — Project created

Scaffolded `~/projects/VinceCam` with `src/`, `docs/`, `files/`, `scratch/`, plus
`CLAUDE.md`, `UNDERSTANDING.md`, `DECISIONS.md`, and this log.

**Next:** Define what VinceCam actually is and fill in `UNDERSTANDING.md`.
