# Work log

Newest entry at the top. Short entries: what changed, what it revealed, what's next.

---

## 2026-09-24 — Twenty-fourth competitor research entry: Working Eye's video-testimonial career discovery, FutureFit/entrext's enterprise-to-consumer pivot, NELVA AI's lifetime institutional license

Daily research routine's entry for 2026-09-24 (23rd entry actually filed in the ledger; entries
are one per day, Sep 2 through Sep 24 inclusive): `overall/research/2026-09-24-competitor-analysis.md`.
Delegated the search to a sub-agent, which tested `WebFetch` directly against five unrelated
domains (arxiv.org, unicloud360.com, emerald.com, en.wikipedia.org, crunchbase.com) — all five
failed identically with `EGRESS_BLOCKED`, and the proxy status endpoint again showed zero relay
failures, confirming the same blanket policy-level block seen 2026-09-20 through 2026-09-22 (not
attempted 2026-09-23). All findings rest on `WebSearch` snippets only. Found **Working Eye** (UK,
crowdfunded via a £75,000 Indiegogo raise), a video-testimonial careers-discovery platform pairing
AI recommendations with short films of real people doing real jobs — content curation, not a
modeled Work-Fit dimension, but a cheap idea worth borrowing for VinceCam's own career pages.
Found **FutureFit/entrext**, a newly surfaced *consumer* spinoff of the already-logged enterprise
FutureFit AI, marketed directly at students — mechanism and pricing unverified due to the
`WebFetch` block, but a notable go-to-market signal that a funded, enterprise-scale workforce
platform is moving downstream into VinceCam's exact beachhead. Found **NELVA AI**, which blends a
labor-market demand/growth signal into one composite score (not an independent axis, unlike
VinceCam's four-dimension split) and offers a new B2B pricing shape — one institutional license,
unlimited tests, for life — worth weighing against the still-open university-pricing question.
Dismissed UniCloud360/codingace.net's offer comparators (same commoditized bucket as
JobComparator.com et al.) and Fit First Technologies (pre-existing, same category as
pymetrics/Harver). No Big 4 internal service-line tool, no material 2026 career-fit funding round,
and no confirmed finance-specific multi-dimensional academic paper were found; one intriguingly
titled arXiv paper ("The Three Axes of Success") surfaced only as an unverified bibliography
citation and is flagged for manual follow-up outside this environment. Both core moat questions
(finance-specific sub-career fit scoring; a true profile-driven Company × Career × Location
comparison or task-level re-scoring loop) came back empty for the **23rd consecutive day**.
Updated `overall/research/ledger.html` (now 23 entries filed). **Artifact publish failed again**
— same version-conflict wall as 2026-09-06 through 2026-09-23, nineteenth day running; see
`DECISIONS.md`. The live artifact is now nineteen entries behind the repo file. Did not send a
second push notification since the founder was already notified about this exact, unresolved
block on 2026-09-09 and nothing material has changed since. No BASE_IDEA.md regression found;
full document re-read this run (4,155 lines, zero `TBD` hits). **Repo hygiene:** second clean start
running — session began on `main`, up to date with `origin/main`, working tree clean.

## 2026-09-23 — Twenty-third competitor research entry: Pivoto's four-driver work-alignment assessment, Gloat's transition-data trajectory precedent, clean repo state

Daily research routine's entry for 2026-09-23 (22nd entry actually filed in the ledger; entries
are one per day, Sep 2 through Sep 23 inclusive): `overall/research/2026-09-23-competitor-analysis.md`.
Per the task brief, `WebFetch` was not attempted this run (confirmed still blocked by network
egress policy); all findings rest on `WebSearch` snippets only, same posture as the prior four
runs. Found **Pivoto** (pivoto.tools), a ~15-minute self-report "Work Alignment Assessment"
scoring four separately-tracked drivers — Task Alignment, Growth Alignment, Environment Fit,
Energy Sustainability — into a one-time PDF report, marketed explicitly against personality-type
tests. It's a fresh, if generic, precedent for VinceCam's core bet that fit should be decomposed
into independently scored dimensions (Task/Growth/Environment loosely echo Work-Fit/Trajectory/
Conditions), but critically it has **no Readiness/competence pillar at all** — preference-only,
no capability evidence, no finance depth, no company/location layer, no living profile. Also
found **Gloat**, an enterprise internal-mobility platform whose "trajectory intelligence" predicts
next-role transitions from historical data — not a competitor (B2B, existing-employee mobility,
not pre-hire student discovery) but the clearest named mechanism yet for how a future
data-driven Trajectory Fit pillar could work. Dismissed CareerTakes.ai (Edkey) and a
RippleMatch-powered application flow as the same already-covered commodity resume-matching lane.
No Big 4 internal service-line tool, no career-fit funding round in the last 1–2 weeks (September
funding news dominated by biotech/health tech/AI infra), and no deployed 2026 academic system
doing finance sub-career disambiguation (only generic surveys and a TalentCLEF 2026 NLP workshop)
were found despite targeted searches. Both core moat questions (finance-specific sub-career fit
scoring; a true profile-driven Company × Career × Location comparison or task-level re-scoring
loop) came back empty for the **22nd consecutive day**. Updated `overall/research/ledger.html`
(now 22 entries filed). No BASE_IDEA.md regression found; full document re-read this run
(4,154 lines, zero `TBD` hits). **Repo hygiene:** unlike the last several runs, this session
started cleanly on `main`, up to date with `origin/main`, working tree clean — no detached-HEAD
recovery needed today, first clean start since before 2026-09-18.

