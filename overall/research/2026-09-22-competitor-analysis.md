# Competitor Analysis — 2026-09-22

Daily research routine, twenty-first entry (Sep 2 through Sep 22, one entry per day). Full
`overall/BASE_IDEA.md` re-read this run — no regression to placeholder/TBD content found; it
remains the full canonical spec described in `LOG.md`'s prior entries. `overall/research/ledger.html`
read directly from the repo per `ARTIFACT.md`.

**Tooling note:** `WebFetch` was blocked on every domain tried, including `example.com` — the
same total-outage shape first seen 2026-09-20, now a third consecutive day (2026-09-20 through
2026-09-22). `curl "$HTTPS_PROXY/__agentproxy/status"` shows the proxy itself healthy with zero
relay failures and full CA coverage, so the block sits above the proxy layer specifically for this
tool, not a network fault. Every finding below rests on `WebSearch` snippets only, unverified by
direct fetch.

## Competitors Found

### SkillMap Pro (skillmappro.com) — headline find

An AI "career intelligence platform" aimed explicitly at "students, pivoters, and professionals"
($4–24/mo subscription, free trial). It matches a user's work-experience-derived skills against
O*NET occupations, ranks candidate career paths by skill overlap with filters for salary/remote/
transition-timeline/growth-potential, and separately offers **career trajectory planning** and
**competency analysis** alongside resume/cover-letter/LinkedIn generation. It also keeps an
"achievement vault" — certifications, awards, projects — linking each stored skill to its
supporting evidence.

