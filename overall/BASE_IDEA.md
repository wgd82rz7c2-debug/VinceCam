# Camvince — Current Canonical Product Idea

**Canonical current-state specification**  
**Date:** September 1, 2026  
**Purpose:** Capture the entire current Camvince concept in one internally consistent document, including the product, user profile, scoring logic, data model, data sources, company/location/posting layers, adaptable profile, business model, competitive differentiation, validation plan, and contradictions/deprecations.

> Editable living document — the source of truth every module under `src/` (`resume-extract/`,
> `preferences/`, `enjoyment/`, `trajectory/`, `scoring-engine/`, `job-logic/`) should trace back
> to. Update it in place when the idea changes; record *why* a change was made in `../DECISIONS.md`
> if it reverses or invalidates something written here. A future validation agent checks that each
> module's supporting info doesn't drift from what's written here.

---

## 0. Read This First — What Is Canonical

This document is intended to be the **current source of truth for the Camvince idea as of September 1, 2026**.

Several older Camvince files contain ideas that were correct when written but have since been changed. Those old files are useful as decision history, but they must **not override this specification** when they conflict with it.

### Source-precedence rule

When two Camvince artifacts disagree, use this order:

1. **This document — `Camvince_Current_Canonical_Idea_2026-09-01.md`**
2. **`Camvince Matching Model Reworked - Scoring Detail.xlsx` — September 1, 2026**
3. **`Role Database - Vincent.docx` — verified 24-career universe, deep source check August 22, 2026**
4. **The current Expanded Agent Ready Business Plan** for product, market, workflow, career pages, company pages, retention, validation, and business-model concepts that do not conflict with items 1–3
5. Older scoring configuration workbooks, flows, contradiction logs, stress tests, and prototypes as **historical/reference material only**

### Important consequence

Older files that say the primary Overall Fit formula is:

> 45% Readiness + 35% Career Match + 20% Preference Fit

or that present:

> Career Match + Readiness + Potential + Preference Fit + Overall Fit + Ideal Fit

as the current primary scoring architecture are **historical versions**.

The latest September 1 scoring model instead separates the Stage 1 career recommendation into:

- **Adjusted Readiness**
- **Conditions Fit**
- **Work Fit / Enjoyment**
- **Trajectory Fit**

and currently combines them as:

- **25% Adjusted Readiness**
- **15% Conditions Fit**
- **35% Work Fit / Enjoyment**
- **25% Trajectory Fit**

Those percentages are a **prototype configuration**, not a scientifically validated final formula.

### Contradiction status

After applying the source-precedence rule above, **this document is internally consistent**. I found historical conflicts in older Camvince artifacts and explicitly resolve them in the contradiction-audit section near the end of this document.

That is different from claiming that every old file has already been physically rewritten. It has not. Old files should be treated as stale wherever this document marks a concept as deprecated.

### Competitive status

Camvince has **significant overlap with CareerExplorer at the career-assessment and career-ranking stage**. It would not be sufficiently differentiated if the product stopped at:

> profile/assessment → top careers → career information.

The current Camvince architecture is meaningfully different **only because the product continues beyond career discovery** into:

> current readiness → company × career comparison → location/office → specific opportunity → entry difficulty → career signal → specialized experience → career trajectory → skill gaps/next step → longitudinal profile updates from actual work experience.

Based on CareerExplorer's current public product materials reviewed on September 1, 2026, I did **not** find evidence that CareerExplorer's core public product provides the same integrated company × role × location decision layer, person-relative employer entry-difficulty layer, employer-role specialized-experience model, or task-level longitudinal experience feedback loop envisioned for Camvince. CareerExplorer may have internal or unreleased capabilities that are not publicly documented, so Camvince should never claim knowledge of features that CareerExplorer does not publicly disclose.

---

# 1. The Core Problem

College students can already find:

- job postings on LinkedIn and Handshake,
- employee reviews on Glassdoor and similar sites,
- career descriptions through O*NET, BLS, CareerOneStop, CareerExplorer, Google, YouTube, Reddit, career centers, alumni, and professors,
- personalized explanations from ChatGPT and other general AI assistants.

The information problem is therefore **not simply that career information does not exist**.

The more important problem Camvince is trying to solve is:

> **Students have fragmented information but still struggle to turn it into an organized, personalized career decision.**

Typical questions include:

- What does FP&A actually do compared with Treasury?
- Would I enjoy FDD more than External Audit?
- Which careers fit the work I actually enjoy?
- Which careers am I currently qualified for?
- Which careers fit me theoretically but are unrealistic right now?
- Which careers could become realistic if I build one or two missing capabilities?
- Which company is best for this specific career?
- Is Company A actually better for this role than Company B, or is it just a more famous company?
- Is an employer prestigious in general or does the **specific employer × role combination** carry strong career signal?
- Which company would give me the specific skills I want?
- Which office/city is strongest for the industry I care about?
- What is the difference between Amazon FP&A in Arlington and Amazon FP&A in Seattle?
- Does this exact posting fit my background and preferences?
- Where do people commonly go after this path?
- What should I do next to improve my options?
- After I complete an internship and learn what I actually like, should my career ranking change?

Camvince is designed to turn those questions into a **structured, repeatable, source-backed decision workflow**.

---

# 2. What Camvince Is

The strongest current description is:

> **Camvince is a Career Decision Intelligence platform that helps early-career users decide what to do, where to do it, and what to do next as their experience evolves.**

A shorter competitive description is:

> **Career discovery is the starting point. Career navigation is the product.**

Another useful framing:

- **O*NET helps describe what work is.**
- **CareerExplorer helps identify careers that may fit a person.**
- **Camvince is intended to help decide which career move makes sense now, which employer/location/opportunity makes sense within it, and what the next move should be.**

Camvince should not be marketed as simply:

- an AI career quiz,
- a personality test,
- a job board,
- a resume scorer,
- a chatbot,
- a static career encyclopedia,
- a prestige ranking,
- an offer-probability calculator.

The system combines several functions, but the product value is the **decision layer connecting them**.

---

# 3. What Camvince Is Not

## 3.1 Not a job board

LinkedIn and Handshake primarily help users **find and apply to opportunities**.

Camvince should primarily help users answer:

> Should I pursue this kind of opportunity in the first place?

Job listings can appear in Camvince later, but job inventory is not the core moat.

## 3.2 Not a generic career test

CareerExplorer already has a sophisticated assessment, psychometric methodology, machine learning, labor-market data, and a large career library.

Camvince should not try to win by saying:

> "We also give you a list of careers."

## 3.3 Not a pure resume-to-job matcher

Resume matching alone overweights what someone has done and can trap the person in their existing path.

A student may be highly qualified for audit while strongly disliking audit work.

Camvince must keep:

- **capability/readiness**
- **work enjoyment**
- **job conditions**
- **future trajectory**

separate.

## 3.4 Not an exact probability engine

Camvince should not claim:

> "You have a 13.7% chance at Goldman Sachs."

unless Camvince later obtains strong, representative applicant/offer data that actually support a probability model.

Instead, it can use transparent categories such as:

- Accessible
- Moderately Competitive
- Competitive
- Highly Competitive
- Extremely Competitive

and separately show:

> Your current readiness relative to this opportunity.

## 3.5 Not a universal prestige score

A company name should not automatically improve a user's Fit.

For example:

> Goldman Sachs Investment Banking

and

> Goldman Sachs Compliance

should not receive identical career-signal logic simply because both use the Goldman Sachs name.

Company reputation must be **role-specific when possible**.

## 3.6 Not a system that invents missing facts

If Camvince does not know:

- exact hours,
- exact travel,
- office-specific pay,
- exact promotion timing,
- a user's SQL ability,
- or a career transition rate,

the answer is:

> **Unknown / inherited / estimated with confidence**

not a fabricated midpoint.

---

# 4. Beachhead Customer and Expansion

## 4.1 First customer

The initial beachhead is:

> **U.S. college business students**

Accounting and finance students are the easiest first test group because:

- the current role universe and research are strongest there,
- many roles have structured early-career recruiting,
- students make repeated internship/recruiting decisions,
- company differences matter,
- there are clear capability and recruiting signals,
- the founders can realistically reach initial users in this population.

This is a **beachhead**, not a permanent market limit.

## 4.2 Expansion path

Only after Camvince proves useful and repeatable should it expand to:

1. other business majors,
2. recent business graduates / early-career workers,
3. high-school students,
4. career changers,
5. additional professional fields such as engineering, healthcare, technology, law, etc.

The product should **not broaden merely to make the TAM slide larger**.

## 4.3 Highest-pain decision moments

Camvince should appear when the user has a real decision:

- before choosing an internship track,
- before recruiting season,
- when deciding between career families,
- when comparing employers,
- when comparing locations,
- when comparing offers,
- after an internship changes what the user thinks they like,
- when a new skill or certification changes realistic options,
- when the user wants to make a lateral/next career move.

---

# 5. The Core Product Architecture

The product is intentionally hierarchical.

## Stage 1 — Career / Role Decision

Main question:

> **What should I do?**

The user is compared against careers **before company or city is allowed to distort the career ranking**.

Examples:

- FP&A
- Treasury
- External Audit
- Internal Audit
- Valuation
- Transaction Advisory / FDD
- Commercial Banking
- Investment Banking

Output:

- career ranking,
- Readiness,
- Evidence Coverage / Confidence,
- Work Fit,
- Conditions Fit,
- Trajectory Fit,
- strongest reasons,
- main tradeoffs,
- missing information,
- next high-value question when needed.

## Stage 2 — Company Decision Within a Career

Main question:

> **Where should I do this kind of work?**

After the user chooses/saves a career, Camvince compares employers offering that career.

A company should not enter Stage 1 just because the company is famous.

The company layer should eventually show separate dimensions such as:

- Fit for You,
- Entry Difficulty / Difficulty for You,
- Career Signal,
- Specialized Experience,
- Conditions,
- Trajectory.

## Stage 3 — Location / Office / Actual Opportunity

Main question:

> **Does this specific opportunity make sense for me?**

The model becomes increasingly specific:

> Career → Company × Career → Office/Location → Actual Posting

A reliable posting-specific fact overrides the broader inherited assumption.

## Stage 4 — Experience and Next Decision

After the user actually does the work:

> Internship / job / class / project → what did you learn? → profile update → re-ranking → next move.

This makes Camvince an ongoing career-navigation product instead of a one-time test.

---

# 6. The User Profile — Four Separate Dimensions

The profile is not one mysterious "Career DNA score."

It contains distinct information that answers distinct questions.

## A. Readiness

Question:

> **Can this person realistically perform or compete for this work today?**

Readiness comes from demonstrated evidence such as:

