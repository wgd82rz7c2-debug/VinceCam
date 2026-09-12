# Competitor Research — 2026-09-12

Eleventh entry in the daily research routine. `overall/BASE_IDEA.md` was read in full this run
(all 86 sections); no regression to placeholder/TBD content was found — the canonical spec is
intact and unchanged in substance since the prior read. This entry searched six angles, all
explicitly excluding the 75+ names already logged 2026-09-02 through 2026-09-11 (see
`overall/research/ledger.html` for the full roster), plus a follow-up verification of one
2026-09-11 finding whose description was flagged as unconfirmed.

## Competitors Found

### Extern (formerly Paragon One) — YC-backed remote externships, paid "next experience" pipeline

Y Combinator-backed (also Foundation Capital, Launch Fund, University Ventures, Learn Capital).
Pivoted from "Paragon One," which sold a career-center-as-a-service coaching platform, into
**Extern**: short, remote, project-based "externships" that let an employer engage hundreds of
students for far less cost than a traditional internship, across finance, marketing, technology,
and other business functions, partnering with Fortune 500 companies and startups. Extern reports
70% of externs are hired into an intern or full-time role within 12 months of completing the
program.

This is the second live example (after Forage, logged 2026-09-02) of a company monetizing the
exact "give a student real task-level work exposure" step that BASE_IDEA §46/§62.10 wants to feed
into VinceCam's Readiness/Work-Fit re-scoring — but the two are structurally different threats.
Forage is free, employer-sponsored, high-volume, low-fidelity (a self-contained simulation).
Extern is a paid, lower-volume, higher-fidelity externship with a real company and a real
hiring outcome attached. Neither turns the completed experience into a scored profile update the
way BASE_IDEA's evidence ladder (§8.4) and evidence-priority rule (§19) describe — Extern's value
proposition stops at "did the company like you enough to hire you," not "what did this externship
teach VinceCam about your capabilities and what you enjoyed." No mechanism was found on Extern's
public materials for exporting a structured record of what was actually done, or capturing
enjoyment ratings task-by-task.

### CoreFactors Career Path — explicit Preference *and* Avoidance scoring, updated April 2026

A B2B instrument sold to career-development practitioners and coaches (not candidate-facing
direct-to-consumer). Its April 2026 update scores both **Preference** and **Avoidance**
independently across 11 Occupational Activity Groupings (Business/Management,
Business/Financial, Digital Data, Mechanical, Scientific, Artistic, Social/Group Involvement,
Home and Nature, Individual/Personal Service, Governmental Service, Health and Medical) plus 6
broader Global Interest Areas, rather than inferring "avoid" as simply the low end of one
preference scale. CoreFactors' own materials cite Prefer/Avoid correlations of only -0.5 to -0.7
— i.e., what a person actively avoids is not fully predictable from what they say they prefer,
and the gap is where they place its diagnostic value.

This is the clearest external validation found in eleven days of research for a specific,
narrow BASE_IDEA design choice: §14's "Strongly dislike → avoid direction, importance 100%"
mapping, which already treats avoidance as informationally distinct from mere low preference
rather than collapsing it onto one dial. CoreFactors is occupation-cluster-level (not VinceCam's
24-career business taxonomy), has no resume/evidence layer, no company/location layer, and no
re-scoring from lived work experience — the by-now-familiar boundary — but it is a second
credentialed practitioner-facing precedent (after JOFI, 2026-09-05) that scored, explicit
avoidance is worth building deliberately rather than assumed to be redundant with a preference
scale.

### OnJob.io — live-ATS-fed match scoring that names the missing skill per job

An AI recruiting platform matching one candidate profile against 20,000+ live job listings
pulled directly from employer ATS feeds — postings disappear from OnJob.io the moment the
employer closes them at the source, rather than lingering as stale inventory the way many job
boards do. Its match score names the *specific* skills separating the candidate from a full
match on each listing, and the platform claims 3.1x more interview call-backs and a 94% success
rate for its users. Mechanically, this is the same resume/keyword-vs-posting match-score category
already logged for Jobright, Sonara, Simplify.jobs, and Teal (2026-09-02, 04, 06) — it does not
touch enjoyment, conditions, or trajectory — but the live-feed sourcing and per-listing missing-
skill breakdown are both concrete, working examples of two specific mechanics BASE_IDEA's own
design calls for elsewhere: posting freshness/expiry (§25) and "largest readiness gaps" output
(§46), here implemented at the keyword level rather than VinceCam's evidence-ladder level.

## Correction to the 2026-09-11 entry: FindSkill.ai

2026-09-11's entry described FindSkill.ai's Job Offer Comparison Tool as the closest single
artifact yet to VinceCam's Stage 3 shape, while flagging the description as search-snippet-only
and unverified. Direct verification was possible this run: FindSkill.ai is not a persistent
product with its own user accounts or profile state. It is a static catalog of individually
addressable "AI skill" template pages — Job Offer Comparison Tool, Career Pivot Simulator, Career
Pivot Risk Calculator, Non-Compete Loophole Finder, and dozens more under a "Learn AI for Your
Job" banner — each one a self-contained prompt/worksheet a visitor runs once, with no login, no
saved profile, and no connection between pages. This *lowers* rather than raises FindSkill.ai's
competitive relevance: the 2026-09-11 framing of it as a near-miss on Stage 3 should be revised
to "an unrelated one-shot content page that happens to share Stage 3's subject matter," not a
product with any persistence to differentiate against. No change to the underlying conclusion
that no competitor operates VinceCam's persistent, profile-driven Company × Career × Location
layer.

