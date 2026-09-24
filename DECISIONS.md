# Decisions

Newest first. One entry per decision that would be expensive or confusing to reverse
without knowing the reasoning.

---

## 2026-09-24 — Same artifact publish conflict, nineteenth day running; second clean repo start in a row

**Decision (artifact):** This run's first publish attempt was refused because the tool considered
the live artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4
entries (Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began,
now for a nineteenth day. Compared that live HTML against the repo's `ledger.html` (already
carrying entries Sep 2 through Sep 24 after today's edit) and confirmed the repo version is still
a strict superset — the Sep 2–5 entries match verbatim. Republished the repo file as the merge.
That second attempt was refused too, with the same message as the prior seventeen days: the
content is identical to the version already refused, and the tool requires an explicit fresh
fetch of the artifact URL to confirm before it will accept the resend. `overall/research/
ARTIFACT.md` bars `read` on this URL for this run for the same permission-prompt-hang reason as
the prior eighteen days, and `force:true` again requires explicit human confirmation this run has
no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-23 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 23 entries (Sep 2 through Sep 24). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 23, now for a nineteenth consecutive day with no
forward progress. Did not send a new push notification about this specific item — the founder was
already notified about this exact, unresolved block on 2026-09-09 and nothing material has changed
since.

**Reversible?** Yes — same remedies as previously logged: (a) a human or future run with
`read`/`force` permission and a human available to approve the resulting prompt, (b) a human
manually republishing `ledger.html` once to reset the artifact's version state, or (c)
reconsidering whether `ARTIFACT.md`'s blanket `read` prohibition should be scoped more narrowly.
Restating rather than re-litigating, since nineteen days of identical escalation have produced no
founder action yet.

**Separately (repo hygiene):** This run started cleanly on `main`, up to date with `origin/main`,
working tree clean — a second consecutive clean start (after 2026-09-23), with no detached-HEAD
recovery needed.

**Separately (tooling):** Per this run's task brief, `WebFetch` was tested directly against five
unrelated domains (`arxiv.org`, `unicloud360.com`, `emerald.com`, `en.wikipedia.org`,
`crunchbase.com`) and failed identically on all five with `EGRESS_BLOCKED`; the proxy status
endpoint again showed zero relay failures, confirming the same blanket policy-level block observed
2026-09-20 through 2026-09-22 (not attempted 2026-09-23). Today's findings rest on `WebSearch`
snippets only; see the research file's Open Questions.

---

## 2026-09-23 — Same artifact publish conflict, eighteenth day running; repo state clean for the first time since 2026-09-18

**Decision (artifact):** This run's first publish attempt was refused because the tool considered
the live artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4
entries (Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began,
now for an eighteenth day. Compared that live HTML against the repo's `ledger.html` (already
carrying entries Sep 2 through Sep 23 after today's edit) and confirmed the repo version is still
a strict superset — the Sep 2–5 entries match verbatim. Republished the repo file as the merge.
That second attempt was refused too, with the same message as the prior sixteen days: the content
is identical to the version already refused, and the tool requires an explicit fresh fetch of the
artifact URL to confirm before it will accept the resend. `overall/research/ARTIFACT.md` bars
`read` on this URL for this run for the same permission-prompt-hang reason as the prior seventeen
days, and `force:true` again requires explicit human confirmation this run has no way to obtain,
so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-22 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 22 entries (Sep 2 through Sep 23). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 22, now for an eighteenth consecutive day with
no forward progress. Did not send a new push notification about this specific item — the founder
was already notified about this exact, unresolved block on 2026-09-09 and nothing material has
changed since.

**Reversible?** Yes — same remedies as previously logged: (a) a human or future run with
`read`/`force` permission and a human available to approve the resulting prompt, (b) a human
manually republishing `ledger.html` once to reset the artifact's version state, or (c)
reconsidering whether `ARTIFACT.md`'s blanket `read` prohibition should be scoped more narrowly.
Restating rather than re-litigating, since eighteen days of identical escalation have produced no
founder action yet.

**Separately (repo hygiene):** This run started cleanly on `main`, up to date with `origin/main`,
working tree clean — the first clean start since before the detached-HEAD pattern began appearing
on 2026-09-18. No recovery action was needed today.

**Separately (tooling):** Per this run's task brief, `WebFetch` was not attempted (confirmed still
blocked by network egress policy, consistent with the total outage observed directly on
2026-09-20 through 2026-09-22). Today's findings rest on `WebSearch` snippets only; see the
research file's Open Questions.

---

## 2026-09-22 — Same artifact publish conflict, seventeenth day running; also fast-forwarded a detached-HEAD repo state (fourth occurrence)

**Decision (artifact):** This run's first publish attempt was refused because the tool considered
the live artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4
entries (Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began,
now for a seventeenth day. Compared that live HTML against the repo's `ledger.html` (already
carrying entries Sep 2 through Sep 22 after today's edit) and confirmed the repo version is still
a strict superset — the Sep 2–5 entries match verbatim. Republished the repo file as the merge.
That second attempt was refused too, with the same message as the prior fifteen days: the
content is identical to the version already refused, and the tool requires an explicit fresh
fetch of the artifact URL to confirm before it will accept the resend. `overall/research/
ARTIFACT.md` bars `read` on this URL for this run for the same permission-prompt-hang reason as
the prior sixteen days, and `force:true` again requires explicit human confirmation this run has
no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-21 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 21 entries (Sep 2 through Sep 22). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 21, now for a seventeenth
consecutive day with no forward progress. Did not send a new push notification about this
specific item — the founder was already notified about this exact, unresolved block on
2026-09-09 and nothing material has changed since.

**Reversible?** Yes — same remedies as previously logged: (a) a human or future run with
`read`/`force` permission and a human available to approve the resulting prompt, (b) a human
manually republishing `ledger.html` once to reset the artifact's version state, or (c)
reconsidering whether `ARTIFACT.md`'s blanket `read` prohibition should be scoped more narrowly.
Restating rather than re-litigating, since seventeen days of identical escalation have produced no
founder action yet.

**Decision (repo hygiene):** This run started with `HEAD` detached at `e9728eb` (2026-09-21's
commit) while local `main` was five commits behind, at `70f0606` (2026-09-16) — `origin/main`,
however, was already caught up to `e9728eb` this time (unlike 2026-09-21, where `origin/main` was
also behind). This is the fourth occurrence of the same shape flagged 2026-09-18, 2026-09-19, and
2026-09-21: the session starts on a detached `HEAD` with the local `main` branch pointer stale.
Verified `HEAD` was a clean fast-forward ahead of local `main` (`git merge-base --is-ancestor main
HEAD`), then fast-forwarded local `main` to `HEAD` and checked out `main`; `origin/main` needed no
push this time since it was already current.

**Why this is safe:** A pure fast-forward onto a commit that already matched `origin/main` carries
no risk of losing or overwriting anyone's work.

**Reversible?** N/A — already applied; `main`, `HEAD`, and `origin/main` all point to the same
commit as of the start of this run's work.

**Open item for the founder, now four occurrences (2026-09-18, 2026-09-19, 2026-09-21, 2026-09-22):**
Restating 2026-09-21's flag rather than a new one, since the pattern and the recommended fix
(check whatever wrapper/environment starts these sessions so the next run begins on `main`) are
unchanged. Each occurrence has still been a clean, risk-free fast-forward, but that has held only
because no run has yet branched off in a conflicting direction while detached.

**Separately (tooling):** `WebFetch` was blocked on every domain tried this run, including
`example.com` — the same total-outage shape as 2026-09-20 and 2026-09-21, now a third consecutive
day. The proxy status endpoint again showed the proxy itself healthy with zero relay failures, so
the block sits above the proxy layer specifically for this tool. Today's findings rest on
`WebSearch` snippets only; see the research file's Open Questions.

---

## 2026-09-21 — Same artifact publish conflict, sixteenth day running; also fast-forwarded a detached-HEAD repo state

**Decision (artifact):** This run's first publish attempt was refused because the tool considered
the live artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4
entries (Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began,
now for a sixteenth day. Compared that live HTML against the repo's `ledger.html` (already
carrying entries Sep 2 through Sep 21 after today's edit) and confirmed the repo version is still
a strict superset — the Sep 2–5 entries match verbatim. Republished the repo file as the merge.
That second attempt was refused too, with the same message as the prior fourteen days: the
content is identical to the version already refused, and the tool requires an explicit fresh
fetch of the artifact URL to confirm before it will accept the resend. `overall/research/
ARTIFACT.md` bars `read` on this URL for this run for the same permission-prompt-hang reason as
the prior fifteen days, and `force:true` again requires explicit human confirmation this run has
no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-20 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 21 entries (Sep 2 through Sep 21). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 21, now for a sixteenth
consecutive day with no forward progress. Did not send a new push notification about this
specific item — the founder was already notified about this exact, unresolved block on
2026-09-09 and nothing material has changed since.

**Reversible?** Yes — same remedies as previously logged: (a) a human or future run with
`read`/`force` permission and a human available to approve the resulting prompt, (b) a human
manually republishing `ledger.html` once to reset the artifact's version state, or (c)
reconsidering whether `ARTIFACT.md`'s blanket `read` prohibition should be scoped more narrowly.
Restating rather than re-litigating, since sixteen days of identical escalation have produced no
founder action yet.

**Decision (repo hygiene):** This run started with `HEAD` detached at `88b5760` (2026-09-20's
commit) while local `main` and `origin/main` were both five commits behind, at `70f0606`
(2026-09-16) — the same detached-HEAD-behind-main failure shape flagged 2026-09-18 and
2026-09-19. Verified with `git log --oneline 70f0606..88b5760` that the five stranded commits
were exactly the legitimate 2026-09-17 through 2026-09-20 daily entries, no divergence or
conflicting work, then fast-forward-merged `main` to the detached tip and pushed before starting
today's work.

**Why this is safe:** A pure fast-forward with a verified-clean commit list on both sides carries
no risk of losing or overwriting anyone's work.

**Reversible?** N/A — already applied; `main` and `origin/main` are now caught up through
2026-09-20's commit as of the start of this run.

**Open item for the founder, now three occurrences (2026-09-18, 2026-09-19, 2026-09-21):**
Whatever mechanism leaves each run's session on a detached `HEAD` one or more commits ahead of
`main` at the *start* of the next run (rather than on `main` itself) keeps recurring. Each time,
recovery has been a clean fast-forward with no data at risk, but that's been true only because no
run has yet branched off in a conflicting direction while detached. Worth a founder-level look at
whatever wrapper/environment starts these sessions, so the next run begins on `main` rather than
relying on this routine to notice and recover a detached state every time.

---

## 2026-09-20 — Same artifact publish conflict, fifteenth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
fifteenth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries
Sep 2 through Sep 20) and confirmed the repo version is still a strict superset — the Sep 2–5
entries match verbatim. Republished the repo file as the merge. That second attempt was refused
too, with the same message as the prior thirteen days: the content is identical to the version
already refused, and the tool requires an explicit fresh fetch of the artifact URL to confirm
before it will accept the resend — functionally the `read` action.
`overall/research/ARTIFACT.md` bars `read` on this URL for this run for the same
permission-prompt-hang reason as the prior fourteen days, and `force:true` again requires
explicit human confirmation this run has no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-19 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 19 entries (Sep 2 through Sep 20). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 19, now for a fifteenth
consecutive day with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now fifteen days running, unresolved since first raised
2026-09-06:** Nothing has changed about this wall in fifteen days of identical daily escalation.
Restating the 2026-09-09 through 2026-09-19 options rather than inventing a new one, since none
of them have been acted on: (a) grant a future run permission to use `read` on this specific URL
with a human available to approve the resulting prompt if it appears, (b) have a human manually
republish `ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

**Separately:** `WebFetch` failed on every domain tried this run, including `example.com` — a
more severe instance than the selective small-site blocking (Nodes.inc, Testerly) running since
2026-09-13, and enough of a step-change to flag on its own rather than folding into the routine
weekly restatement. The proxy status endpoint reported healthy with no relay failures, so this
reads as a policy-level block on the fetch tool for this session rather than a network fault. Not
escalated via push notification on its own this run — it degraded research confidence for one
day's findings rather than the routine's ability to run, commit, or push — but flagged in today's
research file as worth a closer look if it recurs tomorrow.

---

## 2026-09-19 — Detached-HEAD-with-unpushed-commit recurred a second day running; this time no data was actually at risk

**Decision:** This run started the same way 2026-09-18's did: `HEAD` was detached, one commit
ahead of local `main` (`a339918`, 2026-09-18's own recovery commit) and — per this run's first
`git fetch origin main` — one commit ahead of `origin/main` too (still at `70f0606`, 2026-09-16's
commit). Confirmed with `git merge-base --is-ancestor main HEAD` that this was a clean
fast-forward, force-moved local `main` to `HEAD`, checked out `main`, and ran `git push -u origin
main`. The push reported "Everything up-to-date" — by the time it ran, `origin/main` had already
advanced to `a339918` on its own, meaning 2026-09-18's push evidently did succeed after all (or
some other process pushed it) and this run's initial fetch simply caught a stale moment. Net
effect: no commit was actually unreached or at risk this time, but the local working tree
(detached `HEAD`, `main` pointer lagging) was in the same unsafe-looking state as 2026-09-18's
genuine near-miss, for a second consecutive day.

**Why flagged anyway:** Whether or not data was at risk this specific time, a routine that
starts detached from `main` two days running — regardless of cause (a prior session ending
without checking out `main`, a checkout race with an in-flight push, or something else in how
this environment is provisioned between runs) — is a pattern worth the founder's attention
separately from the artifact-publish conflict below. This entry's `git status` check before
finishing confirms today's run ends with local `main` at the same commit as `origin/main`, per
the recommendation 2026-09-18 made.

**Reversible?** N/A — nothing to reverse; this is a process-hygiene flag, not a content change.

**Open item for the founder:** if this recurs a third day, it's probably not coincidence.
Recommend checking whatever wrapper or scheduler starts each day's session for whether it
`git checkout main` (vs. leaving a detached checkout from a prior clone/fetch step) before
handing control to the routine.

---

## 2026-09-19 — Same artifact publish conflict, fourteenth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for
a fourteenth day. Compared that live HTML against the repo's `ledger.html` (already carrying
entries Sep 2 through Sep 19) and confirmed the repo version is still a strict superset — the
Sep 2–5 entries match verbatim. Republished the repo file as the merge. That second attempt was
refused too, with the same message as the prior twelve days: the content is identical to the
version already refused, and the tool requires an explicit fresh fetch of the artifact URL to
confirm before it will accept the resend — functionally the `read` action.
`overall/research/ARTIFACT.md` bars `read` on this URL for this run for the same
permission-prompt-hang reason as the prior thirteen days, and `force:true` again requires
explicit human confirmation this run has no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-18 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 18 entries (Sep 2 through Sep 19). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 18, now for a fourteenth
consecutive day with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now fourteen days running, unresolved since first raised
2026-09-06:** Nothing has changed about this wall in fourteen days of identical daily
escalation. Restating the 2026-09-09 through 2026-09-18 options rather than inventing a new one,
since none of them have been acted on: (a) grant a future run permission to use `read` on this
specific URL with a human available to approve the resulting prompt if it appears, (b) have a
human manually republish `ledger.html` once to reset the artifact's version state, or (c)
reconsider whether `ARTIFACT.md`'s blanket prohibition should instead be scoped to only the
failure mode it was written for, so a run can still fetch-then-publish in the same turn when a
version conflict is detected. The founder was already notified out-of-band about this on
2026-09-09; since nothing material has changed since that notification (same wall, same
unresolved options, no new consequence), this run does not send a second one — repeating an
already-delivered alert with no new information would just be noise. If a human reads this and
still hasn't acted, the 2026-09-09 notification stands as the live ask.

**Separately:** `WebFetch` egress to `nodes.inc` and `testerly.com` failed again this run — now a
seventh consecutive day (2026-09-13 through 2026-09-19) blocking direct verification of both
standing competitor claims, and today additionally blocked a third domain
(`whichfinancebroareyou.com`), suggesting a general egress restriction rather than a
domain-specific one. Not escalated via push notification on its own — it degrades research
confidence on named items, not the routine's ability to run, commit, or push.

---

## 2026-09-18 — Recovered an unpushed 2026-09-17 commit found on session start; distinct from the artifact-publish issue

**Decision:** This run started with `HEAD` detached at a commit (`5b03dde`, "Daily competitor
research: 2026-09-17") that was one commit ahead of both the local `main` branch and
`origin/main` — the 2026-09-17 run's commit had never been merged into `main` or pushed. Fixed
by force-moving local `main` to include it (a fast-forward, since `main` was a strict ancestor),
then committing today's work on top and pushing both commits together. No content was at risk —
the commit existed and matched the repo state this run read at the start — but had this run not
happened to notice `git status`'s "HEAD detached" message, that commit would have stayed
unreachable from any branch and eventually been at risk of git garbage collection. This is a
distinct failure from the standing artifact-publish conflict below (that one leaves the *public
artifact page* stale while the repo stays correct; this one could have left the *repo itself*
missing a day's work). Recommend whoever runs this routine confirm each run ends on `main` with
`git status` showing "up to date with origin/main" before finishing, rather than assuming the
prior run's `git push` succeeded.

---

## 2026-09-18 — Same artifact publish conflict, thirteenth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
thirteenth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries
Sep 2 through Sep 18) and confirmed the repo version is still a strict superset — the Sep 2–5
entries match verbatim. Republished the repo file as the merge. That second attempt was refused
too, with the same message as the prior eleven days: the content is identical to the version
already refused, and the tool requires an explicit fresh fetch of the artifact URL to confirm
before it will accept the resend — functionally the `read` action. `overall/research/ARTIFACT.md`
bars `read` on this URL for this run for the same permission-prompt-hang reason as the prior
twelve days, and `force:true` again requires explicit human confirmation this run has no way to
obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-17 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 17 entries (Sep 2 through Sep 18). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 17, now for a thirteenth consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now thirteen days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in thirteen days of identical daily escalation. Restating the
2026-09-09 through 2026-09-17 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

**Separately:** `WebFetch` egress to `nodes.inc` and `testerly.com` failed again this run — now a
sixth consecutive day (2026-09-13 through 2026-09-18) blocking direct verification of both
standing competitor claims. `WebSearch` was available this run (unlike prior days) and surfaced
materially richer first-party-sourced detail on both names, reducing but not eliminating the need
for direct verification — see today's research file's Open Questions for detail. Not escalated via
push notification on its own — it degrades research confidence on named items, not the routine's
ability to run, commit, or push.

---

## 2026-09-17 — Same artifact publish conflict, twelfth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
twelfth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries
Sep 2 through Sep 17) and confirmed the repo version is still a strict superset — the Sep 2–5
entries match verbatim. Republished the repo file as the merge. That second attempt was refused
too, with the same message as the prior ten days: the content is identical to the version already
refused, and the tool requires an explicit fresh fetch of the artifact URL to confirm before it
will accept the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars
`read` on this URL for this run for the same permission-prompt-hang reason as the prior eleven
days, and `force:true` again requires explicit human confirmation this run has no way to obtain, so
neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-16 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 16 entries (Sep 2 through Sep 17). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 16, now for a twelfth consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now twelve days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in twelve days of identical daily escalation. Restating the
2026-09-09 through 2026-09-16 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

**Separately:** `WebFetch` egress to specific domains (`nodes.inc`, `testerly.com`, and today also
`territorium.com` and `www.mycareercompass.fit`) failed again this run — now five consecutive days
(2026-09-13 through 2026-09-17) blocking direct verification of the two standing competitor claims,
plus two new ones from today's research. This is a distinct infrastructure issue from the artifact
conflict above; see today's research file's Open Questions for detail. Not escalated via push
notification on its own — it degrades research confidence on named items, not the routine's
ability to run, commit, or push.

---

## 2026-09-16 — Same artifact publish conflict, eleventh day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for an
eleventh day. Compared that live HTML against the repo's `ledger.html` (already carrying entries
Sep 2 through Sep 16) and confirmed the repo version is still a strict superset — the Sep 2–5
entries match verbatim. Republished the repo file as the merge. That second attempt was refused
too, with the same message as the prior nine days: the content is identical to the version already
refused, and the tool requires an explicit fresh fetch of the artifact URL to confirm before it
will accept the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars
`read` on this URL for this run for the same permission-prompt-hang reason as the prior ten days,
and `force:true` again requires explicit human confirmation this run has no way to obtain, so
neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-15 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 15 entries (Sep 2 through Sep 16). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 15, now for an eleventh consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now eleven days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in eleven days of identical daily escalation. Restating the
2026-09-09 through 2026-09-15 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

**Separately:** `WebFetch` egress to specific domains (`nodes.inc`, `testerly.com`) failed again
this run — now four consecutive days (2026-09-13 through 2026-09-16) blocking direct verification
of two specific, previously-flagged competitor claims. This is a distinct infrastructure issue
from the artifact conflict above; see today's research file's Open Questions for detail. Not
escalated via push notification on its own — it degrades research confidence on two named items,
not the routine's ability to run, commit, or push.

---

## 2026-09-15 — Same artifact publish conflict, tenth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
tenth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries Sep
2 through Sep 15) and confirmed the repo version is still a strict superset — the Sep 2–5 entries
match verbatim. Republished the repo file as the merge. That second attempt was refused too, with
the same message as the prior eight days: the content is identical to the version already refused,
and the tool requires an explicit fresh fetch of the artifact URL to confirm before it will accept
the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars `read` on this
URL for this run for the same permission-prompt-hang reason as the prior nine days, and
`force:true` again requires explicit human confirmation this run has no way to obtain, so neither
was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-14 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 14 entries (Sep 2 through Sep 15). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 14, now for a tenth consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now ten days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in ten days of identical daily escalation. Restating the
2026-09-09 through 2026-09-14 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

**Separately:** `WebFetch` egress to specific domains (`nodes.inc`, `testerly.com`) failed again
this run — now three consecutive days (2026-09-13 through 2026-09-15) blocking direct verification
of two specific, previously-flagged competitor claims. This is a distinct infrastructure issue
from the artifact conflict above; see today's research file's Open Questions for detail. Not
escalated via push notification on its own — it degrades research confidence on two named items,
not the routine's ability to run, commit, or push.

---

## 2026-09-14 — Same artifact publish conflict, ninth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
ninth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries Sep
2 through Sep 14) and confirmed the repo version is still a strict superset — the Sep 2–5 entries
match verbatim. Republished the repo file as the merge. That second attempt was refused too, with
the same message as the prior seven days: the content is identical to the version already refused,
and the tool requires an explicit fresh fetch of the artifact URL to confirm before it will accept
the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars `read` on this
URL for this run for the same permission-prompt-hang reason as the prior eight days, and
`force:true` again requires explicit human confirmation this run has no way to obtain, so neither
was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-13 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 13 entries (Sep 2 through Sep 14). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 13, now for a ninth consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now nine days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in nine days of identical daily escalation. Restating the
2026-09-09 through 2026-09-13 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

---

## 2026-09-13 — Same artifact publish conflict, eighth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for an
eighth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries Sep
2 through Sep 13) and confirmed the repo version is still a strict superset — the Sep 2–5 entries
match verbatim. Republished the repo file as the merge. That second attempt was refused too, with
the same message as the prior six days: the content is identical to the version already refused,
and the tool requires an explicit fresh fetch of the artifact URL to confirm before it will accept
the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars `read` on this
URL for this run for the same permission-prompt-hang reason as the prior seven days, and
`force:true` again requires explicit human confirmation this run has no way to obtain, so neither
was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-12 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now correctly
contains all 12 entries (Sep 2 through Sep 13). No research content is lost; only the live page is
stale, still showing 4 entries against the repo's 12, now for an eighth consecutive day with no
forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now eight days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in eight days of identical daily escalation. Restating the
2026-09-09 through 2026-09-12 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

---

## 2026-09-12 — Same artifact publish conflict, seventh day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
seventh day. Compared that live HTML against the repo's `ledger.html` (already carrying entries
Sep 2 through Sep 12) and confirmed the repo version is still a strict superset — the Sep 2–5
entries match verbatim. Republished the repo file as the merge. That second attempt was refused
too, with the same message as the prior five days: the content is identical to the version already
refused, and the tool requires an explicit fresh fetch of the artifact URL to confirm before it
will accept the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars
`read` on this URL for this run for the same permission-prompt-hang reason as the prior six days,
and `force:true` again requires explicit human confirmation this run has no way to obtain, so
neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-11 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 11 entries (Sep 2 through Sep 12). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 11, now for a seventh consecutive
day with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now seven days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in seven days of identical daily escalation. Restating the
2026-09-09 through 2026-09-11 options rather than inventing a new one, since none of them have
been acted on: (a) grant a future run permission to use `read` on this specific URL with a human
available to approve the resulting prompt if it appears, (b) have a human manually republish
`ledger.html` once to reset the artifact's version state, or (c) reconsider whether
`ARTIFACT.md`'s blanket prohibition should instead be scoped to only the failure mode it was
written for, so a run can still fetch-then-publish in the same turn when a version conflict is
detected. The founder was already notified out-of-band about this on 2026-09-09; since nothing
material has changed since that notification (same wall, same unresolved options, no new
consequence), this run does not send a second one — repeating an already-delivered alert with no
new information would just be noise. If a human reads this and still hasn't acted, the 2026-09-09
notification stands as the live ask.

---

## 2026-09-11 — Same artifact publish conflict, sixth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
sixth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries Sep
2 through Sep 11) and confirmed the repo version is still a strict superset — the Sep 2–5 entries
match verbatim. Republished the repo file as the merge. That second attempt was refused too, with
the same message as the prior four days: the content is identical to the version already refused,
and the tool requires an explicit fresh fetch of the artifact URL to confirm before it will accept
the resend — functionally the `read` action. `overall/research/ARTIFACT.md` bars `read` on this
URL for this run for the same permission-prompt-hang reason as the prior five days, and
`force:true` again requires explicit human confirmation this run has no way to obtain, so neither
was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-10 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 10 entries (Sep 2 through Sep 11). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 10, now for a sixth consecutive
day with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now six days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in six days of identical daily escalation. Restating the
2026-09-09/09-10 options rather than inventing a new one, since none of them have been acted on:
(a) grant a future run permission to use `read` on this specific URL with a human available to
approve the resulting prompt if it appears, (b) have a human manually republish `ledger.html`
once to reset the artifact's version state, or (c) reconsider whether `ARTIFACT.md`'s blanket
prohibition should instead be scoped to only the failure mode it was written for, so a run can
still fetch-then-publish in the same turn when a version conflict is detected. The founder was
already notified out-of-band about this on 2026-09-09; since nothing material has changed since
that notification (same wall, same unresolved options, no new consequence), this run does not
send a second one — repeating an already-delivered alert with no new information would just be
noise. If a human reads this and still hasn't acted, the 2026-09-09 notification stands as the
live ask.

---

## 2026-09-10 — Same artifact publish conflict, fifth day running; not re-notifying since nothing changed

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly, still stuck at 4 entries
(Sep 2–5) — confirming the live page has not moved since the 2026-09-06 conflict began, now for a
fifth day. Compared that live HTML against the repo's `ledger.html` (already carrying entries Sep
2 through Sep 10) and confirmed the repo version is still a strict superset. Republished the repo
file as the merge. That second attempt was refused too, with the same message as the prior three
days: the content is identical to the version already refused, and the tool requires an explicit
fresh fetch of the artifact URL to confirm before it will accept the resend — functionally the
`read` action. `overall/research/ARTIFACT.md` bars `read` on this URL for this run for the same
permission-prompt-hang reason as the prior four days, and `force:true` again requires explicit
human confirmation this run has no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-09 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 9 entries (Sep 2 through Sep 10). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 9, now for a fifth consecutive day
with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now five days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in five days of identical daily escalation. Restating the
2026-09-09 options rather than inventing a new one, since none of them have been acted on: (a)
grant a future run permission to use `read` on this specific URL with a human available to
approve the resulting prompt if it appears, (b) have a human manually republish `ledger.html`
once to reset the artifact's version state, or (c) reconsider whether `ARTIFACT.md`'s blanket
prohibition should instead be scoped to only the failure mode it was written for, so a run can
still fetch-then-publish in the same turn when a version conflict is detected. The founder was
already notified out-of-band about this on 2026-09-09; since nothing material has changed since
that notification (same wall, same unresolved options, no new consequence), this run does not
send a second one — repeating an already-delivered alert with no new information would just be
noise. If a human reads this and still hasn't acted, the 2026-09-09 notification stands as the
live ask.

---

## 2026-09-09 — Same artifact publish conflict, fourth day running; still not using barred `read`/`force`

**Decision:** This run's first publish attempt was refused because the tool considered the live
artifact unviewed; the refusal handed over the live HTML directly (still stuck at 4 entries,
Sep 2–5 — confirming the live page has not moved since the 2026-09-06 conflict began). That
handoff is not the barred `read` action — it's the tool including the live version as part of
refusing a `publish` call, the same distinction 2026-09-08's entry relied on. Compared that live
HTML against the repo's `ledger.html` (already carrying entries Sep 2 through Sep 9) and
confirmed the repo version is still a strict superset — nothing in the live page's content is
missing from the merge. Republished the repo file as the merge. That second attempt was refused
too, with the same message as 2026-09-07 and 2026-09-08: the content is "identical to the version
already refused," and the tool requires an explicit fresh fetch of the artifact URL to confirm
before it will accept the resend — i.e., functionally the `read` action. `overall/research/
ARTIFACT.md` bars `read` on this URL for this run for the same permission-prompt-hang reason as
the prior three days, and `force:true` again requires explicit human confirmation this run has
no way to obtain, so neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 through 2026-09-08 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 8 entries (Sep 2 through Sep 9). No research content is lost; only the
live page is stale, still showing 4 entries against the repo's 8, now for a fourth consecutive
day with no forward progress.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now four days running, unresolved since first raised 2026-09-06:**
Nothing has changed about this wall in four days of identical daily escalation. Restating the
2026-09-08 options rather than inventing a new one, since none of them have been acted on: (a)
grant a future run permission to use `read` on this specific URL with a human available to
approve the resulting prompt if it appears, (b) have a human manually republish `ledger.html`
once to reset the artifact's version state, or (c) reconsider whether `ARTIFACT.md`'s blanket
prohibition should instead be scoped to only the failure mode it was written for, so a run can
still fetch-then-publish in the same turn when a version conflict is detected. Given four
consecutive unattended failures, this is flagged to the founder outside the repo as well this
run (push notification), since daily re-logging in `DECISIONS.md` alone has not produced action.

---

## 2026-09-08 — Same artifact publish conflict, third day running; still not using barred `read`/`force`

**Decision:** This run's first publish attempt was refused with the live artifact's actual HTML
included in the refusal (stuck at 4 entries, Sep 2–5 — confirming `LOG.md`'s account that the
Sep 6 and Sep 7 entries never made it live). That refusal is distinct from calling the barred
`read` action: it's the tool handing over the live version as part of refusing a `publish` call,
which `overall/research/ARTIFACT.md` does not forbid. Compared that live HTML against the
repo's `ledger.html` (which already carried entries for Sep 2 through 8) and found the repo
version already a strict superset — nothing in the live page's content was missing from the
merge. Republished the repo file as the merge. That second attempt was refused too, this time
saying the content was "identical to the version already refused" and instructing an explicit
re-fetch of the artifact URL to confirm — i.e., the `read` action — before it will accept the
resend. `overall/research/ARTIFACT.md` bars `read` on this URL for this run for the same reason
as the prior two days (risk of an unattended permission-prompt hang on a sensitive save path),
and `force:true` again requires explicit human confirmation this run has no way to obtain, so
neither was used.

**Why this is safe to leave unresolved for now:** Same as 2026-09-06 and 2026-09-07 —
`ledger.html` in the repo is the committed source of truth per `ARTIFACT.md`, and it now
correctly contains all 7 entries (Sep 2 through Sep 8). No research content is lost; only the
live page is stale, now showing 4 entries against the repo's 7.

**Reversible?** Yes. A human, or a future run with `read`/`force` permission (or one that starts
its very first artifact action of the session with an explicit fetch of the URL, satisfying the
tool's "confirm via fresh fetch" requirement before any publish attempt burns it), can republish
`ledger.html` from the repo to catch the live page up in one shot.

**Open item for the founder — now three days running:** The tool's own refusal message says the
fix is a fresh `read`/fetch of the URL; `ARTIFACT.md`'s prohibition on that action was written to
avoid a specific permission-prompt hang, but that prohibition is now the direct cause of three
consecutive stale-artifact days with no way for an unattended run to self-resolve. Recommend one
of: (a) grant a future run permission to use `read` on this specific URL with a human available
to approve the resulting prompt if it appears, (b) have a human manually republish `ledger.html`
once to reset the artifact's version state, or (c) reconsider whether `ARTIFACT.md`'s blanket
prohibition should instead be scoped to only the failure mode it was written for, so a run can
still fetch-then-publish in the same turn when a version conflict is detected.

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