- education,
- major,
- relevant knowledge,
- experience,
- tools/systems,
- quantitative work,
- research,
- writing,
- presentation,
- client/customer work,
- stakeholder work,
- controls/testing,
- process improvement,
- project coordination,
- operations,
- sales/persuasion,
- leadership,
- ownership.

Readiness is primarily evidence-based.

It must **not** infer what the person enjoys.

## B. Work Fit / Enjoyment

Question:

> **Would this person likely enjoy the actual recurring work?**

Examples:

- future-focused analysis,
- detail checking,
- client interaction,
- process improvement,
- persuasion,
- routine,
- ambiguity,
- ownership,
- deadline pressure,
- independent deep work.

This comes from explicit user preferences and, increasingly, from actual experience.

It must **not** be inferred from resume competence.

Being good at audit testing does not mean someone likes audit testing.

## C. Conditions Fit

Question:

> **Does this work/opportunity provide the conditions the user consciously wants?**

Examples:

- hours,
- busy-period intensity,
- schedule predictability,
- travel,
- remote/hybrid/in-person,
- compensation,
- variable compensation,
- company size,
- training/promotion,
- location.

## D. Trajectory Fit

Question:

> **Does this path move the user toward the future they want?**

Examples:

- career optionality,
- long-term compensation growth,
- management path,
- selective-employer access,
- specialist depth,
- geographic portability,
- industry portability,
- internal promotion,
- entrepreneurship,
- employer/career signal.

Trajectory is **probabilistic and evidence-based**, never a guarantee.

---

# 7. Onboarding Philosophy

Camvince should **show value before asking for every possible answer**.

The intended progressive flow is:

1. Upload resume or enter experience manually.
2. Extract obvious facts and evidence.
3. Ask only essential missing questions.
4. Produce a first-pass career ranking.
5. Ask deeper preference questions as they become useful.
6. If two careers are close, ask a discriminating tie-breaker rather than a generic extra questionnaire.
7. After the user saves a career, ask only questions that materially improve company/opportunity comparison.
8. Refresh the profile before recruiting cycles or after meaningful new experience.

The user should not face a giant assessment simply because the database contains many possible attributes.

---

# 8. Resume Parsing — Production Design

The current workbook's Excel/SAP section is a **demo**, not the production limit.

The production parser must extract **all supported evidence categories**, dynamically.

## 8.1 Direct factual fields

Examples:

- degree type,
- degree progress,
- major / field,
- graduation date,
- GPA when present,
- credentials/licenses,
- courses when present,
- employers,
- titles,
- job/internship dates,
- duration,
- industry exposure,
- project names,
- scope,
- quantified impact.

Direct facts should not require a self-rating if the resume already supports them.

## 8.2 Capability categories

The broad current readiness framework includes at least:

1. Education progress
2. GPA where relevant
3. Credentials / licenses
4. Accounting knowledge
5. Finance knowledge
6. Data / analytics knowledge
7. Marketing / customer knowledge
8. Operations / supply-chain knowledge
9. HR / people knowledge
10. Excel / spreadsheet analysis
11. ERP / accounting systems
12. Data tools — SQL / BI / Python
13. Quantitative analysis
14. Modeling / forecasting
15. Research
16. Writing / documentation
17. Presentation
18. External client / customer interaction
19. Internal stakeholder / cross-functional work
20. Controls / compliance / testing
21. Process improvement
22. Project coordination
23. Sales / persuasion
24. Operational execution
25. Leadership
26. Ownership / decision responsibility

The architecture should remain extensible. A new resume phrase should normally map to an existing canonical capability rather than create a duplicate attribute.

## 8.3 Evidence flow

The production chain is:

> **Resume evidence → clarification when necessary → confirmed capability value → backend value → role requirement comparison → Readiness → Overall Career Fit**

There should not be a second disconnected "hidden estimate" after the user confirms a capability.

## 8.4 Capability depth

A universal human-readable evidence ladder is preferable to vague self-rating:

- **0 — No evidence**
- **1 — Exposure / assisted**
- **2 — Performed with guidance**
- **3 — Performed independently**
- **4 — Owned complex work**
- **5 — Led / reviewed / was accountable for the outcome**

The backend can normalize this to a 0–100 scale, but the UI should explain the level rather than imply false precision.

## 8.5 Resume evidence examples

Resume phrase:

> "Analyzed results and variances"

Possible normalized capability:

> Quantitative Analysis

Follow-up only if depth is unclear:

> "What was the highest level of this work you handled personally?"

Resume phrase:

> "Worked with clients"

Normalized capability:

> External Client / Customer Work

Follow-up:

> "How independently did you handle client interactions?"

Resume phrase:

> "Automated a process"

Normalized capability:

> Process Improvement / Automation

Follow-up:

> "Which part of the solution did you personally own?"

Resume phrase:

> "Coordinated teams and deadlines"

Normalized capability:

> Project Coordination

Resume phrase:

> "Led a project"

Normalized capability:

> Leadership / Ownership

The system should not treat the word **led** as automatically meaning expert-level ownership.

---

# 9. Systems / Software — Exact Tool + Transferable Family

A major current design decision is the **hybrid exact-system + capability-family model**.

The parser extracts only tools actually supported by evidence.

Examples:

| Exact system | Capability family |
|---|---|
| Excel / Google Sheets | Spreadsheet Analysis |
| Power BI / Tableau / Looker | BI & Visualization |
| SAP / Oracle / NetSuite | ERP Systems |
| SQL / Snowflake / BigQuery | Data Query / Database |
| Python / R / VBA | Programming / Automation |
| Salesforce / HubSpot | CRM |
| Jira / Asana / Monday | Project / Workflow Tools |
| PowerPoint / Google Slides | Presentation Tools |

## Why both are needed

Suppose the user has SAP experience.

### Job asks for generic ERP experience

Camvince can use:

> ERP Systems capability

Result:

> transferable credit.

### Job asks specifically for SAP

Camvince uses:

> exact SAP evidence + ERP-family evidence.

Result:

> direct match.

### Job asks specifically for Oracle

Camvince must **not convert SAP into Oracle**.

It can say:

> ERP-family experience is transferable, but Oracle specifically is unknown.

This is more realistic than either extreme:

- treating all ERP systems as identical, or
- refusing to recognize transferable experience.

## Current system-use confirmation scale

When depth is unclear:

- **10** — Used once or twice; needed help
- **30** — Used occasionally; followed instructions
- **55** — Used regularly; needed help sometimes
- **80** — Used regularly; handled normal work independently
- **100** — Used throughout the role; handled difficult work independently

Again, these are backend standardization values, not claims that a person is "80% good at Excel."

---

# 10. Missing Resume Data

The rule is:

> **Unknown ≠ zero.**

If a resume does not mention SQL, the system should not automatically say:

> SQL ability = 0.

It should say:

> SQL = Unknown.

If SQL is important for a decision, Camvince can ask a targeted question later.

Missing evidence reduces **Coverage / Confidence**, not the person's assumed competence.

This prevents a sparse resume from being artificially punished.

---

# 11. User Editing and Confirmation

The user should edit **normal-language facts and answers**, not internal IDs or formula cells.

This reconciles two older product ideas:

- "show extracted information and let the user correct it,"
- "derived attributes remain backend."

Both can be true.

Example:

> Camvince extracts graduation date = May 2027.

The UI can ask:

> "We found May 2027 as your expected graduation date. Is that correct?"

The user corrects the **answer/fact**.

Then the system re-derives any affected recruiting-timing attributes.

The user should not see or edit:

> `ED-GRAD = .74`

or a hidden canonical Attribute ID.

---

# 12. Conditions / Preference Inputs

Current conditions questions include:

1. Maximum normal-week hours
2. Busy-period overtime tolerance
3. Desired schedule predictability
4. Travel tolerance
5. Work arrangement
6. Variable/performance-pay tolerance
7. Minimum acceptable starting salary
8. Company-size preference
9. Growth/change/stability preference
10. Training/promotion importance

Location is handled primarily **after a career is selected** so that a city preference does not determine which career the user should theoretically pursue.

## Neutrality rule

For preference questions:

- **No preference** → ranking weight 0
- **Not important** → ranking weight 0

A neutral answer should not pull every fit score toward 50.

---

# 13. Location Preferences

Location should be treated as a **user preference**, not as the same concept as labor-market opportunity.

These are separate:

### Location Fit

> How much does the user personally want to live/work there?

### Industry / Market Opportunity

> How strong is that market for the industry or career context?

Example:

A user may strongly prefer Pittsburgh.

Dallas may have stronger concentration in a particular industry.

The model should be able to say both:

> Pittsburgh is your stronger personal location preference.

and

> Dallas currently has stronger industry concentration for this target sector.

It should not silently merge those into one mysterious city score.

---

# 14. Work Fit / Enjoyment Questions

The current model uses concrete work activities rather than vague labels such as "you are an ENTJ."

Core current work-fit concepts:

1. Analyze numbers/data to understand what happened
2. Use numbers to plan future outcomes
3. Check details for small errors
4. Research unfamiliar topics
5. Write detailed explanations
6. Present conclusions
7. Talk with outside clients/customers
8. Build professional relationships
9. Persuade / handle objections / sell ideas
10. Improve inefficient processes
11. Coordinate people/tasks/deadlines
12. Check work against rules/standards
13. Keep day-to-day operations running
14. Help/coach/recruit/develop people
15. Do recurring/repeatable work
16. Work on changing topics/projects
17. Work without clear instructions
18. Work under tight deadlines
19. Own recommendations/decisions
20. Solve problems collaboratively
21. Work independently for long periods
22. Work toward clear personal performance targets

## Response logic

A useful current mapping is:

- **Strongly dislike** → avoid direction, importance 100%
- **Dislike** → avoid direction, importance ~70%
- **Neutral** → ranking weight 0
- **Enjoy** → prefer more, importance ~70%
- **Strongly enjoy** → prefer more, importance 100%

The role has a corresponding **activity intensity**.

The comparison happens only at scoring time.

---

# 15. Role Fingerprints and Differentiation

A career must have a **work fingerprint**, not just a generic job description.

Important cross-role discriminators include:

- past-focused vs future-focused work,
- rules vs judgment,
- internal vs external interaction,
- analysis vs relationship work,
- routine vs project variety,
- quantitative intensity,
- persuasion/selling,
- detail/error sensitivity,
- ambiguity,
- decision ownership,
- deadline/pressure intensity,
- independent vs collaborative work,
- process/operations orientation,
- writing/documentation,
- presenting/storytelling,
- client service,
- technology/data intensity,
- type of recurring work product.

Each role should store:

1. **Activity intensity**
2. **Role salience / importance**

A characteristic that barely varies across careers should not dominate the ranking merely because it is measured.

