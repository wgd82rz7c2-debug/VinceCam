# VinceCam — Business Plan (working draft)

> Scaffolded for Duquesne New Venture Challenge Stage II (executive summary + short
> business plan, due 2027-02-14) and built to expand into the Stage III full plan
> (≤7,500 words, due 2027-04-04). Judging criteria from `../DUQUESNE_TIMELINE.md`:
> management team, problem/opportunity, solution, target market, implementation
> strategy, business model, financial outlook, exit pathways — this doc is organized
> to hit each one directly.
>
> Sections marked **[NEEDS FOUNDER INPUT]** are genuine gaps — real numbers or
> decisions only you can supply. Everything else is drafted from `../BASE_IDEA.md` and
> the competitor research in `research/`. Edit freely; this is a first pass.

---

## 1. Executive Summary

VinceCam is a Career Decision Intelligence platform for college business students. It
builds a living profile from a student's resume, stated preferences, what they actually
enjoy doing day to day, and where they want their career to go — then uses that profile
to rank careers, compare specific employers and locations within a career, and flag
realistic next steps. Unlike career-assessment tools that stop at "here are your top
matches," VinceCam continues into the decisions that actually determine outcomes:
which employer, which office, which posting — and updates itself as real internship and
job experience changes what a student knows about themselves.

We're starting with accounting and finance students, where recruiting is structured and
repeated internship/full-time decisions create natural reasons to return. Free for
students; long-term revenue comes from university career centers, who can serve more
students with structured, persistent decision support than a small advising staff can
offer alone. **[NEEDS FOUNDER INPUT: funding ask amount and use of funds, if this plan
is meant to solicit investment/prize capital toward a specific milestone.]**

---

## 2. The Problem

College business students have no shortage of career information — LinkedIn, Glassdoor,
O*NET, ChatGPT. The problem is turning fragmented information into one organized,
personal decision. Typical unanswered questions: What does FP&A actually do compared
with Treasury? Would I enjoy FDD more than External Audit? Is Company A actually better
for this role than Company B, or just more famous? After an internship changes what I
like, should my career ranking change? (Full list: `../BASE_IDEA.md` §1.)

---

## 3. The Solution

VinceCam separates four distinct dimensions of fit instead of collapsing them into one
opaque score:

| Dimension | Question it answers |
| --- | --- |
| Readiness | Can I realistically compete for this work today? |
| Work Fit / Enjoyment | Would I actually like doing this, day to day? |
| Conditions Fit | Does it match what I want (hours, pay, travel, location)? |
| Trajectory Fit | Does it move me toward the future I want? |

The product moves through three stages: **career ranking** → **employer comparison**
(entry difficulty, career signal, specialized experience — not just brand prestige) →
**location/posting fit**. After real internship or job experience, the profile updates
and the system explains exactly what changed and why. (Full model: `../BASE_IDEA.md`
§5–6, §26–45.)

---

## 4. Target Market

**Beachhead:** U.S. college accounting and finance students — strongest existing role
research, structured early-career recruiting, repeated internship/recruiting decisions
create natural return visits.

**Expansion path (only after the beachhead is proven):** other business majors → recent
grads/early-career workers → high schoolers → career changers → other professional
fields (engineering, healthcare, tech, law).

**[NEEDS FOUNDER INPUT: market sizing.** Rough TAM/SAM/SOM figures — e.g., number of
U.S. business undergrads, accounting/finance majors specifically, and a defensible
penetration assumption for the beachhead. `../BASE_IDEA.md` doesn't currently size the
market; judges will expect at least directional numbers with a source.]

---

## 5. Competitive Landscape

Full analysis: `../BASE_IDEA.md` §55–66 (CareerExplorer, general AI) and the dated files
in `research/` (resume-parsing APIs, pymetrics/Harver, Eightfold AI, Prentus, Forage,
and others, refreshed nightly).

**The core competitive fact:** every adjacent tool we've found does at most two of
VinceCam's three things — assess *(interests/personality → career match)*, place
*(resume → job posting)*, or develop *(virtual work experience, skills)*. None combine
resume-verified readiness + actual enjoyment signal + trajectory into one profile that
then follows the student through employer and location choice and updates from real
task-level experience. CareerExplorer is the closest assessment-stage competitor but
stops at "top career matches" — it doesn't have VinceCam's employer/location/posting
layer or longitudinal profile updates from actual work.

---

## 6. Differentiation

1. **Depth over breadth.** CareerExplorer covers 1,500+ careers; VinceCam goes deep on
   ~24 closely related business paths where the confusion (FP&A vs. Treasury vs.
   Internal Audit) is exactly the decision students are stuck on.
2. **Readiness kept separate from enjoyment.** A student can be told "you'd love this
   work but aren't currently competitive for it" — most tools conflate the two.
3. **The product doesn't stop at career match.** Employer, office, and posting-level
   comparison is the actual moat — see `../BASE_IDEA.md` §62.
