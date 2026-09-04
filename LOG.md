# Work log

Newest entry at the top. Short entries: what changed, what it revealed, what's next.

---

## 2026-09-04 — Third competitor research entry: general AI job copilots vs. resume-parsing commoditization

Daily research routine's third entry: `overall/research/2026-09-04-competitor-analysis.md`.
Covered ground the prior two passes hadn't: consumer AI job-search copilots (Jobright.ai's
0-100 match scoring, Sonara.ai's "career fingerprint" auto-apply loop) and confirmed the
resume-parsing API market (Affinda/Textkernel/RChilli/Sovren/MokaHR/Superparser) is mature and
cheap (~$0.04-0.20/resume) — sharpening a build-vs-buy call on `src/resume-extract/`. Updated
`overall/research/ledger.html` (now 3 entries filed) and republished the artifact.

## 2026-09-03 — Second competitor research entry: university-channel incumbents

Daily research routine's second entry: `overall/research/2026-09-03-competitor-analysis.md`.
Covered ground the Sept 2 pass hadn't: 12Twenty and Symplicity (business-school career-center
incumbents, logistics not fit-scoring), Firsthand/Vault (employer rankings, a plausible Career
Signal data source), O*NET's own free Interest Profiler, Traitify/Crosschq, Handshake's newer
AI features (the sharpest adjacent threat found so far), ChangeBegins.ai, and Find Your Grind.
Updated `overall/research/ledger.html` (now 2 entries filed) and republished the artifact.

## 2026-09-02 — First real competitor research entry (merged two passes)

Daily research routine's first real find: `overall/research/2026-09-02-competitor-analysis.md`.
Nine new competitors/adjacents logged (JobCannon, pymetrics, Eightfold AI, Prentus, Forage,
RippleMatch, resume-parser APIs, ATS screening tools). Merged in a prior run's findings
(pymetrics/Eightfold/Prentus/Forage) that had reached the live Competitor Ledger artifact but
never got committed to git — no matching file/commit existed anywhere in history, so treated
as an interrupted earlier run and folded into this entry rather than duplicated or dropped.
Updated `overall/research/ledger.html` (now 1 entry filed) and republished the artifact.

**Next:** consider whether the session-reliability gap (publish succeeded, commit never
happened) needs investigating separately from the routine's own logic.

## 2026-09-02 — Drafted business plan skeleton

Created `overall/pitch/BUSINESS_PLAN.md`, structured around DNVC's Stage II/III judging
criteria and pulling from `overall/BASE_IDEA.md` + competitor research where content
exists. Flagged real gaps inline rather than inventing numbers: market sizing, pricing/
unit economics, financial projections, team bios, exit strategy point of view, and
prototype timeline are all still open.

**Next:** Founder fills in the flagged gaps, starting with whichever is most decision-
blocking (likely business model pricing and team).

## 2026-09-02 — Resolved naming, drafted Stage I materials

Founder chose "VinceCam" over "Camvince" — updated all 122 references in
`overall/BASE_IDEA.md` and the Competitor Ledger. Drafted
`overall/pitch/STAGE_I_DESCRIPTION.md` (short written description) and
`overall/pitch/STAGE_I_VIDEO_SCRIPT.md` (1-minute video script) for DNVC Stage I.

**Next:** Founder reviews/edits both drafts, registers on the DNVC entrant submission
system, records the video, submits before 2026-11-15.

## 2026-09-02 — Targeting Duquesne New Venture Challenge 2026-2027 cycle

Researched and recorded the real DNVC timeline in `overall/DUQUESNE_TIMELINE.md`.
Team entrant submissions opened 2026-09-01; Stage I (short description + 1-min video)
due 2026-11-15. Duquesne affiliation confirmed already covered on the team (needed by
Stage III, April 2027). This is now the driving deadline for near-term project work.

**Next:** Resolve Camvince/VinceCam naming, then draft Stage I written description and
video script from `overall/BASE_IDEA.md`.

## 2026-09-01 — Published Competitor Ledger artifact, wired into daily routine

Published a Claude Artifact (`overall/research/ARTIFACT.md` has the URL) as a
human-readable, always-current view of the daily competitor research — a running log,
newest entry first, instead of requiring a `git pull` to read a markdown file. Updated
the "VinceCam daily competitor research" routine to read that URL, append each night's
entry to the artifact (via the Artifact tool's read-then-publish-to-same-URL pattern),
in addition to its existing `overall/research/*.md` file + `LOG.md` line + git push.

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