The model can eventually weight an attribute conceptually as:

> User importance × role salience × cross-role discrimination.

---

# 16. Dynamic Tie-Breaker Questions

If the top careers are very close, Camvince should not force the user to answer another 50 generic questions.

Instead:

1. Identify which characteristic most separates the top candidates.
2. Ask one plain-English tradeoff question.
3. Recalculate.
4. Repeat only if still useful.

Potential tie-breakers:

- past vs future focus,
- rules vs judgment,
- internal vs external work,
- recurring process vs project variety,
- analysis vs persuasion,
- independent vs collaborative,
- detailed checking vs open-ended problem solving,
- ownership vs execution.

Tie-breakers are optional production logic. They were intentionally removed from the concise stress-test UI because they were unnecessary for basic model testing.

---

# 17. Trajectory Profile

Trajectory is independent of present-day enjoyment.

A user can enjoy a job but reject it because it does not lead where they want.

Current future-priority dimensions include:

1. Career Optionality
2. Long-Term Pay Growth
3. Management Path
4. Selective Employer Access
5. Specialist Depth
6. Geographic Portability
7. Industry Portability
8. Internal Promotion
9. Entrepreneurship Potential
10. Employer Brand / Career Signal

Industry interests are mainly a **Stage 2** factor after the career is selected because most business careers can exist across multiple industries.

Current industry list includes:

- Technology
- Financial Services
- Healthcare
- Consumer / Retail
- Manufacturing / Industrial
- Energy / Utilities
- Real Estate / Construction
- Transportation / Logistics
- Government / Public Sector
- Media / Entertainment
- Professional Services
- Defense / Aerospace

---

# 18. Career Trajectory / Exit Data

Trajectory should be based on **observed accessibility and path strength**, not deterministic claims.

Do not say:

> "Audit guarantees an FP&A exit."

Prefer:

> "FP&A is an observed adjacent transition from external audit, but the strength of the path depends on experience, employer, skills, market, and individual choices."

Future transition data can include:

- starting career,
- starting employer,
- starting location/seniority where reliable,
- next career,
- next employer,
- time to transition,
- sample size,
- transition rate or relative strength,
- confidence.

Potential data sources:

- licensed workforce-transition data,
- Camvince's own longitudinal user outcomes,
- later institution/employer outcomes data if appropriately licensed.

Camvince should **not build its core commercial transition database by unauthorized LinkedIn scraping**.

---

# 19. The Adaptable / Living Profile

This is one of the most important parts of the current idea.

The profile is not meant to be a test result frozen at age 20.

It should evolve when the user gains real experience.

## Profile areas that can change

### Readiness can change because of:

- internship,
- full-time role,
- class,
- project,
- certification,
- new tool,
- new responsibility,
- promotion,
- leadership experience.

### Work Fit can change because of:

- tasks actually enjoyed,
- tasks disliked,
- repeated exposure showing prior assumptions were wrong,
- new responsibilities.

### Conditions Fit can change because of:

- desired hours,
- remote/hybrid preference,
- pay needs,
- location,
- travel tolerance,
- family/lifestyle needs.

### Trajectory can change because of:

- new long-term goals,
- desire for management,
- desire for entrepreneurship,
- preference for specialization,
- changed industry interest,
- changed importance of employer signal.

## Example

Before an audit internship, a student may rank:

1. External Audit
2. Internal Audit
3. Tax
4. FP&A

During/after the internship, Camvince learns:

- accounting readiness ↑
- controls/testing readiness ↑
- stakeholder experience ↑
- process-improvement preference ↑
- repetitive testing preference ↓
- client-service preference ↑
- future-focused analysis preference ↑

The next ranking might become:

1. FP&A
2. FDD
3. Internal Audit
4. Valuation
5. External Audit

The important point is not the exact ranking.

The important point is that Camvince can explain:

> **what changed, which evidence changed it, and why the recommendation changed.**

## Evidence priority

Behavior should not silently overwrite explicit user statements.

A good rule:

1. direct confirmed user answer,
2. repeated real-experience evidence,
3. resume/behavioral inference,
4. low-confidence personality/supporting inference.

If actual experience suggests a meaningful preference change, Camvince can ask:

> "You repeatedly marked recurring testing as one of your least-favorite activities. Should we update your preference for recurring compliance/testing work?"

The user confirms the meaningful profile change.

---

# 20. Persistent Career Identity and History

The system should preserve history rather than overwrite the user's past.

Recommended identity model:

- **Permanent User ID** — never changes
- **Profile Version** — increments when meaningful profile state changes
- optional **profile fingerprint / Dynamic Match ID** — identifies the normalized score-relevant state used for a result
- **Model Version** — records which scoring rules produced the result
- **Career/job data version or timestamp** — records which job-market data were used

This makes it possible to explain:

> "Your FP&A recommendation changed from 76 to 87 because your profile changed and the model used newer evidence."

rather than producing unexplained score drift.

The old concept of encoding visible traits directly into a readable Match ID such as `ae12` is deprecated.

---

# 21. Verified Career Universe

The current verified primary universe contains **24 entry-level U.S.-focused business career paths**.

1. External Audit
2. Internal Audit
3. Tax
4. Corporate Accounting
5. Forensic Accounting / Fraud Investigation
6. FP&A
7. Treasury
8. Investment Banking
9. Corporate Banking
10. Commercial Banking
11. Investment / Equity Research
12. Asset Management
13. Wealth Management / Financial Planning
14. Transaction Advisory / Financial Due Diligence
15. Valuation
16. Management Consulting
17. Risk Advisory
18. Financial Risk
19. Compliance
20. Market Research / Marketing Analytics
21. Supply Chain / Logistics
22. Human Resources
23. Sales Development / Business Development
24. Project Management / Project Coordination

The Role Database's deep source check supports retaining all 24 in the frozen primary universe.

## Important taxonomy rules

### "Financial Analyst" is not one career

It may refer to:

- FP&A,
- operations finance,
- treasury,
- credit,
- investments,
- other finance.

Camvince must map by **team and responsibilities**, not title alone.

### "Business Analyst" is not one career

It may refer to:

- consulting,
- systems/IT,
- operations,
- strategy,
- analytics,
- process improvement.

Again, map by actual work.

### "Operations" is too broad

Do not create a universal Operations profile unless narrowed.

### Leadership Development Program is a recruiting program

The underlying rotation may map to:

- finance,
- operations,
- sales,
- HR,
- general management.

Map the actual career content.

### Commercial Credit Analyst

Treat as an entry title within:

> Commercial Banking / Credit.

### Corporate Development

It is a legitimate career, but the verified role universe currently keeps it outside the frozen primary entry-level list because broad direct-undergraduate entry is less standardized.

---

# 22. Career Data Evidence Standard

The verified role database uses an evidence-first hierarchy.

## Tier 1 — Stable occupational evidence

Examples:

- career definitions,
- standardized tasks,
- education,
- broad occupational employment,
- broad outlook.

Sources:

- O*NET,
- BLS,
- other government sources.

## Tier 2 — Profession-specific evidence

Examples:

- credentials,
- professional standards,
- technical responsibilities,
- role terminology.

Sources:

- professional organizations,
- profession-specific authoritative sources.

## Tier 3 — Employer/location/current recruiting evidence

Examples:

- actual entry titles,
- current internships,
- company-specific responsibilities,
- location-specific compensation,
- program timing.

Sources:

- official employer career pages,
- current postings,
- reliable current market data.

## Do-not-generalize rule

Fields that vary heavily by:

- employer,
- office,
- team,
- geography,
- time,

must not be presented as universal career truths.

That includes especially:

- exact hours,
- travel,
- compensation,
- software,
- hybrid policy,
- GPA preferences,
- promotion timing.

BLS median pay must **not** be presented as entry-level compensation.

---

# 23. Career Data Hierarchy

The production database should have four levels.

## Level 1 — Career

Example:

> FP&A

Stores:

- generic responsibilities,
- recurring activities,
- baseline skills/knowledge,
- broad requirements,
- broad conditions when supportable,
- broad trajectory,
- broad labor-market data.

## Level 2 — Company × Career

Example:

> Amazon × FP&A

Stores only employer-role differences supported by evidence:

- recurring tools,
- recurring responsibilities,
- training,
- business-partnering exposure,
- operating complexity,
- company-role recruiting,
- specialized experience,
- career signal,
- conditions if reliably different.

## Level 3 — Company × Career × Location/Office

Example:

> Amazon FP&A × Arlington

Stores:

- regional compensation,
- whether the role is available there,
- local recruiting,
- local industry exposure,
- office-specific facts only when verified.

## Level 4 — Specific Posting

Example:

> Financial Analyst — specific team — Arlington

Stores:

- exact requirements,
- exact responsibilities,
- explicit salary,
- work mode,
- travel,
- team context,
- graduation requirements,
- exact tools.

## Override rule

> **Most-specific reliable evidence wins.**

A posting that explicitly says SQL is required overrides a generic FP&A baseline that says SQL is merely common.

---

# 24. Data Status Values

Every material field should be able to carry a status such as:

- **Known**
- **Inherited**
- **Unknown**
- **N/A**

### Known

Directly supported at that level.

### Inherited

No more-specific evidence exists, so the value comes from the broader layer.

### Unknown

Insufficient evidence.

### N/A

The field genuinely does not apply.

Do not conflate:

> Unknown

with:

> the value is zero.

---

# 25. Confidence and Freshness

Each material fact should store:

- source,
- source URL,
- source type,
- source authority,
- date retrieved,
- source data version,
- last checked,
- refresh cadence,
- stale threshold,
- sample size if aggregated,
- confidence,
- whether direct or inherited.

Changing information should expire.

Examples:

- recruiting dates — frequent/seasonal refresh
- postings — daily/weekly in a live system
- official company program pages — perhaps 30–90 day checks around recruiting
- broad O*NET career information — update with O*NET releases
- BLS annual occupational data — update with release
- subjective company-role experience — refresh based on new evidence and sample size.

When sources conflict:

1. preserve both,
2. compare authority,
3. compare recency,
4. flag the affected record,
5. make a deliberate resolution,
6. do not silently overwrite.

---

# 26. Current Stage 1 Readiness Math

The latest September 1 workbook uses a meet-or-exceed approach.

For each **known** user capability:

\[
\text{Capability Match}_i = \min\left(\frac{\text{User Capability}_i}{\text{Role Requirement}_i},1\right)
\]

The contribution is weighted by the role requirement.

Conceptually:

\[
\text{Raw Readiness}
=
\frac{
\sum [\min(U_i/R_i,1)\times R_i]
}{
\sum [R_i \text{ where } U_i \text{ is known}]
}
\times 100
\]

## Why cap at 100

