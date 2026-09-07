# Decisions

Newest first. One entry per decision that would be expensive or confusing to reverse
without knowing the reasoning.

---

## 2026-09-07 — Same artifact publish conflict recurred; skipped again, escalating to the founder

**Decision:** The 2026-09-07 run first merged the 2026-09-06 entry (which never made it live)
into `ledger.html`, confirmed the live artifact was still stuck at "4 entries" via the version
diff the Artifact tool's `publish` refusal itself surfaced (not via the barred `read` action),
and resent the merged, now-6-entry file. That resend was refused too, this time because the
tool could not distinguish "this is the same content as my last refused attempt" from "this
content already includes the newer version's changes" without an explicit `read` of the
artifact URL to confirm — which `overall/research/ARTIFACT.md` still bars this run for the same
reason as 2026-09-06 (risk of an unattended permission-prompt hang on a sensitive save path).
`force:true` was also not used, since it requires explicit human confirmation this run has no
way to obtain. Repeating the exact prior refusal on a second consecutive day means this is a
structural gap in the run's tool permissions, not a one-off fluke — see the open item below.

**Why this is safe to leave unresolved for now:** Same reasoning as 2026-09-06 — `ledger.html`
in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly contains
all 6 entries (Sep 2 through Sep 7) even though the live page only shows 4. No research content
is lost.

**Reversible?** Yes. A human (or a future run with `read`/`force` permission, or one that starts
by explicitly fetching the artifact URL before editing) can republish `ledger.html` from the
repo to catch the live page up in one shot.

**Open item for the founder:** Two runs in a row have now hit this exact wall. Either grant a
future run permission to use the Artifact `read` action on this specific URL (accepting the
permission-prompt-hang risk `ARTIFACT.md` describes, perhaps by having a human available when
that run fires), or have a human manually republish `ledger.html` once to reset the artifact's
version state so subsequent same-session publishes stop conflicting.

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