4. **Longitudinal, not one-shot.** The profile updates from real internship/job
   experience, not just a retaken quiz.

---

## 7. Business Model

**Status: explicitly unvalidated** — `../BASE_IDEA.md` §67 and §77 (open design
questions 14–16) already flag this. Current hypotheses, not commitments:

- **Free core** for students — profile, career ranking, enough save/compare to build
  trust. Free must stay genuinely useful, not a stripped teaser.
- **Premium student features** (unvalidated): deeper company comparisons, skill-gap
  roadmaps, offer comparison, recruiting alerts.
- **One-time "Career Blueprint" product** (unvalidated): a paid, comprehensive
  report — top careers, employer/location targets, skill-development plan.
- **University/career-center licensing** — the most credible long-term revenue line:
  full student access + counselor dashboard + cohort analytics + outcome analytics.
  Since CareerExplorer already sells to universities, the pitch has to be a deeper
  decision-management value proposition, not "we also have an assessment."

**[NEEDS FOUNDER INPUT — this is the single biggest gap in the plan:**
- Actual price points (student premium, Career Blueprint, per-seat or per-student
  university licensing).
- Which revenue line is primary vs. supplementary.
- Unit economics: rough CAC (campus ambassadors? paid?), and what "enough students" per
  university looks like before the university-licensing pitch is credible.
Judges score "business model" directly — a plan with hypotheses but no numbers reads as
incomplete at Stage II.]

---

## 8. Go-to-Market / Implementation Strategy

Manual, relationship-driven early acquisition per `../BASE_IDEA.md` §73: student
organizations, professors, accounting/finance clubs, alumni, career-center contacts,
campus pilots, student ambassadors. Explicitly *not* paid acquisition before there's
evidence of profile completion, save/compare behavior, and return visits (validation
experiments GTM-001 through GTM-004 in §72).

**Natural first pilot:** Duquesne itself, given the founding team's Duquesne
affiliation and the DNVC relationship — the career center connection this competition
creates is itself a go-to-market opportunity, not just a funding source.
**[NEEDS FOUNDER INPUT: is a Duquesne career-center pilot actually being pursued, or is
that a future idea?]**

---

## 9. Financial Outlook

**[NEEDS FOUNDER INPUT — nothing exists here yet.** At minimum, Stage II likely expects:
- A simple revenue projection (even directional, 2–3 years) tied to the business-model
  assumptions above once they're set.
- Rough cost structure: what does it cost to build/run the product (data licensing —
  O*NET/CareerOneStop/BLS/BEA per `../BASE_IDEA.md` §49 — plus hosting, plus any paid
  acquisition later).
- If this plan supports a funding ask (DNVC prize money, or investment), what it would
  be used for and over what runway.
Per `../BASE_IDEA.md` §54's "No Fake Precision" principle, don't publish invented exact
figures — use ranges and state assumptions explicitly, the same way the product itself
is designed to show confidence/coverage instead of false precision.]

---

## 10. Exit Pathways

Not yet addressed anywhere in the project. For reference: CareerExplorer/Sokanu was
acquired by Penn Foster in 2021 (terms undisclosed; reported 10M+ annual users at
acquisition) — evidence the category has real strategic acquisition value, not proof of
VinceCam's own outcome. **[NEEDS FOUNDER INPUT: does the team have a point of view on
exit strategy (acquisition by an ed-tech/HR-tech player, career-services incumbent, or
long-term independent growth)? Judges score this explicitly — even a brief, honest
"too early to commit, but comparable exits exist in the category" is better than
silence.]**

---

## 11. Team

**[NEEDS FOUNDER INPUT — entirely blank.** Judges score "strength of the management
team" directly. Need: founder(s) and roles, relevant background/why this team,
confirmation of the Duquesne-affiliated member required for Stage III eligibility (see
`../DUQUESNE_TIMELINE.md` — already confirmed covered, but name/role should be in the
plan itself).]

---

## 12. Milestones / Roadmap

| Date | Milestone |
| --- | --- |
| 2026-11-15 | DNVC Stage I: written description + 1-min video (drafted, see `STAGE_I_DESCRIPTION.md` / `STAGE_I_VIDEO_SCRIPT.md`) |
| 2027-01-10 | Stage I results |
| 2027-02-14 | DNVC Stage II: exec summary + this business plan + 5-min video |
| 2027-03-01 | Stage II results |
| 2027-04-04 | DNVC Stage III: full plan + deck |
| 2027-04-10 | Final presentation |

**Product-side milestones** (not yet scheduled — `../BASE_IDEA.md` doesn't commit to an
implementation stack): the six `src/` modules (`resume-extract`, `preferences`,
`enjoyment`, `trajectory`, `scoring-engine`, `job-logic`) are currently empty scaffolding.
**[NEEDS FOUNDER INPUT: is there a working prototype planned before Stage II (Feb),
Stage III (April), or is this plan pitched as pre-product? That changes how
"implementation strategy" should be written.]**