If a role needs capability 70 and the user has 100, the user meets the requirement.

The role is not necessarily a better fit merely because the person massively exceeds a minimum.

Overqualification may be a separate concept later, but it should not inflate basic readiness.

---

# 27. Evidence Coverage

The model calculates how much of the role's relevant requirement space is actually known.

\[
\text{Coverage}
=
\frac{
\sum [R_i \text{ where user evidence is known}]
}{
\sum [\text{all applicable } R_i]
}
\times 100
\]

Example:

- Known capabilities all look excellent.
- But only 30% of the role's weighted capability requirements are known.

The system should not show:

> Readiness 100, high confidence.

It should show:

> strong known evidence, low coverage.

---

# 28. Adjusted Readiness

Current prototype:

\[
\text{Adjusted Readiness}
=
50 + (\text{Raw Readiness}-50)\times \frac{\text{Coverage}}{100}
\]

Meaning:

- coverage = 100% → Adjusted Readiness = Raw Readiness,
- coverage = 0% → result moves to neutral 50.

This prevents incomplete evidence from producing falsely extreme readiness.

This is a **prototype confidence adjustment**, not a final scientifically validated formula.

---

# 29. Current Conditions-Fit Logic

The September 1 stress-test logic currently includes these rules.

## Normal hours

If:

> job normal hours ≤ user's maximum

then:

> 100.

If above:

> subtract roughly 10 points per hour above the maximum.

## Busy-period intensity

If job intensity ≤ user tolerance:

> 100.

Otherwise:

> subtract one point per point above tolerance.

## Schedule unpredictability

Same directional threshold idea.

If the user says:

> No preference

the ranking weight is 0.

## Travel

If job travel ≤ user maximum:

> 100.

Otherwise current prototype subtracts roughly:

> 3 points per percentage point above the maximum.

## Work mode

Current prototype uses a normalized remote → in-person scale and:

\[
100 - |\text{user target} - \text{job value}|
\]

## Variable pay

If job variable compensation is within tolerance:

> 100.

Otherwise current prototype reduces fit.

## Starting salary

If starting compensation ≥ user's minimum:

> 100.

If below, current prototype subtracts roughly:

> 5 points per $1,000 below the minimum.

### Important

These penalty slopes are **stress-test mechanics**, not validated behavioral science.

They should be tuned using real user decisions.

---

# 30. Current Work-Fit Math

The user has a preference value for each work activity.

The role has an activity-intensity value.

A basic compatibility term is:

\[
100 - |\text{User Preference} - \text{Role Activity Intensity}|
\]

But the user's **response weight** determines whether that question matters.

Neutral:

> weight 0.

Strong preferences:

> higher weight.

Role salience/discrimination can provide additional weighting so that role-defining differences matter more.

---

# 31. Current Trajectory-Fit Math

For future priorities the user assigns importance.

The career has a trajectory value.

Conceptually:

\[
\text{Trajectory Fit}
=
\frac{
\sum [\text{Role Trajectory Value}_i \times \text{User Importance}_i]
}{
\sum[\text{User Importance}_i]
}
\]

Not Important:

> weight 0.

This allows two users to evaluate the same path differently.

---

# 32. Current Overall Career Fit

The current September 1 prototype formula is:

\[
\text{Overall Career Fit}
=
0.25(\text{Adjusted Readiness})
+
0.15(\text{Conditions})
+
0.35(\text{Work Fit})
+
0.25(\text{Trajectory})
\]

Current weights:

| Component | Weight |
|---|---:|
| Adjusted Readiness | 25% |
| Conditions Fit | 15% |
| Work Fit / Enjoyment | 35% |
| Trajectory Fit | 25% |

### Why the separation matters

A user can receive:

- high Work Fit,
- low Readiness,
- strong Trajectory,
- weak Conditions.

That is more informative than a single unexplained "82% match."

### Weight status

These are **starting weights for the current model**, not final universal truth.

They must be stress-tested and validated against real user decisions.

---

# 33. Confidence Label

The current workbook uses:

- **High** — Coverage ≥ 70%
- **Medium** — Coverage ≥ 40%
- **Low** — Coverage < 40%

Production confidence should eventually combine:

- user evidence coverage,
- user evidence quality,
- job-data confidence,
- source freshness,
- sample size,
- source specificity.

A role may have:

> High profile confidence

but:

> Low employer-hours confidence.

Those should eventually be distinguishable.

---

# 34. Eligibility / Hard Gates

Eligibility is conceptually separate from Fit.

Possible gates:

- work authorization,
- graduation window,
- required degree,
- legally required license,
- must-have geographic constraint,
- hard salary constraint if the user explicitly marks it as non-negotiable,
- exact required credential.

A gate should say:

> Pass / Fail / Unknown

and explain why.

Do not award extra fit points merely for passing an eligibility gate.

A user can:

> love a career but fail a current posting's eligibility.

That is different from disliking the career.

---

# 35. Stage 1 Output

The career ranking should show enough detail to understand tradeoffs.

Possible output:

| Rank | Career | Overall | Readiness | Coverage | Work Fit | Conditions | Trajectory |
|---|---|---:|---:|---:|---:|---:|---:|

Then:

### Strongest reasons

- future-focused analytical work aligns strongly,
- demonstrated spreadsheet and finance capability,
- strong long-term optionality.

### Main tradeoffs

- schedule may be heavier than preferred,
- current evidence for modeling is incomplete,
- low confidence on travel assumptions.

### Missing information

- forecasting evidence unknown,
- client-interaction preference unknown.

### Suggested next question

Only ask if it could materially separate the top roles.

---

# 36. Career Page

A career page must answer:

> **What would I actually do, what would my life look like, and why might I like or dislike this career?**

It should not read like a dictionary.

## Required sections

### Overview

1–2 plain-English sentences describing:

- what the job exists to accomplish,
- who it serves,
- what the main output is.

### Day / Week

- 5–10 recurring activities,
- rough activity mix where supportable,
- meetings,
- analysis,
- writing,
- systems,
- client/internal work,
- busy periods.

### Skills & Systems

Separate:

- capabilities normally needed to enter,
- capabilities commonly developed later.

### Lifestyle

When reliable:

- normal-hour ranges,
- busy-period ranges,
- travel,
- schedule predictability,
- deadline pressure,
- client contact,
- remote/hybrid patterns.

Do not convert one employee anecdote into a universal fact.

### Compensation & Progression

- sourced entry-level range,
- promotion ladder,
- common next titles,
- observed/realistic exits.

Keep company-specific pay separate from general career pay.

### Fit / Misfit

Tie directly to profile dimensions.

Examples:

> May fit someone who enjoys future-focused analysis and business partnering.

> May frustrate someone who strongly dislikes recurring monthly cycles.

### Current Market

- hiring level,
- recruiting timing,
- geographic concentration,
- changing skill expectations,
- AI/technology impact,
- emerging sub-roles.

### Learn More

High-quality:

- official organizations,
- authoritative articles,
- strong videos/podcasts,
- certifications,
- training resources.

Affiliate relationships must never affect rankings.

---

# 37. Stage 2 — Company Comparison

Once a user selects a career, the question changes.

> **Where should I do this work?**

Camvince should avoid a single "Company Score" that hides fundamentally different concepts.

The target production dimensions are:

1. **Fit for You**
2. **Entry Difficulty / Difficulty for You**
3. **Career Signal**
4. **Specialized Experience**
5. **Conditions**
6. **Trajectory**

---

# 38. Fit for You at the Company Layer

This should measure whether the **actual work/conditions at that employer-role combination** align with the user.

It should not automatically increase because:

- the employer is famous,
- the employer is selective,
- the employer pays a lot,
- the role is hard to get.

A highly prestigious employer can still be a poor personal fit.

---

# 39. Entry Difficulty

Entry Difficulty answers:

> **How difficult is this opportunity for someone with my current profile?**

It should be separated into two concepts when possible:

### Market selectivity

How competitive is this employer-role opportunity generally?

Potential evidence:

- applicant volume where known,
- hiring volume,
- recruiting structure,
- candidate profile requirements,
- selectivity,
- school/recruiting concentration,
- role scarcity.

### Your readiness

How does the user's evidence compare with the opportunity requirements?

Then Camvince can label:

- Strong realistic target
- Realistic
- Competitive
- Stretch
- Major stretch

without pretending it knows an exact acceptance probability.

---

# 40. Career Signal

"Prestige" is too vague.

Preferred concept:

> **Career Signal**

Meaning:

> How strongly does experience in this employer × role combination tend to signal capability to future employers?

Potential evidence:

- employer recognition,
- function/practice reputation,
- selectivity,
- training/program quality,
- sophistication/complexity,
- responsibility,
- observed exits,
- recruiter recognition.

Career Signal should be:

> company × role

not just:

> company.

It should not increase core Fit.

---

# 41. Specialized Experience

This measures:

> **What experience is this employer-role combination likely to build?**

Possible dimensions:

- SQL/data work,
- modeling,
- forecasting,
- automation,
- ERP exposure,
- accounting overlap,
- business partnering,
- presentation,
- leadership exposure,
- operational ownership,
- client exposure,
- cross-functional work,
- process structure,
- strategy,
- industry depth.

Example:

Two FP&A employers may both be legitimate FP&A roles, but one may repeatedly emphasize:

- SQL,
- automation,
- operational ownership,

while another emphasizes:

- reporting,
- budgeting,
- Excel,
- accounting close.

Camvince should let the user compare those **experience footprints**.

---

# 42. Company Views

Different users may want different optimization views.

Possible views:

- **Best Overall**
- **Most Realistic**
- **Highest Upside**
- **Best Lifestyle**
- **Best Resume Builder**

These views are not the same as redefining Fit.

For example:

### Most Realistic

Can emphasize:

- Fit + accessibility.

### Highest Upside

Can emphasize:

- trajectory + career signal.

### Best Lifestyle

Can emphasize:

- conditions.

### Best Resume Builder

Can emphasize:

- career signal + specialized experience.

This keeps the underlying dimensions transparent.

---

# 43. Stage 3 — Location / Office

The location layer should contain two different types of information.

## Personal location preference

Examples:

- Very Interested
- Interested
- Neutral
- Prefer Not
- Strongly Avoid

## Market/industry opportunity

Examples:

- industry employment concentration,
- industry GDP,
- regional labor-market depth,
- relevant employer concentration,
- compensation context.

Do not use:

> "Dallas is prestigious"

as a city metric.

Use actual economic evidence.

---

# 44. BEA and City × Industry Strength

BEA can provide regional economic data such as:

- employment,
- income,
- GDP,
- industry data,
- state/county statistics,
- some MSA price-parity data.

Camvince can derive a concentration-style metric.