## Also found, lower relevance

- A cluster of one-shot "AI job displacement risk" calculators (JobForesight, What About AI,
  Prosumely's Career Transition Feasibility Calculator, Loopcv, SolidAITech, TripleTen) —
  answers "will AI take my job," not "which job/company/location fits me." Different question
  entirely from anything in BASE_IDEA; noted only because several share FindSkill.ai's
  single-page-tool shape and are easy to mistake for fit-matchers on first search-snippet read.
- CareerFitter's "FIT Score" (100,000+ calculations against 1,000+ careers) and My-Career-Path.com
  (RIASEC + 500 career matches + AI coach, free) — both already-commoditized general career-quiz
  shapes, same category repeatedly logged since 2026-09-02; no material new mechanism.

## Differentiation Opportunities

1. **Extern sharpens, rather than closes, the "next experience → profile update" gap.** A
   VinceCam integration or partnership angle exists here that doesn't exist with Forage: Extern
   externships are paid, lower-volume, and already produce a real employer hiring signal per
   student — exactly the kind of task-level, real-world evidence BASE_IDEA §19/§46 wants feeding
   the profile, and unlike Forage's self-contained simulations, an externship has a defined
   employer and function that could map directly onto VinceCam's Company × Career schema (§23
   Level 2). Worth a founder decision on whether to pursue a data-partnership conversation with
   Extern (import structured externship outcomes as Readiness/Work-Fit evidence) rather than
   building an equivalent real-experience pipeline from zero.
2. **CoreFactors validates building explicit avoidance capture, not just a bidirectional
   preference dial, into the Work Fit questionnaire (§14).** VinceCam's current design already
   does this implicitly via the "Strongly dislike" tier: recommend explicitly labeling and
   surfacing avoidance as its own signal in the UI/output (e.g., "activities to avoid" as a
   distinct output section, not just a negative-weighted preference), since the practitioner-side
   research CoreFactors cites suggests this is where satisfaction-relevant signal concentrates
   that a single preference scale would miss.
3. **OnJob.io's live-ATS-feed sourcing is a concrete pattern worth adopting for VinceCam's own
   posting layer (§45 Specific Posting Layer).** Rather than manually re-scraping/re-checking
   postings on a fixed cadence (§25), sourcing directly from employer ATS feeds where available
   would give VinceCam the same "a role disappears the moment it's actually closed" freshness
   guarantee without inventing new infrastructure — an implementation detail to fold into the
   eventual data-source stack (§49.6), not a new competitive threat.

## Profitability Opportunities

1. **Extern is a proof of willingness-to-pay for structured real-work exposure among employers**,
   distinct from BASE_IDEA's existing revenue hypotheses (university licensing, direct-to-student
   Career Blueprint). If VinceCam's Career Board (§47) eventually recommends specific next
   experiences to close a readiness gap (§46), a referral or data-exchange arrangement with an
   Extern-like externship provider is a plausible non-dilutive revenue/partnership line that
   doesn't require VinceCam to build or staff its own externship marketplace — flagged as a
   business-development idea, not a scoring or ranking feature (must stay outside the ranking-
   independence rule, §67, if any commission changes hands).
2. **CoreFactors' B2B-to-career-coaches channel is a third go-to-market lane distinct from
   university licensing and Talentprise's per-unlock model** (both already logged): selling a
   VinceCam-derived Career Path/Work-Fit report as a tool independent career coaches and
   counselors buy per-client, alongside — not instead of — the university-wide license
   hypothesis. Worth a line in the eventual pricing-model open question (§77 item 14) rather than
   a new open question of its own.
3. **The FindSkill.ai correction is itself a profitability signal, read the other way.** A site
   built from disposable, stateless, one-shot "AI skill" template pages can apparently attract
   enough search traffic to rank for "job offer comparison tool" and similar queries with zero
   persistent product behind it. That is weak evidence of real demand for the *questions* VinceCam
   answers (offer comparison, career pivot risk) even when the supply is this thin — useful as an
   SEO/content-marketing data point (cheap, disposable comparison pages draw searchers) rather
   than as a competitive product concern.

## Open Questions for the Founder

- The Stage 2/3-vs-Stage-1-polish prioritization question has now been raised in six of the last
  eight entries (2026-09-05, 07, 08, 09, 10, 11) without a recorded decision in `DECISIONS.md`.
  This entry does not raise it a seventh time as a fresh question — the evidence for it has not
  changed since 2026-09-11 — but notes it remains unresolved.
- New, narrower question from today's research: should VinceCam pursue a data-partnership
  conversation with a real-externship provider (Extern or similar) to source structured
  task-level evidence, rather than building or waiting for its own longitudinal user base to
  reach a size where that evidence is self-generated? This is a build-vs-partner question
  distinct from the previously-logged build-vs-license questions (resume parsing, psychometric
  instruments, labor-market data), since no comparable licensable dataset exists here — it would
  be a direct partnership or acquisition-of-data-access conversation.
- The artifact-publish version-conflict (`overall/research/ledger.html` vs. the live Competitor
  Ledger artifact) has now recurred for six consecutive prior days (2026-09-06 through
  2026-09-11); see `DECISIONS.md` for this run's outcome and whether it has changed.