## 2026-09-22 — Twenty-second competitor research entry: SkillMap Pro's evidence-linked skill vault plus trajectory planning, a fee-on-hire marketplace cluster, third straight total WebFetch outage

Daily research routine's entry for 2026-09-22 (21st entry actually filed in the ledger; entries
are one per day, Sep 2 through Sep 22 inclusive): `overall/research/2026-09-22-competitor-analysis.md`.
`WebFetch` was blocked on every domain tried, including `example.com` — the same total-outage
shape as 2026-09-20 and 2026-09-21, now a third consecutive day; the proxy status endpoint again
showed zero relay failures, so the block sits above the proxy layer specifically for this tool.
All findings rest on `WebSearch` snippets only. Found **SkillMap Pro** (skillmappro.com, $4–24/mo),
an AI career-intelligence platform matching work-derived skills to O*NET occupations with career
trajectory planning, competency analysis, and an evidence-linked "achievement vault" — the closest
match yet to VinceCam's evidence-backed Readiness + Trajectory pairing specifically, though fully
generic across occupations, with no enjoyment dimension, no company/location layer, and no
re-scoring from real work experience. Also found Career Fit Test (a third distinct, near-identically-
named competitor pair in this series), Fika Jobs (a $4M-funded AI video-interview hiring
marketplace — a fourth fee-on-hire data point, same downstream-of-the-decision category as Big 4
Talent and Company.fit), and NeduAI SmartProfiles (a static "living profile" convenience, not a
scored profile). No Big 4 internal staffing tool and no 2026 career-fit funding round found. Both
core moat questions (finance-specific sub-career fit scoring; a true profile-driven Company ×
Career × Location comparison or task-level re-scoring loop) came back empty for the 21st
consecutive day. Updated `overall/research/ledger.html` (now 21 entries filed; corrected the
stale "Entries filed" stat, which had been reading 19 against an actual 20 pre-existing entries).
**Artifact publish failed again** — same version-conflict wall as 2026-09-06 through 2026-09-21,
seventeenth day running; see `DECISIONS.md`. The live artifact is now seventeen entries behind the
repo file. Did not send a second push notification since the founder was already notified about
this exact, unresolved block on 2026-09-09 and nothing material has changed since. No BASE_IDEA.md
regression found; full document read this run. **Repo hygiene:** this run started with `HEAD`
detached at `e9728eb` (2026-09-21's commit) with local `main` five commits behind, at `70f0606`
(2026-09-16) — `origin/main` was already caught up this time. Fast-forwarded local `main` to the
detached tip before starting today's work; no data was at risk. See `DECISIONS.md` — this is the
fourth occurrence of this exact pattern (2026-09-18, 2026-09-19, 2026-09-21, 2026-09-22).

## 2026-09-21 — Twenty-first competitor research entry: Big 4 Talent's 19-dimension transparent recruiting score, second straight total WebFetch outage confirmed at proxy layer

Daily research routine's twenty-first entry: `overall/research/2026-09-21-competitor-analysis.md`.
Ran the search directly (no sub-agent delegation this run) against the brief's most pointed fresh
angles: finance sub-career disambiguation, separated enjoyment-vs-competence scoring at task
level, role-specific employer comparison, outcome-data re-scoring loops, Big-4/accounting-specific
tools, 2026 funding rounds in career-fit/job-matching, resume-parsing-API scoring vendors, and
internal service-line-matching tools. `WebSearch` worked normally; `WebFetch` was blocked on every
domain tried, including `example.com` — the same total-outage shape as 2026-09-20, now confirmed
a second consecutive day. This time checked `curl "$HTTPS_PROXY/__agentproxy/status"` directly:
the proxy reports healthy with zero relay failures and full CA coverage, so the block sits above
the proxy layer specifically for `WebFetch`, not a network or proxy fault — all findings below are
therefore `WebSearch`-snippet-only and marked unverified. Found **Big 4 Talent** (bigfourtalent.com,
founded Jan 2023 by Justin Marcus and Jason Allinder), a B2B2C recruiting marketplace exclusively
for Deloitte/PwC/EY/KPMG alumni that scores every candidate-to-opening match across 19 disclosed,
weighted dimensions (level, comp, skills, certs, industry, company size, commute) shown
transparently rather than as a black box — candidates free, employers pay ~12.5% on hire. It's the
most finance/accounting-specific, multi-dimension, transparent-scoring product found across the
whole 21-day series outside quiz tools, but it's a hiring/placement marketplace, not career
discovery: its dimensions are hiring logistics, not Readiness/Enjoyment/Conditions/Trajectory, and
it treats Big 4 alumni as one labor pool rather than disambiguating audit vs. tax vs. FP&A as
distinct career paths. Also checked and dismissed as non-competitors: **Freudly** (general
AI-therapist app with a generic finance-flavored quiz page), **Atlas CPA Index** (static,
non-personalized Big 4 editorial comparison), and **Joberney**/**Pin** (a general AI job-search
copilot and a B2B recruiter-sourcing embedding-matcher, respectively — same base-covered
categories as already-logged tools). No 2026 funding rounds, no Big 4 internal service-line-
matching tool, and no deployed (non-academic) outcome-data re-scoring engine were found despite
targeted searches. Both core moat questions (finance-specific sub-career fit scoring; a true
profile-driven Company × Career × Location comparison or task-level re-scoring loop) came back
empty for the 21st consecutive day — reinforcing, on a night that specifically targeted the
brief's sharpest fresh angles, the 2026-09-20 recommendation to treat the gap as settled pitch
evidence rather than a nightly open question. Updated `overall/research/ledger.html` (now 21
entries filed). No BASE_IDEA.md regression found; full document read this run. **Repo hygiene:**
this run started with `HEAD` detached at `88b5760` (2026-09-20's commit) with local `main` and
`origin/main` both five commits behind, at `70f0606` (2026-09-16) — the same recurring
detached-HEAD-behind-main failure shape flagged 2026-09-18 through 2026-09-19. Fast-forwarded
`main` to the detached tip and pushed before starting today's work; no data was at risk since the
detached commits were already-filed, unpushed prior entries. See `DECISIONS.md`.

## 2026-09-20 — Nineteenth competitor research entry: PathPilot's B2B2C launch, CoreFactors' dual-axis enjoyment×competence scoring, total WebFetch outage

Daily research routine's nineteenth entry: `overall/research/2026-09-20-competitor-analysis.md`.
Delegated the web search to a sub-agent briefed on VinceCam's architecture, the two standing
moat gaps, and the 100+ names already logged 2026-09-02 through 2026-09-19. `WebSearch` worked
normally, but `WebFetch` was blocked on **every domain tried today, including `example.com`** —
a more severe, general instance of the selective small-site blocking (Nodes.inc, Testerly)
running since 2026-09-13; the proxy status endpoint showed no relay failures, so this reads as a
policy-level block rather than a network fault. Found **PathPilot** (pathpilot.ai, launched
2026-09-17), a Canadian B2B2C skills-gap job-matching platform at real pilot scale (1,700+ job
seekers, 80+ practitioners, named partners) — not a direct competitor, but fresh cross-border
evidence that selling through an institutional intermediary that owns the target population
works as a channel, generalizing VinceCam's university-licensing hypothesis. Found **CoreFactors'
"Career Signals"** (a second, distinct product from the vendor logged 2026-09-12), which plots
each skill on two independent axes — enjoyment and competence — the closest mechanism-level
precedent in the whole series for VinceCam's own Readiness/Work-Fit separation, though generic-
skill-level and coach-administered rather than finance-sub-career-specific and self-serve. Also
found a second wave of commoditized free offer-comparison calculators (Careertics, MaxOfJob,
LoopCV) and InternTrack, a fourth distinct shape of structured work-exposure data nobody pipes
into a fit model. Both core moat questions (finance-specific sub-career fit scoring; a true
profile-driven Company × Career × Location comparison or task-level re-scoring loop) came back
empty for the 20th consecutive day — the research file recommends the founder consider this
settled evidence for pitch purposes and reconsider this routine's nightly cadence on those two
questions specifically. Updated `overall/research/ledger.html` (now 19 entries filed).
**Artifact publish failed again** — same version-conflict wall as 2026-09-06 through 2026-09-19,
fifteenth day running; see `DECISIONS.md`. The live artifact is now fifteen entries behind the
repo file. Did not send a second push notification since the founder was already notified about
this exact, unresolved block on 2026-09-09 and nothing material has changed since. No
BASE_IDEA.md regression found; full document read this run. **Repo hygiene:** this run started
with `HEAD` detached at `origin/main`'s tip with local `main` four commits behind; fast-forwarded
local `main` to match, no data at risk.

## 2026-09-19 — Eighteenth competitor research entry: FinanceFit's finance-archetype quiz, CFA Institute's ICAN pathway tool, Callings.ai's shallow company fit report

Daily research routine's eighteenth entry: `overall/research/2026-09-19-competitor-analysis.md`.
Delegated the web search to a sub-agent briefed on VinceCam's architecture, the two standing
moat gaps, and the 100+ names already logged 2026-09-02 through 2026-09-18. Found **FinanceFit**
("Which Finance Bro Are You," ~12,800 self-reported quiz-takers) sorting students into finance
sub-career archetypes — likely a single-pass personality quiz with no resume evidence or scored
dimensions; unverified since `WebFetch` to the site was blocked. Found the **CFA Institute's
ICAN Specialized Pathways Quiz**, a free, institutionally-backed values quiz reaching the same
student population through a professional-association channel — narrower than VinceCam's
24-career universe, but a new acquisition-channel idea (professional associations, not just
universities) for BASE_IDEA §73. Found **Callings.ai** (formerly JobHunters.ai), whose
per-company "fit report" feature is the shape closest to VinceCam's Stage 2 seen yet, but
appears to be generic resume-vs-company matching rather than a career-specific employer
comparison — a second "how not to compete" anchor for Stage 2. `WebFetch` to `nodes.inc` and
`testerly.com` remained blocked a seventh consecutive day (2026-09-13 through 2026-09-19), and
today also blocked the FinanceFit site, suggesting a general egress restriction. Both core moat
questions (finance-specific sub-career fit scoring; a true profile-driven Company × Career ×
Location comparison or task-level re-scoring loop) came back empty for the 19th consecutive
day. Updated `overall/research/ledger.html` (now 18 entries filed). **Repo hygiene:** this run
started with `HEAD` detached one commit ahead of `main` — the same failure shape as 2026-09-18's
recovery note — fast-forwarded and re-pushed; by push time `origin/main` had already caught up,
so nothing was at risk, but see `DECISIONS.md` for the recurrence flagged to the founder. No
BASE_IDEA.md regression found; full document read this run. See `DECISIONS.md` for whether
today's artifact-publish attempt succeeded or extended the standing conflict.

## 2026-09-18 — Seventeenth competitor research entry: AmplifyME, a mature at-scale finance-specific simulation incumbent, plus Talantir's explainable hiring output

Daily research routine's seventeenth entry: `overall/research/2026-09-18-competitor-analysis.md`.
`WebSearch` was available this run (alongside `WebFetch`) and surfaced the most material find of
the whole series: **AmplifyME**, a finance-only simulation platform founded 2009, serving
250,000+ students across 400+ universities with live Markets/Banking/Asset-Management/Quant
simulations, used by real banks (Morgan Stanley, UBS, Jefferies, RBC, Evercore) for assessment,
training, and a fast-track hiring pipeline. It is the first competitor in 18 days of searching to
combine genuine finance-specificity with real institutional scale — but has no Audit/Tax/FP&A/
Treasury tracks, no resume-based Readiness layer, and no four-dimension fit score, so the core
moat gap narrows without closing. Also found **Talantir** (EU work-simulation-to-hiring platform
whose employer output explains a candidate's reasoning process, not just a score — a second
precedent for VinceCam's explainability principle after JobMatchAI), and richer secondary-source
detail on the two standing unverified names (Nodes.inc now looks like a real B2C+B2B fit-score
product; Testerly's CareerExplorer-founder-origin story reconfirmed) though direct `WebFetch` to
both remained blocked a sixth consecutive day. Updated `overall/research/ledger.html` (now 17
entries filed). **Artifact publish failed again** — same version-conflict wall as 2026-09-06
through 2026-09-17, thirteenth day running; see `DECISIONS.md`. The live artifact is now thirteen
entries behind the repo file. Did not send a second push notification since the founder was
already notified about this exact, unresolved block on 2026-09-09 and nothing material has
changed since. No BASE_IDEA.md regression found; full document read this run.

## 2026-09-17 — Sixteenth competitor research entry: AI-generated career-simulation cluster, Territorium's posting-level skill match, 17th straight blank on the moat layers

Daily research routine's sixteenth entry: `overall/research/2026-09-17-competitor-analysis.md`.
Found a genuinely new mechanism rather than another quiz or matcher: a cluster of products
(Career Compass, ExploreYou, Simploy, newl) that infer work-fit signal from a user's choices
inside a synthetic, AI-generated task simulation rather than from self-report or real
employer-sponsored exposure — Simploy runs complete 3–4 week career simulations inside
AI-generated companies with performance analytics. A fifth distinct shape of task-level
work-exposure data (after Forage/Extern/GoSprout/generic internship apps), the first synthetic
one, but none finance-specific and none paired with resume-based Readiness or a company/location
layer; all sit one decision-stage earlier (major choice) than VinceCam's post-declaration
business-function disambiguation. Found Territorium's "Opportunity Fit Score," a live,
at-scale K12/higher-ed/workforce-board posting-level skill-gap matcher — pure skills/credential
matching, no enjoyment/trajectory dimension, but a useful reference for VinceCam's own
posting-override display. `WebFetch` remained blocked for `nodes.inc` and `testerly.com` for a
fifth consecutive day (2026-09-13 through 2026-09-17), and also blocked `territorium.com` and
`mycareercompass.fit` today. Both core moat questions (finance-specific sub-career fit scoring;
a true profile-driven Company × Career × Location comparison or task-level re-scoring loop) came
back empty for the 17th consecutive day. Updated `overall/research/ledger.html` (now 16 entries
filed). **Artifact publish failed again** — same version-conflict wall as 2026-09-06 through
2026-09-16, twelfth day running; see `DECISIONS.md`. The live artifact is now twelve entries
behind the repo file. Did not send a second push notification since the founder was already
notified about this exact, unresolved block on 2026-09-09 and nothing material has changed
since. No BASE_IDEA.md regression found; full document read this run.

## 2026-09-16 — Fifteenth competitor research entry: WayUp's resume-replacing profile, The Culture Factor's per-company culture tool, 16th straight blank on the moat layers

Daily research routine's fifteenth entry: `overall/research/2026-09-16-competitor-analysis.md`.
Found WayUp, a college-student job platform that replaces the resume with a self-reported
"Digital Profile" and soft-skills assessment feeding its match — same posting-match category as
Handshake/Simplify/Teal, but a new name and a concrete existence-proof that VinceCam's target
students already tolerate a lightweight personality questionnaire elsewhere. Found The Culture
Factor's "Company Comparison" tool, which infers a six-dimension culture report for any employer
from public digital signals rather than crowdsourced reviews — not a competitor, but a candidate
third data source for VinceCam's own Conditions/Career-Signal company record. Testerly's founder
story (original author of the Sokanu/CareerExplorer assessment, now marketing Testerly against a
precision limit in that same earlier work) firmed up further via the company's own first-person
comparison page surfaced in search, though still not independently fetched. `WebFetch` remained
blocked for both `nodes.inc` and `testerly.com` for a fourth consecutive day (2026-09-13 through
2026-09-16). Both core moat questions (finance-specific sub-career fit scoring; a true
profile-driven Company × Career × Location comparison or task-level re-scoring loop) came back
empty for the 16th consecutive day. Updated `overall/research/ledger.html` (now 15 entries
filed). **Artifact publish failed again** — same version-conflict wall as 2026-09-06 through
2026-09-15, eleventh day running; see `DECISIONS.md`. The live artifact is now eleven entries
behind the repo file. Did not send a second push notification since the founder was already
notified about this exact, unresolved block on 2026-09-09 and nothing material has changed
since. No BASE_IDEA.md regression found; full document read this run.

## 2026-09-15 — Fourteenth competitor research entry: FutureFit AI's funded resume-to-pathway pipeline, 15th straight blank on the moat layers

Daily research routine's fourteenth entry: `overall/research/2026-09-15-competitor-analysis.md`.
Found FutureFit AI, an Achieve Partners-backed workforce platform extracting transferable skills
from resumes and recommending career pathways via labor-market data, deployed at real
government-workforce scale (~50,000 served in Connecticut, 85% claimed placement) — B2B2G, not
student-facing, and confirms the same wall as every other name found so far (no enjoyment layer,
no trajectory layer, no company × location comparison) even at that funding and scale level.
Filled in yesterday's thin CareerHub.com mention with its official April 2026 launch detail
(explicit resume-vs-keyword scoring). Confirmed CareerfIT as a distinct, small product from the
already-logged CareerFitter despite the near-identical name — no new mechanism. `WebFetch`
remained blocked for both `nodes.inc` and `testerly.com` for a third consecutive day
(2026-09-13 through 2026-09-15), so both remain unverified pending restored fetch access. Both
core moat questions (finance-specific sub-career fit scoring; a true profile-driven Company ×
Career × Location comparison or task-level re-scoring loop) came back empty for the 15th
consecutive day. Updated `overall/research/ledger.html` (now 14 entries filed). **Artifact publish
failed again** — same version-conflict wall as 2026-09-06 through 2026-09-14, tenth day running;
see `DECISIONS.md`. The live artifact is now ten entries behind the repo file. Did not send a
second push notification since the founder was already notified about this exact, unresolved
block on 2026-09-09 and nothing material has changed since.

---

## 2026-09-14 — Thirteenth competitor research entry: Testerly's founder is CareerExplorer's own creator, GoSprout's compliance-grade task data, 14th straight blank on the moat layers

Daily research routine's thirteenth entry: `overall/research/2026-09-14-competitor-analysis.md`.
`WebFetch` was blocked again today for `testerly.com` specifically, a second straight day of egress
trouble, so today's Testerly finding rests on secondary sources rather than a direct fetch. It
revises yesterday's "suspected white-label" hypothesis: secondary sources describe Testerly's
founder as the original assessment scientist (PhD, I/O psychology) who built the Sokanu/
CareerExplorer instrument itself before leaving it, now marketing his own independent instrument
against his own earlier work — not a reseller, a second instance (after MyPassion.AI vs. Truity)
of competitors marketing against each other inside the commoditizing quiz category. Found GoSprout,
a compliance-grade apprenticeship/internship tracking platform (sponsor-verified hours, tasks,
evaluations; automates state/federal RAPIDS/WIPS/PIRL reporting) — a fourth distinct shape of
task-level work-exposure data after Forage/Extern, worth a line in future data-partnership
thinking though no export path was found. Flagged Nodes.inc's "AI Fit Score Calculator" content
(explicitly claims trajectory/culture/growth-potential scoring) as likely SEO/lead-gen marketing
rather than a verified product, pending direct-fetch confirmation. Found JobMatchAI, an ACL 2026
academic system demonstrating the same compute-score-then-explain architecture BASE_IDEA §53–54
already specifies — not a competitor, but a citable precedent for VinceCam's explainability
design. Both core moat questions (finance-specific sub-career fit scoring; a true profile-driven
Company × Career × Location comparison or task-level re-scoring loop) came back empty for the 14th
consecutive day. Updated `overall/research/ledger.html` (now 13 entries filed). **Artifact publish
failed again** — same version-conflict wall as 2026-09-06 through 2026-09-13, ninth day running;
see `DECISIONS.md`. The live artifact is now nine entries behind the repo file. Did not send a
second push notification since the founder was already notified about this exact, unresolved block
on 2026-09-09 and nothing material has changed since. No BASE_IDEA.md regression found; full
document read this run.

## 2026-09-13 — Twelfth competitor research entry: HireGlide, Company.fit, a suspected CareerExplorer white-label, and a 13th straight blank on the moat layers

Daily research routine's twelfth entry: `overall/research/2026-09-13-competitor-analysis.md`.
WebFetch was unavailable this run (every attempt returned `EGRESS_BLOCKED`), so all findings rest
on search snippets only — flagged as lower-confidence than usual. Found Testerly, whose per-career
"fit report" pages describe an interest taxonomy matching the Sokanu/CareerExplorer engine,
raising an unverified hypothesis that it's a white-label reseller rather than an independent
competitor — worth a direct-fetch verification once network access is restored. Found Company.fit
(free candidate profile scored as a match % against live postings, employers pay per verified
hire — a fourth distinct B2B monetization lane) and two more general AI job boards (HireGlide,
CareerHub.com), all in the already-commoditized resume-plus-preferences category. Found
JobComparator.com and a cluster of offer-comparison-calculator clones — a second concrete
"how not to compete" anchor for Stage 3 after FindSkill.ai (9/11) — and Wing/SLI.pro, a personal-
branding coaching product whose "Career Intelligence Platform" branding is close enough to
VinceCam's own positioning language to flag for pitch messaging, though it's not a functional
competitor. Checked Apuphi, Extern, CoreFactors, RippleMatch/JobGet, CareerExplorer, and Handshake
AI for 2026 updates; found none that close either moat gap (Handshake's Spring '26 release adds
employer-side analytics and a student AI job-fit chat assistant, still no finance disambiguation
or task-level feedback loop — recommended downgrading it to a monthly re-check). Both moat
questions (finance-specific sub-career fit scoring; a true profile-driven Company × Career ×
Location comparison or task-level re-scoring loop) came back empty for the 13th consecutive day;
explicitly re-raised the Stage 2/3-vs-Stage-1-polish prioritization question given that streak.
Updated `overall/research/ledger.html` (now 12 entries filed). **Artifact publish failed again**
— same version-conflict wall as 2026-09-06 through 2026-09-12, eighth day running; see
`DECISIONS.md`. The live artifact is now eight entries behind the repo file. Did not send a second
push notification since the founder was already notified about this exact, unresolved block on
2026-09-09 and nothing material has changed since. No BASE_IDEA.md regression found; full document
read this run.

## 2026-09-12 — Eleventh competitor research entry: Extern's paid externships, CoreFactors' avoidance scoring, and a FindSkill.ai correction

Daily research routine's eleventh entry: `overall/research/2026-09-12-competitor-analysis.md`.
Found Extern (formerly Paragon One; YC-backed) selling paid, real-employer remote externships
in finance and other business functions — a second, higher-fidelity live example (after Forage)
of a company monetizing the "real task-level work exposure" step BASE_IDEA wants feeding
VinceCam's profile, and a new build-vs-partner question (import structured externship outcomes
as evidence, vs. waiting on VinceCam's own longitudinal base). Found CoreFactors' Career Path
(B2B, updated April 2026), which scores Preference and Avoidance as two independent dimensions —
the clearest external validation yet for BASE_IDEA §14's "strongly dislike" design choice, and a
third B2B go-to-market lane (coaches) distinct from university licensing and Talentprise's
per-unlock model. Found OnJob.io (live-ATS-fed match scoring naming the missing skill per
listing) as a concrete implementation pattern for posting freshness (§25) and gap-naming output
(§46), though same resume-keyword-match category as prior entries. Corrected the 2026-09-11 entry:
direct verification found FindSkill.ai is a stateless one-shot template catalog with no login or
persistent profile, not a near-miss on VinceCam's Stage 3 shape as framed yesterday — the
underlying "no competitor operates the persistent Company × Career × Location layer" conclusion
stands. Updated `overall/research/ledger.html` (now 11 entries filed). **Artifact publish failed
again** — same version-conflict wall as 2026-09-06 through 2026-09-11, seventh day running; see
`DECISIONS.md`. The live artifact is now seven entries behind the repo file. Did not send a
second push notification since the founder was already notified about this exact, unresolved
block on 2026-09-09 and nothing material has changed since. No BASE_IDEA.md regression found;
full document read this run. Did not re-raise the Stage 2/3-vs-Stage-1-polish prioritization
question a seventh time since the evidence hasn't changed since 2026-09-11; it remains
unresolved in `DECISIONS.md`.

## 2026-09-11 — Tenth competitor research entry: Apuphi's feedback loop, FindSkill.ai's offer calculator, ten-for-ten on the moat layers

Daily research routine's tenth entry: `overall/research/2026-09-11-competitor-analysis.md`.
Found Apuphi (India; the first mechanism in ten nights that re-scores a profile from real
third-party feedback — employer interview feedback, not internship task-level feedback — a
partial precedent for the §19 re-scoring loop) and FindSkill.ai's Job Offer Comparison Tool
(closest artifact yet to VinceCam's Stage 3 shape, but a static, non-profile-driven calculator;
description unverified beyond search snippets since direct fetch was blocked by network policy).
Also found Tsenta and CareerTakes.ai (more auto-apply/resume-matching copilots, same category as
prior entries) and a material update — RippleMatch was acquired by JobGet on 2026-05-28. Tenth
consecutive day with no competitor found scoring fit specifically within finance/accounting
careers or operating a true profile-driven Company × Career × Location comparison layer.
Recommended in the research file and ledger entry that the founder record a decision on the
long-standing Stage 2/3-vs-Stage-1-polish prioritization question (raised five times since
2026-09-05 without one) — did not decide it myself, since that is a founder-level product call,
not something this routine has standing to resolve. Updated `overall/research/ledger.html` (now
10 entries filed). **Artifact publish failed again** — same version-conflict wall as 2026-09-06
through 2026-09-10, sixth day running; see `DECISIONS.md`. The live artifact is now six entries
behind the repo file. Did not send a second push notification since the founder was already
notified about this exact, unresolved block on 2026-09-09 and nothing material has changed
since. No BASE_IDEA.md regression found; full document read this run.

## 2026-09-10 — Ninth competitor research entry: ZipRecruiter's Phil, Talentpluto, and nine-for-nine on the moat layers

Daily research routine's ninth entry: `overall/research/2026-09-10-competitor-analysis.md`.
Found ZipRecruiter's Phil (conversational AI career advisor at large consumer scale, same
preference-to-posting shape as Jobright/Sonara/Indeed Career Scout) and Talentpluto (a genuinely
new pattern: a voice AI agent turning a 10-minute conversation into a profile queryable by other
AI agents — raises a new open question about candidate-consented profile sharing with outside
agents/employers), plus more B2B skills-assessment vendors (Testlify, WeCP, Vervoe, same category
as Accountests) and one more enterprise internal-mobility name (TalentGuard). Ninth straight day
with no competitor found scoring fit specifically within finance/accounting careers, operating a
Company × Career × Location comparison layer, or re-scoring from real post-experience feedback —
this entry stops re-arguing that evidence nightly and only flags that the founder's prioritization
decision is still unrecorded. Updated `overall/research/ledger.html` (now 9 entries filed).
**Artifact publish failed again** — same version-conflict wall as 2026-09-06 through 2026-09-09,
fifth day running; see `DECISIONS.md`. The live artifact is now five entries behind the repo file.
Did not send a second push notification since the founder was already notified about this exact,
unresolved block on 2026-09-09 and nothing material has changed since. No BASE_IDEA.md regression
found; full document read this run.

## 2026-09-09 — Eighth competitor research entry: FindYou.io, Talentprise, and eight-for-eight on the moat layers

Daily research routine's eighth entry: `overall/research/2026-09-09-competitor-analysis.md`.
Found FindYou.io (adaptive Big Five/RIASEC/values psychometric test, $4/~$55 no-subscription
pricing — a second precedent alongside Truity for one-time paid reports) and Talentprise
(resume+preference profile matched to recruiter searches, candidates free, employers pay
per-unlock — a new B2B monetization pattern), plus more AI job-search copilots (Careerflow,
Huntr, Jobscan, Kickresume, Zippia) and psychometric quizzes (16Personalities Premium Career
Suite, YouScience, PathSource, MyPlan.com), none combining resume evidence with enjoyment/
trajectory. Eighth straight day with no competitor found scoring fit specifically within
finance/accounting careers, operating a Company × Career × Location comparison layer, or
re-scoring from real post-experience feedback — strong enough now that the research file
recommends resolving the "prioritize Stage 2/3 vs. Stage 1 polish" question rather than
re-raising it a sixth time. Updated `overall/research/ledger.html` (now 8 entries filed).
**Artifact publish failed again** — same version-conflict wall as 2026-09-06 through 2026-09-08,
fourth day running; see `DECISIONS.md`. The live artifact is now four entries behind the repo
file. Sent a push notification to the founder about this recurring block, since daily re-logging
alone hasn't produced action. No BASE_IDEA.md regression found; full document read this run.

## 2026-09-08 — Seventh competitor research entry: Apt AI, Accountests, and seven-for-seven on the moat layers

Daily research routine's seventh entry: `overall/research/2026-09-08-competitor-analysis.md`.
Found Apt AI (freemium personality-quiz + bolted-on resume tools, closest yet to VinceCam's
joint Readiness/Work-Fit pairing but still two separate features) and Accountests (first
accounting-specific personality instrument found, but B2B employer-hiring-side, not a
candidate-facing competitor), plus a cluster of ungated finance-career marketing quizzes and
Indeed Career Scout (new AI career coach, same marketplace-optimization shape as Handshake AI
and LinkedIn Career Explorer). Seventh straight day with no competitor found operating the
Company × Career × Location × Posting layer or re-scoring from real post-experience feedback.
Updated `overall/research/ledger.html` (now 7 entries filed) but **could not republish the
artifact** — same version-conflict wall as 2026-09-06 and 2026-09-07, third day running; see
`DECISIONS.md`. The live artifact is now three entries behind the repo file.

## 2026-09-07 — Sixth competitor research entry: Truity's static personality report vs. MyPassion.AI

Daily research routine's sixth entry: `overall/research/2026-09-07-competitor-analysis.md`.
Found Truity's Career Personality Profiler (Big Five + RIASEC, $29 one-time report, 25M+ users
at scale — validates a one-time-paid-report business model close to BASE_IDEA's "Career
Blueprint" hypothesis) and MyPassion.AI (small bootstrapped competitor explicitly marketing a
childhood-pattern-based enjoyment critique against static personality quizzes). Sixth straight
day with no accounting/finance-specific fit-scoring competitor found. Updated
`overall/research/ledger.html` (6 entries filed, including the 2026-09-06 entry that a prior
run's publish conflict had left off the live page) but **could not republish the artifact** —
same version-conflict refusal as 2026-09-06, whose only offered fix (the `read` action) is
barred by `ARTIFACT.md` this run; see `DECISIONS.md`. The live artifact is now two entries
behind the repo file.

---

## 2026-09-06 — Fifth competitor research entry: Lightcast Career Coach and the apply-stage tools

Daily research routine's fifth entry: `overall/research/2026-09-06-competitor-analysis.md`.
Found Lightcast Career Coach (labor-market-data company Lightcast's occupation/degree-program
fit assessment, deployed at 300+ colleges — the first genuine fit-scoring incumbent found in
the university channel, vs. 12Twenty/Symplicity's pure logistics), plus Simplify.jobs and Teal
HQ (AI job-search copilots with resume-match scores, already installed by VinceCam's own
beachhead students today) and LinkedIn Career Explorer (free public skill-adjacency tool,
further proof trajectory mapping alone has no moat). Updated `overall/research/ledger.html`
(now 5 entries filed) but **could not republish the artifact** — the Artifact tool refused the
publish over a version conflict and its suggested fixes (`read`, `force`) are both barred for
this routine; see `DECISIONS.md` 2026-09-06 entry. The live artifact page is stale until a
future run or a human republishes it from this file.

**Next:** a human (or a future run once the conflict clears) should republish
`overall/research/ledger.html` to the artifact URL in `overall/research/ARTIFACT.md`, checking
first whether the artifact received an out-of-band edit that needs merging rather than
overwriting.

## 2026-09-05 — Fourth competitor research entry: JOFI's occupation-level fit score vs. Welcome to the Jungle's values matching

Daily research routine's fourth entry: `overall/research/2026-09-05-competitor-analysis.md`.
Found JOFI Assessments (DoD-derived psychometric instrument, evidence-based job-fit score
across all 923 O*NET occupations, sold to workforce boards/colleges/career coaches) — the
closest match yet to VinceCam's Readiness + Work Fit pairing, but still occupation-level
only with no company/location/posting layer or re-scoring from lived experience. Also found
Welcome to the Jungle (formerly Otta, ~1.7M users) matching on skills + values + culture at
the posting level. Five straight passes now confirm no competitor operates VinceCam's full
Company × Career × Location × Posting layer. Updated `overall/research/ledger.html` (now 4
entries filed) and republished the artifact.

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