Example:

\[
\text{Industry Concentration}
=
\frac{
\text{Local Industry Share}
}{
\text{National Industry Share}
}
\]

If an industry is 10% of local activity but 5% nationally:

\[
10\%/5\%=2.0
\]

That suggests the industry is roughly twice as concentrated locally as nationally.

Camvince can translate the metric into understandable bands, but must preserve the raw source and methodology.

---

# 45. Specific Posting Layer

The most-specific opportunity should be able to override broader assumptions.

Potential posting fields:

- title,
- employer,
- location,
- team/business unit,
- description,
- responsibilities,
- degree requirement,
- graduation window,
- GPA if stated,
- exact tools,
- years/experience,
- skills,
- salary range,
- travel,
- work mode,
- sponsorship/work authorization,
- recruiting deadline,
- source URL,
- date collected.

Example:

Career baseline:

> ERP familiarity helpful.

Company-role baseline:

> SAP appears frequently.

Specific posting:

> Oracle required.

The posting-specific Oracle requirement is the most specific fact.

---

# 46. "What Should I Do Next?" Layer

Career ranking should not be the end.

If the user selects FP&A and has:

- strong Excel,
- finance/accounting knowledge,
- weak forecasting evidence,
- unknown SQL,
- limited business-partnering evidence,

Camvince can produce:

### Current strengths

- spreadsheet analysis,
- finance/accounting foundation.

### Largest readiness gaps

- forecasting/modeling evidence,
- SQL/data querying,
- business-partnering evidence.

### Next experiences

- FP&A internship,
- forecasting project,
- financial-modeling project,
- BI/SQL project,
- role with budgeting/variance analysis.

### Relevant credentials/training

Only when a credential actually addresses a verified gap.

### Counterfactual

Later:

> If forecasting capability increases from X to Y, which careers/opportunities become more realistic?

This is where the older "Career Potential" concept can still be useful.

**Current resolution:** Potential is not a core Stage 1 ranking component in the September 1 model. It may be reintroduced as a separate **gap-closure/actionability output**, not mixed into fit without an explicit future decision.

---

# 47. Career Board / Persistent Decision System

Camvince should remember what the user is considering.

Suggested stages:

> Exploring → Interested → Targeting → Applying → Applied → Offer → Rejected / No Longer Interested

Save:

- careers,
- companies,
- career × company × location combinations,
- specific opportunities,
- notes,
- likes/dislikes,
- readiness gaps,
- recruiting status,
- comparison decisions.

The Career Board creates continuity between sessions.

---

# 48. Reasons to Return

A one-time career assessment has weak retention.

Camvince should become useful when either the **person** changes or the **market** changes.

## Person changes

- new internship,
- new job,
- new class,
- new skill,
- certification,
- changed hours preference,
- changed pay goal,
- changed city,
- new long-term goal,
- changed likes/dislikes.

## Market changes

- new recruiting program,
- new role,
- changed salary,
- employer stops/starts hiring,
- changed recruiting deadline,
- new industry trend,
- AI changes job content,
- changed employer program.

Notifications should always answer:

> **Why does this matter to something you care about?**

Do not send generic company news simply to increase engagement.

---

# 49. Data Source Stack

Camvince should use source-backed data rather than rely on generic AI memory.

## 49.1 O*NET — career baseline

Use for:

- tasks,
- skills,
- knowledge,
- abilities where relevant,
- work activities,
- work context,
- education/job zones,
- technology skills,
- tools,
- interests/work styles as source evidence.

O*NET should feed the **raw career evidence layer**.

Camvince then maps it to the universal Camvince schema.

Important:

> O*NET is a source. The Camvince normalization/decision model is the product layer.

Current O*NET 31.0 downloadable database is broadly available under CC BY 4.0, with attribution and modification disclosure requirements. O*NET Web Services are free for commercial/noncommercial use subject to account, attribution, licensing, and terms. For a commercial product, the downloadable database may be operationally simpler because modified/derived Camvince structures can be maintained locally under the database license, while Web Services have additional terms.

## 49.2 CareerOneStop — current job/market layer

Use for:

- job title,
- company,
- location,
- job description,
- posting/acquisition date,
- original URL,
- O*NET codes,
- occupation information,
- wages,
- projected employment,
- certifications,
- licenses,
- training,
- labor-market information.

CareerOneStop explicitly offers Web APIs so third parties can integrate its quality-controlled datasets into their own websites; its API data are described as open data under USDOL's Open Data Policy.

## 49.3 BLS

Use for:

- occupational wages,
- employment,
- occupation/industry trends,
- outlook,
- validation of other labor-market estimates.

BLS data are public, but derived analyses should clearly state that BLS cannot vouch for analyses after retrieval.

## 49.4 BEA

Use for:

- regional employment,
- regional income,
- GDP,
- industry economic activity,
- regional price-parity context.

Use these facts to derive transparent economic concentration rather than manually scoring cities.

## 49.5 Official employer pages

Use for:

- recruiting programs,
- internships,
- actual titles,
- locations,
- eligibility,
- current deadlines,
- company claims,
- official salary where posted,
- team/program descriptions.

## 49.6 Current job postings

Use for:

- exact requirements,
- actual responsibilities,
- exact tools,
- salary,
- travel,
- location,
- work mode.

Repeated postings can help build company × role patterns.

One posting should **not** define an entire employer-role experience.

## 49.7 Camvince user data

Long-term proprietary source:

- task-level likes/dislikes,
- role/company experience,
- skills developed,
- hours ranges,
- training,
- responsibilities,
- career transitions,
- internship outcomes,
- satisfaction,
- decisions.

Use aggregation thresholds and privacy controls.

## 49.8 Licensed transition data later

Potential vendors:

- workforce-transition datasets,
- labor-market providers.

Use them if the license allows the intended commercial use.

Do not build the business on unauthorized scraping.

---

# 50. How Company × Role Profiles Should Be Derived

Suppose Camvince collects 50 recent FP&A postings from Employer A.

The system can parse recurring signals:

- Excel mentioned in 90%,
- SQL in 60%,
- forecasting in 80%,
- business partnering in 70%,
- automation in 40%.

Those percentages are illustrative only.

Camvince can derive:

> Employer A FP&A appears to place relatively high emphasis on forecasting, data querying, and business partnering.

The record should also store:

- posting count,
- date range,
- source URLs,
- location mix,
- title mix,
- confidence.

This is much stronger than manually assigning:

> SQL = 85.

---

# 51. Employee Experience Data

Fields like:

- hours,
- culture,
- stress,
- work-life balance,
- management quality,

are much noisier than:

- degree requirement,
- posting location,
- tool listed.

Camvince should treat subjective information as:

- distributions,
- ranges,
- themes,
- confidence bands,

not universal facts.

Long term, Camvince's own structured post-internship/post-job survey may be more useful than a generic employer star rating because Camvince can ask:

> What career were you in?  
> Which team/function?  
> Which location?  
> Which activities did you perform?  
> What did you actually enjoy?  
> How many hours did you typically work?  
> What skills did you develop?

That produces **role-specific employer intelligence**.

---

# 52. Legal / Data-Access Principle

Technology does not change data rights.

Using:

- an API,
- an MCP server,
- an AI agent,
- a browser automation tool,

does not automatically make data use legal.

The rule is:

> **The underlying access and license must permit the use.**

Safe architecture:

- O*NET under applicable license,
- CareerOneStop API,
- BLS,
- BEA,
- official employer sources according to applicable terms,
- licensed commercial data,
- user-consented Camvince data.

Avoid making unauthorized large-scale LinkedIn scraping or scraped employee-review data a core dependency.

MCP can be a technical integration layer, but it is **not a license**.

---

# 53. Explainability

Every recommendation should be able to answer:

> Why?

Not:

> "AI says 87."

Possible explanation:

> **Why FP&A ranked highly**
>
> - You strongly prefer future-focused quantitative work.
> - Your current spreadsheet/finance evidence meets much of the role's known baseline.
> - Your desired long-term optionality aligns well with the role.
> - Typical travel appears below your stated maximum.
>
> **What holds it back**
>
> - Forecasting/modeling evidence is incomplete.
> - Some company-specific hours data are inherited rather than directly verified.

A user should be able to trace:

> evidence → normalized attribute → role comparison → component score → recommendation.

---

# 54. No Fake Precision

Internally, formulas may produce:

> 87.3642

The UI generally should not imply that this is a scientifically exact quantity.

Better:

> 87 / Strong Fit

with:

> Confidence: Medium

and a plain-English explanation.

Tie bands are acceptable.

If top careers are nearly tied, the system should say:

> These are functionally close based on what we currently know.

Then ask the highest-information question.

---

# 55. CareerExplorer — What It Actually Does

CareerExplorer is a **serious competitor**, not a basic quiz.

Current public CareerExplorer materials say its assessment uses:

- psychometrics,
- machine learning,
- career satisfaction data,
- interests,
- goals,
- history,
- workplace preferences,
- personality,
- education/work history,
- location,
- salary expectations.

Its current career-test page advertises:

- **1,500+ careers and degrees**
- **140+/150+ personality traits**, depending on the page wording
- hundreds of millions of questions answered.

CareerExplorer describes four major fit dimensions:

1. **Workplace**
2. **History**
3. **Interests**
4. **Personality**

CareerExplorer's FAQ also says it considers:

- salary requirements,
- salary-growth potential,
- job demand,
- job availability in the user's area,
- required training,
- whether the training timeline fits the user's needs.

Its matching system updates recommendations when the user supplies new relevant information.

Therefore these claims are **not valid Camvince differentiators by themselves**:

- "We use work history."
- "We use education."
- "We use salary."
- "We use location."
- "We use O*NET."
- "We update recommendations."
- "We explain why a career fits."
- "We consider whether training is needed."

CareerExplorer already publicly describes those capabilities.

---

# 56. CareerExplorer Inputs

CareerExplorer currently asks or derives information across:

- interests,
- personality/work style,
- workplace preferences,
- past career/work history,
- education,
- goals,
- salary expectations,
- urgency/timeline,
- location-related considerations.

Its traditional assessment is described as roughly 30 minutes across modules such as:

- Welcome,
- History & Goals,
- Workplace,
- Interests,
- Personality,

with optional refinements.

---

# 57. CareerExplorer Outputs

CareerExplorer provides:

- ranked careers,
- career/degree matches,
- personality/archetype insights,
- compatibility explanations,
- career pages,
- salary data,
- demand/job-market information,
- education/training information,
- satisfaction information,
- personality/work-environment information,
- AI-impact information on career pages,
- saved/rated career reactions,
- organizational dashboards for universities/counselors.

CareerExplorer's public site also says users can explore the world of work and make a plan to get to a desired career.