This is the closest match found in the whole 21-day series to VinceCam's *evidence-backed
Readiness + Trajectory* pairing specifically (as distinct from JOFI's Readiness+Work-Fit pairing,
9/5, or CoreFactors' enjoyment×competence pairing, 9/20): it ties a stored skill claim to cited
evidence (parallel to BASE_IDEA §8.4's evidence ladder) and separately plans a trajectory, not just
a static ranking. It still falls well short of VinceCam's architecture on every axis that matters
for the beachhead: fully generic across all occupations rather than scoped to a verified 24-career
business taxonomy; no enjoyment/Work-Fit dimension at all (skill overlap is competence-only, the
same blind spot CoreFactors' 9/20 entry flagged in the category generally); no company × role ×
location layer; and no mechanism to re-score from actual internship/job task-level experience —
"achievement vault" entries appear to be user-entered, not derived from a living profile that
updates itself. Neither core moat question — finance-specific sub-career fit scoring, or a true
profile-driven Company × Career × Location comparison / task-level re-scoring loop — is closed by
it.

### Also found (not logged as competitors)

- **Career Fit Test** (careerfittest.com, "trusted 25+ years," distinct company from the
  already-logged CareerFitter.com despite the near-identical name) — a classic SIMA-style
  60-skill card-sort: users react to their enjoyment level for each skill, producing a "motivated
  skills" code mapped to careers. A third instance (after Truity vs. MyPassion.AI, 9/07, and
  Testerly vs. CareerExplorer, 9/14–16) of the psychometric-quiz category containing two
  near-identically-named but independently-run competitors — worth a naming-collision note for
  VinceCam's own trademark search, nothing more. Same generic, occupation-agnostic,
  evidence-free shape as every other enjoyment-only quiz already logged.
- **Fika Jobs** (Stockholm, $4M raised, announced 2026-06-23) — an AI video-interview hiring
  marketplace: candidates do a 10-minute AI-agent interview from their LinkedIn profile, get
  turned into short video clips employers browse; free for candidates, 10% of first-year salary
  on hire. Same shape as Big 4 Talent (9/21) and Company.fit (9/13): a placement marketplace
  monetizing candidate discovery, not a career-discovery or fit-scoring product — no enjoyment,
  readiness, or trajectory dimension at all, just "can this person communicate well on camera."
  Logged only because its fee-on-hire economics are a fourth data point (after Big 4 Talent,
  Company.fit, Talentprise) for the "candidates free / employer pays on placement" monetization
  pattern, still judged a poor near-term fit for VinceCam's pre-decision positioning.
- **NeduAI SmartProfiles** — a "living profile" that pre-fills ~70% from a CV/LinkedIn and stays
  shareable across applications. Conceptually adjacent to BASE_IDEA §19's persistent/adaptable
  profile concept, but it is a static data-portability convenience (skills, experience, goals as
  free text), not a scored, evidence-laddered, four-dimension profile — no fit score of any kind.
- Searched directly, again, for a Big 4 internal service-line-matching/staffing tool (candidate
  preference vs. audit/tax/advisory assignment) — came back empty for a consecutive day; results
  were exclusively public-facing Big 4 career-page and AI-adoption content, nothing on an internal
  preference-based staffing algorithm.
- Searched directly for any 2026 funding round in career-fit/job-matching-beyond-keywords —
  nothing found this week; Fika Jobs (above) is a hiring-marketplace raise, not a fit-scoring one.
- Searched directly for enjoyment-vs-competence as explicitly separated, task-level scored
  dimensions (the CoreFactors precedent, 9/20) — found only generic secondary commentary (NACE
  competency frameworks, a general observation that interest and competence scores are not
  strongly correlated) rather than a second shipped product doing it; CoreFactors remains the only
  concrete precedent found in the series.

Both core moat questions — a competitor scoring fit specifically within finance/accounting
sub-careers using preference/enjoyment/trajectory signals (not keyword matching), and a
competitor operating a true profile-driven Company × Career × Location comparison or
task-level re-scoring loop — came back empty again today, the **21st consecutive day**.

## Differentiation Opportunities

- SkillMap Pro's "achievement vault" (evidence linked to each stored skill claim) is close enough
  to BASE_IDEA §8.4's evidence ladder that it is worth a one-line addition to BASE_IDEA's
  competitive-analysis section (§55–66) the next time that section is revised — a second
  named product (after JOFI, CoreFactors) validating "tie every capability claim to its source
  evidence" as a real, buildable, user-facing pattern rather than a purely internal data-modeling
  choice.
- SkillMap Pro also sharpens a pitch contrast worth adding alongside the existing
  CareerExplorer/AmplifyME/JOFI lines: SkillMap Pro tells a generalist what skills they already
  have and which occupations those skills transfer to; it never asks whether the person would
  *enjoy* doing that occupation's actual recurring work, and it has no finance-sub-career depth
  (Audit vs. Tax vs. FP&A vs. Treasury) at all. VinceCam's Work Fit dimension (BASE_IDEA §14) and
  24-career verified taxonomy (§21) are exactly the two things a skill-transferability tool like
  this structurally cannot offer.
- The Fika-Jobs/Big-4-Talent/Company.fit cluster (three fee-on-hire marketplaces logged in three
  days) is now a strong enough pattern to note explicitly in BASE_IDEA §67 as "adjacent business
  models VinceCam should not converge toward": all three sit downstream of a decision VinceCam is
  trying to help a student make *before* that student is even a candidate for a specific opening.
  Worth an explicit sentence distinguishing "VinceCam helps you decide what to pursue" from
  "these platforms help an employer discover you once you're pursuing it" for pitch and judge Q&A.

## Profitability Opportunities

- No new pricing anchor changes VinceCam's standing hypotheses (university licensing per §67,
  a one-time "Career Blueprint" report per the Truity/FindYou.io precedents). SkillMap Pro's
  $4–24/mo range is a fifth low-single-digit-to-mid-double-digit monthly subscription anchor for a
  student/early-career population (after Sonara $23.95/4wk, Jobright $39.99/mo, Truity's $29
  one-time, FindYou.io's ~$55 one-time) — reinforces that a monthly subscription above ~$25 is
  likely too high for this exact beachhead, and a one-time unlock in the $15–30 range remains the
  better-supported early experiment.
- The fee-on-hire cluster (Fika Jobs 10%, Big 4 Talent ~12.5%) is a second and third data point
  (after Company.fit) for what a future placement-adjacent revenue line could charge *if* VinceCam
  ever brokers an introduction once a user has a saved, targeted opportunity — still logged as a
  possible far-future Stage 3 lane, not a near-term recommendation, consistent with 9/21's framing.
- No action recommended on pricing this run beyond what's already logged; the open pricing
  questions (§77.14–16) remain unresolved and are not re-litigated here without new evidence.

## Open Questions for the founder

1. **Repeat of the 9/9-through-9/21 recommendation, now at 21 consecutive blank days on both core
   moat questions, including three separate runs (9/17, 9/20, 9/21) that specifically targeted
   the sharpest remaining fresh angles rather than generic ones:** this routine again recommends
   treating "no competitor scores finance sub-career fit using enjoyment/preference/trajectory
   signals, and no competitor operates VinceCam's Company × Career × Location comparison or a
   real task-level re-scoring loop" as settled pitch evidence, not a nightly open research
   question. This is restated rather than re-argued, since the evidence hasn't changed; a founder
   decision on this routine's own future cadence on those two specific questions is still
   unrecorded in `DECISIONS.md`.
2. **`WebFetch` has now been fully blocked (all domains, including `example.com`) for three
   consecutive days (2026-09-20 through 2026-09-22).** Every finding across this span, including
   today's SkillMap Pro headline, rests on `WebSearch` snippets only and is unverified against a
   primary source. If this is an intentional environment change, no action is needed beyond
   flagging it here (again); if unintentional, it's now degraded three straight days of research
   confidence and is worth a founder-level look at whatever governs this session's tool
   permissions.
3. No BASE_IDEA.md regression to placeholder/TBD content was found this run — restating per the
   task brief's instruction, since prior entries have consistently confirmed the document is in
   its full, filled-in canonical state, not because there was any indication otherwise today.
