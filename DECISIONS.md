# Decisions

Newest first. One entry per decision that would be expensive or confusing to reverse
without knowing the reasoning.

---

## 2026-09-06 — Skipped artifact publish this run rather than use Artifact `read` or `force`

**Decision:** The 2026-09-06 research run edited `overall/research/ledger.html` (new entry,
updated entry count) but did **not** get the change onto the live Competitor Ledger artifact.
The Artifact tool refused the publish, reporting a version conflict against a "newer version"
of the artifact and instructing that the fix is to fetch the artifact's URL (the `read` action)
to reconcile before retrying, or to pass `force:true`. Both are barred for this routine:
`overall/research/ARTIFACT.md` explicitly forbids `read` on this URL this run (it can save a
copy under a sensitive `~/.claude/projects/.../tool-results/` path that hangs an unattended run
waiting on a permission prompt nobody can approve), and `force` requires explicit human
confirmation this run has no access to. Retrying the identical publish twice reproduced the
same refusal rather than resolving it.

**Why this is safe to leave unresolved for now:** `ledger.html` in the repo is the committed
source of truth per `ARTIFACT.md`; nothing about the underlying research or repo state was
lost. The live artifact page is simply stale (still showing 4 entries) until the next run, a
human, or a future session republishes it from this file.

**Reversible?** Yes, trivially — republish `overall/research/ledger.html` to the artifact URL
in `ARTIFACT.md` once the version conflict is understood (worth checking, when a human is
available, whether the artifact received an out-of-band edit — e.g. a viewer comment or manual
publish — that the next run needs to merge rather than overwrite).

---

## 2026-09-02 — Product name is VinceCam, not Camvince

**Decision:** The product name is "VinceCam" — matching the project directory and GitHub
repo. `overall/BASE_IDEA.md` and `overall/research/ledger.html` (which called it
"Camvince" throughout) were updated to match.

**Why:** Needed one settled name before drafting Duquesne New Venture Challenge Stage I
materials for judges. Founder chose VinceCam over Camvince when asked directly.

**Reversible?** Yes, but costly — reverses a naming decision baked into 122 references
across the canonical spec. Don't flip again without strong reason.

---

## 2026-09-01 — Adopted full canonical spec as overall/BASE_IDEA.md

**Decision:** The user-supplied "Camvince — Current Canonical Product Idea" document
(dated 2026-09-01) replaces the placeholder `overall/BASE_IDEA.md` in full, verbatim.

**Why:** It's the authoritative current-state spec per its own internal source-precedence
rule, superseding older scoring formulas and design docs referenced within it (see its own
§78 contradiction audit).

**Reversible?** Yes — it's a living document meant to be edited in place going forward.
(Naming later resolved to "VinceCam" — see 2026-09-02 entry above.)

---

## 2026-09-01 — Six-module layout under src/

**Decision:** Application code under `src/` is split into six modules:
`resume-extract`, `preferences`, `enjoyment`, `trajectory`, `scoring-engine`,
`job-logic`.

**Why:** Requested layout — resume parsing, user preferences, and enjoyment signals
feed a scoring engine that evaluates jobs (job logic), with trajectory tracked as a
separate factor rather than folded into preferences.

**Reversible?** Yes — folders are currently empty; renaming or merging them costs
nothing yet.

---

## 2026-09-01 — Plain folder, no git

**Decision:** VinceCam lives at `~/projects/VinceCam` as a plain directory, not a git repo.

**Why:** Chosen at setup time; version history wasn't wanted yet.

**Reversible?** Yes — `git init` in place at any point, nothing depends on this.