Therefore Camvince should **not** position CareerExplorer as:

> "just a personality test."

That would be inaccurate and easy for a judge to challenge.

---

# 58. CareerExplorer Validation / Scientific Strength

CareerExplorer publicly describes substantial psychometric work.

Its science documentation states:

- its assessment is based on the O*NET Content Model,
- scales were developed by an I/O psychologist,
- all scales have Cronbach's alpha above .8,
- average reported reliability is .88,
- it validates predictions against users' "thumbs up / thumbs down" reactions to careers.

This is a real competitive strength.

Camvince should not claim scientific superiority before Camvince has performed its own validation.

---

# 59. CareerExplorer Organizational Business

CareerExplorer sells an organizational product for:

- universities,
- high schools,
- counselors,
- nonprofits,
- consultants,
- other organizations.

Its organization product publicly describes:

- student assessments,
- personalized reports,
- career library,
- admin dashboard,
- student progress,
- aggregate participation,
- co-branded experiences.

This means:

> "We sell to universities"

is also **not a unique Camvince differentiator**.

Camvince needs a different institutional value proposition.

---

# 60. CareerExplorer Revenue / Scale

CareerExplorer's current standalone revenue is **not publicly disclosed**.

Penn Foster acquired Sokanu/CareerExplorer in March 2021.

The acquisition announcement said CareerExplorer was used by **more than 10 million people annually**.

The transaction terms were not disclosed.

Therefore Camvince should not cite a made-up CareerExplorer revenue number in a pitch.

The defensible takeaway is:

> This category has demonstrated very large user demand and strategic acquisition value.

---

# 61. Where CareerExplorer and Camvince Overlap

| Capability | CareerExplorer | Camvince |
|---|---:|---:|
| Interests | Yes | Yes |
| Work preferences | Yes | Yes |
| Personality/work style | Yes | Optional/supporting |
| Education | Yes | Yes |
| Work history | Yes | Yes |
| Salary preference | Yes | Yes |
| Location consideration | Yes | Yes |
| Career ranking | Yes | Yes |
| Career descriptions | Yes | Yes |
| Explain why career fits | Yes | Yes |
| Labor-market data | Yes | Yes |
| Training/readiness consideration | Yes | Yes, but more explicitly separated |
| Recommendations update with new info | Yes | Yes |
| University product | Yes | Possible |
| Saved career reactions | Yes | Yes |

The overlap is substantial.

That is why **career matching cannot be the entire Camvince product**.

---

# 62. Where Camvince Must Be Different

The intended differentiation is not one feature.

It is a deeper workflow.

## 62.1 Domain depth

CareerExplorer is broad.

Camvince starts narrow and attempts to distinguish closely related business paths such as:

- External Audit
- Internal Audit
- FDD
- Valuation
- FP&A
- Treasury
- Corporate Banking
- Commercial Banking
- Investment Banking

rather than stopping at a broad occupational label.

## 62.2 Explicit Readiness separated from Work Fit

Camvince should show:

> You may love this work.

separately from:

> You are currently competitive for this work.

Example:

**Investment Banking**

- Work Fit: High
- Readiness: Low/Medium
- Entry Difficulty: Extremely Competitive

**FP&A**

- Work Fit: High
- Readiness: High
- Entry Difficulty: Competitive

This is a decision tradeoff.

## 62.3 Evidence Coverage

Camvince explicitly tracks:

> how much of the recommendation is actually supported.

Unknown information should reduce confidence rather than silently become an average.

## 62.4 Company × Career layer

Career selection is not the end.

Camvince asks:

> Which employer is best for this role for this person?

## 62.5 Role-specific employer signal

Camvince separates:

> Career Signal

from:

> personal Fit.

## 62.6 Entry Difficulty

Camvince separately evaluates:

> general competitiveness + the user's current readiness.

## 62.7 Specialized Experience

Camvince attempts to estimate:

> what this employer-role combination will teach/build.

## 62.8 Location/office specificity

Camvince moves:

> career → employer → office → posting.

## 62.9 Actual posting overrides

Current opportunity facts can replace broad assumptions.

## 62.10 Longitudinal task-level learning

Camvince's profile is intended to learn from:

> the actual tasks a user performed and liked/disliked during internships/jobs.

This is stronger than merely allowing someone to update an assessment answer.

## 62.11 Persistent decision history

Career Board remembers:

- what was considered,
- what was rejected,
- what was targeted,
- what changed.

## 62.12 Next-move engine

Camvince should tell the user:

> What evidence/skill/experience would most improve the next decision?

rather than ending at:

> "This career may fit you."

---

# 63. Competitive Conclusion — Is Camvince Actually Different?

## If Camvince is built as:

> Resume + preferences + personality → career ranking → career descriptions

then:

> **No. The differentiation is not strong enough.**

That product sits directly in CareerExplorer's territory.

## If Camvince is built as:

> living evidence-backed profile → career fit/readiness/conditions/trajectory → company × role decision → employer accessibility → career signal → specialized experience → location/office → posting-specific comparison → skill gaps → observed career paths → post-internship profile update → next move

then:

> **Yes. That is a materially different product architecture and user workflow from the CareerExplorer experience described in CareerExplorer's current public materials.**

The safest competitive language is:

> **CareerExplorer is a powerful career-discovery and assessment platform. Camvince is being designed as a career decision-navigation system that continues from career choice into employer, location, opportunity, and next-move decisions using a persistent evidence-backed profile.**

Do not say:

> "CareerExplorer doesn't update."

It does.

Do not say:

> "CareerExplorer doesn't use work history."

It does.

Do not say:

> "CareerExplorer doesn't consider salary/location/training."

It does.

Do not say:

> "CareerExplorer is only a personality test."

It is not.

---

# 64. The One-Sentence Differentiation

A useful line:

> **CareerExplorer helps users discover careers; Camvince is designed to help users navigate the sequence of decisions that follows—career, employer, location, opportunity, development, and next move—as their real experience changes.**

Another:

> **Camvince turns career discovery into an ongoing decision system.**

---

# 65. Why General ChatGPT Is Still a Major Competitor

General AI can already:

- explain roles,
- compare careers,
- analyze a resume,
- brainstorm companies,
- discuss salaries,
- personalize advice,
- summarize web research.

Therefore:

> **If Camvince is only a chat interface, the company is weak.**

Camvince needs durable structure that a one-off conversation does not automatically maintain:

- canonical user profile,
- versioned profile history,
- source-backed career database,
- company × career database,
- source freshness,
- standardized scoring,
- persistent Career Board,
- tracked decisions,
- company/location/posting comparison,
- confidence/coverage,
- longitudinal outcomes,
- reproducible recommendations.

General AI can power pieces of Camvince, but the **structured data, workflow, history, and proprietary longitudinal dataset** are what can turn it into a company rather than a prompt.

---

# 66. Other Competitors / Substitutes

## LinkedIn

Strengths:

- network,
- jobs,
- companies,
- professional identity.

Camvince differentiation:

> decision support before and between applications.

## Handshake

Strengths:

- campus job access,
- university recruiting.

Camvince differentiation:

> deeper career understanding and company/path decisions.

## Glassdoor / employee-review platforms

Strengths:

- employee reviews,
- salary/culture information.

Camvince differentiation:

> role-specific structured decision model rather than generic employer ratings.

## Reddit / YouTube / Google

Strengths:

- real-world anecdotes,
- breadth,
- free information.

Weakness:

- fragmented,
- inconsistent,
- not personalized in a persistent structured way.

Camvince should use such sources carefully for qualitative discovery, not automatically treat anecdotes as facts.

---

# 67. Business Model — Current Hypotheses

No pricing model is validated yet.

## Free core

The free product should be genuinely useful:

- basic profile,
- career understanding,
- initial recommendations,
- enough save/compare functionality to build trust.

Do not intentionally make free useless.

## Potential premium features

Ideas to validate:

- advanced fit analysis,
- deeper company comparisons,
- recruiting/market alerts,
- skill-gap roadmaps,
- advanced Career Board,
- personalized next-step planning,
- offer comparison,
- more detailed opportunity intelligence.

## One-time product

Potential:

> **Career Blueprint**

Could include:

- top careers,
- company/location targets,
- readiness gaps,
- skill-development plan,
- recruiting timeline,
- next steps.

## University / career-center licensing

Potential B2B2C model:

- full student access,
- counselor dashboard,
- cohort analytics,
- decision-progress visibility,
- career-center efficiency,
- custom branding,
- outcome analytics.

Because CareerExplorer already sells to universities, Camvince must sell a **deeper decision-management value proposition**, not merely "we also have an assessment."

## Later revenue

Possible:

- API,
- white label,
- employer/recruiter tools,
- affiliate education/training,
- employer branding.

### Ranking independence rule

Ads, sponsors, affiliates, employers, or paid placement must **never change recommendation rankings**.

If paid employer promotion ever exists, it must be clearly separated and labeled.

---

# 68. What Becomes Defensible

The defensibility is not O*NET.

Anyone can obtain O*NET data under its license.

The potential moat is the **derived and longitudinal layer**.

## 68.1 Normalized career schema

A universal way to map:

- career tasks,
- skills,
- conditions,
- work activities,
- trajectory,
- systems,

into one comparable data contract.

## 68.2 Company × role profiles

Repeated current-posting evidence turned into:

- company-role requirements,
- specialized experience,
- role-specific career signal,
- conditions.

## 68.3 Longitudinal user profiles

Data showing:

> what users thought before experience → what they actually did → what they liked/disliked → what they pursued next.

## 68.4 Observed outcomes

Over time:

- which recommendations users save,
- which they reject,
- which internships they accept,
- which career moves they make,
- which skills they build,
- satisfaction after experience.

## 68.5 Decision history

A persistent graph of:

> person state → available options → recommendation → choice → outcome.

That is significantly harder to recreate than a static assessment.

---

# 69. The Long-Term Data Flywheel

1. More users create profiles.
2. Users receive structured recommendations.
3. Users save/reject/compare paths.
4. Users pursue internships/jobs.
5. They return with actual experience.
6. Camvince learns task-level likes/dislikes and capabilities.
7. Profiles become more evidence-based.
8. Career/company intelligence gains outcome evidence.
9. Recommendations become better.
10. Better recommendations create more value and retention.

The most valuable proprietary data eventually may be:

> **longitudinal decision and outcome data**, not quiz responses.

---

# 70. Trust Model

Students should trust Camvince because the system can show:

- where a fact came from,
- how current it is,
- how confident Camvince is,
- whether it is direct or inherited,
- which user answer affected the result,
- which evidence is missing,
- why a ranking changed,
- what is fact vs estimate,
- which fields are subjective.

Trust should come from **transparency**, not a claim that "AI knows your perfect career."

---

# 71. Validation Before Scale

The current business plan correctly treats key assumptions as unvalidated.

## We need to prove:

1. Students experience real career-decision pain.
2. Camvince is meaningfully better than a one-off AI conversation.
3. Users will complete enough profile information.
4. Recommendations introduce useful options.
5. Users save/compare decisions.
6. Users return.
7. Users trust the explanations.
8. Company-level comparison adds value after career discovery.
9. Users care about readiness/entry difficulty/trajectory enough to use them.
10. Someone is willing to pay—student, university, or another customer.

---

# 72. Current Validation Experiments

Existing project plan includes:

### GTM-001 — Camvince vs general AI

Give target students the same career decision through:

- Camvince,
- a normal general AI tool.

Then ask:

- Which was more useful?
- Which was more trustworthy?
- Which was easier to continue later?
- Which would you return to?
- Why?

Current placeholder success target:

> 60% prefer Camvince.

This is a hypothesis, not proof.

### GTM-002 — Profile completion

Measure:

> start → resume/profile → minimum profile complete → recommendations.

Current placeholder target:

> 70% complete.

### GTM-003 — Useful discovery

Ask whether the user found at least one career they had not seriously considered but now would explore.

Current placeholder target:

> 30%.

### GTM-004 — Save/compare behavior

Measure users who save or compare at least one:

- career,
- employer,
- career/company/location path.

Current placeholder target:

> 50%.

Again, these are experiment thresholds, not market facts.

---

# 73. First User Acquisition

Early acquisition should be manual.

Possible first channels:

- student organizations,
- professors,
- accounting clubs,
- finance clubs,
- classmates,
- alumni,
- career-center contacts,
- campus pilots,
- student ambassadors.

Do not spend heavily on paid acquisition before there is evidence of:

- product completion,
- save/compare behavior,
- return behavior.

---

# 74. Current Prototype vs Production Target

## Current prototype proves

- resume evidence can become standardized capabilities,
- Unknown can be excluded instead of scored as zero,
- Coverage can separate confidence from score,
- career attributes can be compared with user values,
- changing a meaningful preference can change rankings,
- Stage 1 can be separated from Stage 2,
- career ranking can feed company/location exploration.

## Current prototype does **not** yet prove

- final weights are correct,
- company numeric data are validated,
- entry-difficulty formula is validated,
- career-signal formula is validated,
- hours are accurate for every employer,
- trajectory transitions are empirically validated,
- students will pay,
- universities will buy,
- retention exists,
- CareerExplorer users will switch,
- general AI users will switch.

The spreadsheet is a **model stress test**, not final scientific validation.

---

# 75. Prototype Company Data Warning

Any prototype company values such as:

- Signal = 93,
- Difficulty = 80,
- Specialized Experience = 75,
- Salary = X,

must not be presented as researched fact unless the underlying company-role record has actual supporting evidence.

Current stress-test company values were created to test model behavior.

Production data must replace them with:

- sourced facts,
- derived metrics with formulas,
- source counts,
- freshness,
- confidence.

---

# 76. Prototype City Data Warning

Manual city-industry assumptions such as:

> Dallas Energy = 90

are not production facts.

Production should derive market strength from:

- BEA,
- BLS,
- CareerOneStop,
- other licensed/public market data.

---

# 77. Open Design Questions — Not Contradictions

The following are **not contradictions**. They are unresolved decisions that need validation.

1. Final Stage 1 weights
2. Final Conditions penalty slopes
3. Final confidence thresholds
4. Whether to display numeric Overall or primarily bands
5. Exact number of careers in the first public MVP
6. Exact number of employers/markets in the first public MVP
7. Final company Fit formula
8. Entry Difficulty formula/data requirements
9. Career Signal methodology
10. Specialized Experience methodology
11. Minimum posting sample for company-role inference
12. Minimum employee-feedback sample for display
13. Transition-data provider
14. Exact university-pricing model
15. Exact student premium price
16. Consumer vs university primary revenue channel
17. Whether Potential is reintroduced as a formal score
18. Exact profile-confidence model
19. Exact refresh cadence by source type
20. How much employer/office detail can be reliably sourced
21. Which profile questions can be deferred until role selection
22. Whether personality assessment remains a meaningful supporting input or is minimized in favor of work-activity evidence

These require testing, not arbitrary resolution.

---

# 78. Contradiction Audit — Historical Conflicts and Current Resolution

## Conflict 1 — Overall scoring formula

### Older rule

> Overall Fit = 45% Readiness + 35% Career Match + 20% Preference Fit.

### Current rule

Stage 1 prototype:

> 25% Adjusted Readiness + 15% Conditions + 35% Work Fit + 25% Trajectory.

### Resolution

**Current September 1 model wins.**

The older formula remains decision history only.

---

## Conflict 2 — Ideal Fit

### Older rule

> Ideal Fit = 75% Career Match + 25% Preference Fit.

### Current rule

The September 1 reworked model does not use Ideal Fit as a primary current output.

### Resolution

**Ideal Fit is deprecated from the current primary architecture.**

It may be reintroduced only if there is a future deliberate product reason.

---

## Conflict 3 — Career Potential

### Older rule

Potential is one of the core named scores.

### Current model

Stage 1 currently ranks with:

- Readiness
- Conditions
- Work Fit
- Trajectory.

### Resolution

Potential is **not a core current ranking component**.

The concept remains useful later as:

> gap closure / how realistic it is to become competitive.

---

## Conflict 4 — Lifestyle inside Career Match

### Older version

Hours/travel/work setting were sometimes included inside Career Match.

### Current version

Work enjoyment and job conditions are separate.

### Resolution

- Work content → **Work Fit**
- hours/pay/travel/work mode → **Conditions Fit**

This is canonical.

---

## Conflict 5 — Company Fit includes prestige

### Current workbook demo

The Stage 2 demo still uses brand/training inputs in a simplified Company Fit.

### Production design

Separate:

- Fit
- Entry Difficulty
- Career Signal
- Specialized Experience
- Conditions
- Trajectory.

### Resolution

The demo formula is **temporary prototype logic**.

Do not treat brand/prestige as core fit.

---

## Conflict 6 — Resume only scores Excel and SAP

### Workbook demo

Excel and SAP are the populated example.

### Current production requirement

All supported extracted capabilities can be scored.

### Resolution

Excel/SAP are **examples only**.

The production parser is dynamic across the full resume capability schema.

---

## Conflict 7 — User directly edits derived profile

### Old wording

Some files say users "edit profile fields."

### More precise current architecture

Users confirm/correct:

- resume facts,
- normal-language answers.

Backend:

- canonical attributes,
- IDs,
- scores,

are re-derived.

### Resolution

The user can edit what they actually told Camvince.

They do **not** edit scoring IDs or derived score values.

---

## Conflict 8 — Feedback silently updates Career DNA

### Old ambiguity

Some flow language suggested actions could directly change profile fields.

### Current rule

Behavior is evidence.

Meaningful changes should be confirmed when they conflict with explicit user answers.

### Resolution

Do not silently overwrite explicit preferences from a click.

Use behavioral evidence to:

- increase confidence,
- suggest a change,
- trigger a targeted question.

---

## Conflict 9 — Readable Match ID

### Old concept

Profile traits encoded into readable Match ID.

### Current concept

- permanent user ID,
- profile version,
- optional normalized fingerprint.

### Resolution

Readable trait-concatenation Match ID is deprecated.

---

## Conflict 10 — 12 careers vs 24 careers

### Older launch plan

A narrow MVP could launch with ~12 researched careers.

### Verified role universe

24 careers are supported in the frozen target universe.

### Resolution

These statements are compatible if phrased correctly:

- **24 = verified target universe**
- **MVP coverage may be narrower if data quality requires it**
- only sufficiently sourced records should be marked active.

---

## Conflict 11 — Company/office specificity

### Risk

Older prototypes create a full numeric record for every company/city.

### Current evidence rule

Do not fabricate office-level differences.

### Resolution

Use inheritance:

> career → company-role → office → posting.

Only create a more-specific override when evidence exists.

---

## Conflict 12 — City preference vs city industry strength

### Risk

One city score could mix the user's preference with market opportunity.

### Current rule

Separate:

- personal Location Fit,
- objective market/industry context.

### Resolution

Canonical.

---

## Conflict 13 — "Prestige"

### Old label

Prestige.

### Current label

Career Signal.

### Resolution

Career Signal is preferred because it is:

- role-specific,
- evidence-based,
- future-employer-facing,
- separate from Fit.

---

## Conflict 14 — Exact employer acceptance probability

### Possible temptation

Turn Entry Difficulty into offer odds.

### Current rule

Do not claim exact probability without representative applicant/outcome data.

### Resolution

Use competitive bands and person-relative readiness.

---

## Conflict 15 — Career transition guarantees

### Possible old language

"Exit opportunities."

### Current rule

Use:

> observed/estimated transition strength.

### Resolution

No guaranteed exits.

---

## Conflict 16 — CareerExplorer is only a personality quiz

### Incorrect simplification

CareerExplorer = personality quiz.

### Verified reality

CareerExplorer combines psychometrics, interests, workplace preferences, work/education history, salary/location/training considerations, career data, and career reports.

### Resolution

Never position against a straw-man competitor.

---

## Conflict 17 — Adaptive profile is unique by itself

### Incorrect claim

CareerExplorer is static; Camvince updates.

### Verified reality

CareerExplorer says recommendations update when users provide new relevant information.

### Resolution

Camvince's differentiation must be more specific:

> **actual task-level work experience + readiness changes + company/opportunity decision history + longitudinal navigation**.

---

# 79. Current Canonical Decisions Snapshot

The following should be treated as current unless explicitly changed later.

### Product

- Career decision/navigation platform, not just career test.
- Business students first.
- Career ranking is Stage 1, not the entire product.

### Profile

- Four separate dimensions: Readiness, Work Fit, Conditions, Trajectory.
- Resume evidence does not imply preference.
- Actual experience can update profile over time.
- Unknown does not equal zero.
- User edits normal-language evidence/answers, not backend IDs/scores.

### Resume

- Dynamic extraction across all supported categories.
- Exact system + transferable family.
- Targeted follow-up only when ambiguity matters.
- Confirmed value directly feeds backend scoring.

### Career model

- 24 verified primary careers.
- Ambiguous titles map by actual work.
- Role fingerprints use activity intensity + salience.

### Scoring

- Latest Stage 1 prototype weights: 25 / 15 / 35 / 25.
- Coverage/confidence stays visible.
- Neutral preferences have zero ranking weight.
- Meet/exceed readiness caps at requirement.
- No fake precision.

### Employer model

- Company comparison happens after career selection.
- Fit, Difficulty, Signal, Specialized Experience, Conditions, Trajectory remain separate.
- Signal/Difficulty do not inflate core Fit.

### Data

- O*NET as career baseline.
- CareerOneStop for jobs/current career/market/training data.
- BLS for labor-market validation.
- BEA for regional/industry economics.
- Employer pages/postings for current specific facts.
- Licensed or proprietary transition data later.
- User feedback becomes proprietary role-specific data.
- Most-specific reliable fact overrides broader inherited fact.
- Every changing fact needs source/freshness/confidence.

### Retention

- Career Board persists decisions.
- Profile changes and market changes create reasons to return.
- Notifications must be decision-relevant.

### Competition

- CareerExplorer is a major direct competitor at Stage 1.
- General-purpose AI is the biggest substitute threat.
- Camvince must win through structured longitudinal navigation beyond career matching.

---

# 80. How to Answer the Nine Hard Questions

## "Why isn't this CareerExplorer?"

> CareerExplorer is already a strong career assessment and discovery platform. Camvince overlaps at the initial career-matching stage, but the intended product continues into current readiness, company × role comparison, entry difficulty, career signal, specialized experience, city/office context, exact posting comparison, skill gaps, observed career transitions, and a living profile that learns from real internship/job activity. If Camvince stopped at top career matches, the differentiation would not be enough.

## "Why can't ChatGPT do this?"

> ChatGPT can explain careers and personalize one conversation. Camvince's value is the persistent structured system: canonical profile, version history, source-backed career/company database, standardized scoring, Career Board, data freshness, company/location/posting hierarchy, longitudinal outcomes, and reproducible decisions. AI can power Camvince, but it is not the whole product.

## "Where does the career data come from?"

> O*NET and BLS for career/labor foundations; CareerOneStop for current job, training, wage, and labor-market data; BEA for regional economic context; employer pages and actual postings for employer/location-specific facts; later licensed workforce-transition data and Camvince's own user outcome data.

## "How do you know the rankings are correct?"

> We do not claim they are scientifically perfect today. The model is transparent, configurable, coverage-aware, and designed to be validated. We will compare recommendations with user decisions, satisfaction, saved/rejected options, post-internship feedback, and longitudinal outcomes. We show confidence and missing evidence rather than hiding uncertainty.

## "Why would students trust you?"

> Every material recommendation can show the user's contributing evidence, the job attributes it was compared with, the source and freshness of market facts, and the missing data. Unknowns remain unknown. Employer sponsorship does not affect rankings.

## "Who pays?"

> Free student core first. Potential premium student features and one-time Career Blueprint should be tested. Long term, universities/career centers are a strong potential buyer because the platform can help a small advising staff serve more students with structured, persistent decision support. Pricing is not validated.

## "How do you acquire customers?"

> Start manually through reachable business students, clubs, professors, alumni, and campus partners. Prove completion, usefulness, saving, and return behavior before scaling SEO/social/referrals/paid channels.

## "What becomes defensible as you scale?"

> Normalized career/company-role data, longitudinal user profiles, task-level work feedback, career transition/outcome data, decision histories, company-role experience footprints, and validated matching relationships—not O*NET itself.

## "Why does this become a company rather than a feature?"

> Because the product is a persistent decision system that lives across years of career choices, continuously updates structured person and market data, supports employer/location/opportunity decisions, and accumulates proprietary longitudinal outcomes. If it were only one career quiz or one chat answer, it would be a feature.

---

# 81. Pitch Positioning

Avoid:

> "We use AI to find your perfect career."

Avoid:

> "A better CareerExplorer."

Avoid:

> "LinkedIn but for career matching."

Prefer:

> **Camvince is a Career Decision Intelligence platform for students and early-career professionals. It builds a living profile from what you've done, what you actually enjoy, the conditions you want, and where you want your career to go. It first helps you choose a career, then helps you compare where to do it, how realistic each opportunity is, what experience it will build, and what move to make next. The profile updates as your real experience changes.**

Short form:

> **What should I do? Where should I do it? What should I do next?**

---

# 82. The Product in One Full Flow

```text
USER JOINS
    ↓
Resume upload / manual experience
    ↓
Extract facts + capabilities
    ↓
Ask only important missing confirmations
    ↓
Conditions preferences
    ↓
Work-activity enjoyment
    ↓
Trajectory priorities
    ↓
VERSIONED LIVING PROFILE
    ↓
Compare to source-backed career fingerprints
    ↓
READINESS
WORK FIT
CONDITIONS
TRAJECTORY
COVERAGE / CONFIDENCE
    ↓
STAGE 1 — CAREER RANKING
    ↓
Career page
    ↓
Save / reject / compare
    ↓
Targeted tie-breaker if needed
    ↓
Select career
    ↓
STAGE 2 — EMPLOYER COMPARISON
    ↓
FIT FOR YOU
ENTRY DIFFICULTY
CAREER SIGNAL
SPECIALIZED EXPERIENCE
CONDITIONS
TRAJECTORY
    ↓
Select employer
    ↓
STAGE 3 — LOCATION / OFFICE / POSTING
    ↓
Specific opportunity fit + eligibility + readiness gaps
    ↓
Save / target / apply / compare offer
    ↓
WHAT SHOULD I DO NEXT?
    ↓
Skills / experience / training / recruiting actions
    ↓
User completes internship / class / job / project
    ↓
Camvince asks what changed
    ↓
New capabilities + actual task likes/dislikes + new goals
    ↓
New profile version
    ↓
Recalculate
    ↓
Explain what changed and why
    ↓
NEXT CAREER DECISION
    ↺
```

---

# 83. Why the Product Can Become More Accurate Over Time

At the beginning:

> "You think you would enjoy client work."

Confidence:

> low/medium.

After two internships with repeated actual exposure:

> "You repeatedly enjoyed stakeholder analysis but disliked recurring external-client service."

Confidence:

> higher.

The system becomes evidence-rich because it learns from behavior and real tasks.

This allows the product eventually to move from:

> **self-perception-heavy matching**

toward:

> **longitudinal evidence-backed career navigation.**

---

# 84. Final Competitive Confirmation

### Confirmed overlap

Camvince and CareerExplorer both involve:

- personal profiles,
- career matching,
- interests/preferences,
- history/education,
- salary/location considerations,
- career information,
- recommendation updates.

### Confirmed differentiation in the **current Camvince specification**

Camvince's planned core extends into:

- explicit evidence-based Readiness,
- Evidence Coverage,
- company × career profiles,
- person-relative Entry Difficulty,
- role-specific Career Signal,
- Specialized Experience,
- city/industry separation,
- office/posting specificity,
- inherited vs direct source logic,
- longitudinal Career Board,
- task-level post-internship/job profile learning,
- career-transition evidence,
- next-step skill-gap planning.

Based on CareerExplorer's official public materials reviewed for this document, those combined elements are not presented as the core CareerExplorer workflow.

### Final caveat

The differentiation exists **in the architecture**.

It will only become a defensible market difference if Camvince actually builds and validates the post-career-discovery layers.

A demo that only shows:

> assessment → Top 10 careers

will still look like CareerExplorer.

A demo that shows:

> career → readiness → company → difficulty/signal/experience → city/posting → next move → profile changes after real experience

will tell a substantially different story.

---

# 85. Source Notes

## Internal Camvince sources reviewed

- `Camvince Matching Model Reworked - Scoring Detail.xlsx` — latest September 1 scoring/data-pull specification
- `Camvince Matching Model Reworked.xlsx`
- `Camvince_Stress_Test_Expanded_Resume_Profile.xlsx`
- `Role Database - Vincent.docx` — verified 24-role universe, deep source check August 22, 2026
- `Camvince Expanded Agent Ready Business Plan.xlsx`
- `Camvince — Scoring Config & Website API.xlsx` — older scoring architecture retained for historical comparison
- `Camvince — Contradiction Control Center.xlsx` — used to identify older known scoring/profile/data-contract conflicts

## CareerExplorer official sources reviewed

- Career test: https://www.careerexplorer.com/career-test/
- Main platform: https://www.careerexplorer.com/
- How the career test works: https://www.careerexplorer.com/faqs/careerexplorer-career-test/how-does-careerexplorer-career-test-work/
- Why different scores: https://www.careerexplorer.com/faqs/assessment-science/why-am-i-given-different-scores/
- How to decide between recommended careers: https://www.careerexplorer.com/faqs/careerexplorer-career-test/how-do-i-decide-between-my-recommended-careers/
- Science / technical manual: https://www.careerexplorer.com/science/
- Reliability: https://www.careerexplorer.com/science/reliability/
- Career prediction validity: https://www.careerexplorer.com/science/career-prediction-validity/
- Organizations product: https://www.careerexplorer.com/for-organizations/
- Careers library: https://www.careerexplorer.com/careers/
- About: https://www.careerexplorer.com/about/

## CareerExplorer scale/acquisition source

- Penn Foster acquisition announcement, March 19, 2021:
  https://www.prnewswire.com/news-releases/penn-foster-acquires-pioneering-career-discovery-platform-301250853.html

The announcement reported 10M+ annual users at the time and did not disclose transaction terms. Current standalone CareerExplorer revenue is not publicly disclosed in a reliable company-reported source reviewed here.

## O*NET

- O*NET Web Services: https://services.onetcenter.org/
- O*NET Web Services terms: https://services.onetcenter.org/terms
- O*NET Web Services data license: https://services.onetcenter.org/help/license_data
- O*NET 31.0 database/license: https://www.onetcenter.org/database.html
- Database CC BY 4.0 license: https://www.onetcenter.org/license_db.html

## CareerOneStop

- Developer/Web API overview:
  https://www.careeronestop.org/Developers/WebAPI/web-api.aspx
- API Explorer:
  https://api.careeronestop.org/api-explorer/

## BLS

- API/developer information:
  https://www.bls.gov/developers/
- Terms:
  https://www.bls.gov/developers/termsOfService.htm

## BEA

- API:
  https://apps.bea.gov/api/

---

# 86. Final Source-of-Truth Statement

As of **September 1, 2026**, the intended Camvince product is:

> **A persistent, source-backed Career Decision Intelligence platform that builds a living profile of a user's current capabilities, actual work preferences, desired job conditions, and long-term trajectory; uses that profile first to rank careers, then to compare employers, locations, and specific opportunities; keeps current readiness, entry difficulty, career signal, specialized experience, conditions, and trajectory conceptually separate; tracks uncertainty and source freshness; remembers the user's decisions over time; and updates recommendations after real education and work experience so the product can answer not only "What career fits me?" but "What should I do, where should I do it, and what should I do next?"**

Everything else in the project should be updated to align with this statement unless a future explicit product decision supersedes it.
