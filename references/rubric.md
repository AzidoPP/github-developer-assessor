# Multi-Axis Assessment Rubric

Use this rubric to score separate constructs. Do not collapse missing axes into
zero and do not call a composite score “engineering capability.”

## Contents

1. Engineering capability (E)
2. Stewardship and ownership (S)
3. Ecosystem impact (I)
4. Development trajectory (T)
5. Technology scarcity (R)
6. Confidence (C)
7. Interpretation rules

## Shared 0–5 anchors

Apply these anchors to each subdimension, then use the dimension-specific notes
below.

| Score | General anchor |
|---:|---|
| 0 | Relevant inspectable evidence shows no credited behavior, or the work is wholly attributable elsewhere. Mere absence is unknown, not 0. |
| 1 | Exploratory, copied, fragile, or narrowly supervised evidence. |
| 2 | Completes ordinary scoped work; important boundaries remain weak. |
| 3 | Independently handles meaningful work with appropriate quality. |
| 4 | Handles difficult constraints, cross-module effects, and sustained responsibility. |
| 5 | Repeatedly shapes major systems, practices, or ecosystems with durable judgment. |

Use half points only when evidence genuinely falls between anchors. Attach at
least one concrete evidence item to every scored subdimension.

## 1. Engineering capability (E) — 0–100

E is criterion-referenced. The same evidence receives the same score regardless
of the comparison set, popularity, employer, followers, or technology scarcity.

| Subdimension | Weight | What to evaluate |
|---|---:|---|
| Implementation quality | 20 | Readability, data structures, error handling, resource management, appropriate abstraction, change discipline. |
| Architecture and interfaces | 25 | Module boundaries, API/contracts, cross-module reasoning, extensibility, compatibility, migration design. |
| Problem solving and debugging | 20 | Reproduction, root cause, trade-offs, performance analysis, cross-layer diagnosis, prevention. |
| Correctness and reliability | 20 | Tests, edge cases, concurrency, failure handling, CI, release safety, physical validation where applicable. |
| Constraint depth | 15 | Demonstrated handling of difficult correctness, performance, platform, physical, operational, or domain constraints. |

Calculate:

`E = sum(subdimension_score / 5 * weight)`

### Engineering anchors

#### Implementation quality

- 1: Mostly copied, monolithic, or happy-path code.
- 3: Clear and proportionate implementation with sensible failure handling.
- 5: Repeatedly improves complex core code while preserving behavior and
  reviewability.

#### Architecture and interfaces

- 1: Boundaries are unclear or accidental.
- 3: Modules and interfaces fit the project scale.
- 5: Repeated architecture judgment under compatibility and ecosystem
  constraints.

#### Problem solving and debugging

- 1: Symptom patches without traceable reasoning.
- 3: Reproduces, narrows, fixes, and validates meaningful problems.
- 5: Leads diagnosis of ambiguous, cross-layer, performance, concurrency, or
  lifecycle failures and improves prevention.

#### Correctness and reliability

- 1: Little validation beyond manual happy paths.
- 3: Core behavior and regressions are tested appropriately for project type.
- 5: Shapes project-wide correctness, compatibility, release safety, physical
  validation, or incident prevention.

#### Constraint depth

- 1: Surface use of frameworks without difficult constraints.
- 3: Solid role-relevant depth in at least one non-trivial constraint class.
- 5: Repeatedly handles multiple tightly coupled constraints, such as ABI plus
  performance, concurrency plus recovery, or firmware plus measured hardware.

Rarity alone never raises this score.

## 2. Stewardship and ownership (S) — 0–100

S measures responsibility for systems and contributors, not raw activity.

| Subdimension | Weight | What to evaluate |
|---|---:|---|
| Ownership and delivery | 30 | End-to-end delivery, subsystem responsibility, follow-through, operational accountability. |
| Maintenance and release | 25 | Releases, migrations, compatibility, deprecation, dependency work, recovery, technical debt. |
| Collaboration and review | 25 | Review quality, design discussion, feedback response, issue support, helping contributors succeed. |
| Governance and contributor leverage | 20 | Merge/release responsibility, standards, roadmap stewardship, mentoring, contributor pathways, bus-factor reduction. |

Calculate:

`S = sum(subdimension_score / 5 * weight)`

### Stewardship anchors

- 0–1: Relevant sampled evidence shows no sustained responsibility, or only
  one-time uploads without follow-through. If responsibility evidence is merely
  unavailable, report it as unknown instead.
- 2: Owns small projects or completes scoped collaborative work.
- 3: Sustains a meaningful project or subsystem and participates constructively
  in collaboration and releases.
- 4: Coordinates changes across modules or contributors and manages
  compatibility, releases, or operational consequences.
- 5: Demonstrates durable technical stewardship, high-quality reviews,
  governance, contributor development, and ecosystem responsibility.

AI or bot implementation does not remove S credit when specification, decision,
verification, and accountability are directly evidenced. It does reduce
implementation attribution where appropriate.

## 3. Ecosystem impact (I) — 0–100

Use `impact-and-scarcity.md` before scoring I.

| Subdimension | Weight | What to evaluate |
|---|---:|---|
| Adoption | 30 | Sustained downstream use, reverse dependencies, installations, integrations, organizational diversity. |
| Downstream technical leverage | 20 | How much other engineering work the project, API, tool, or standard enables. |
| Authority and standards | 20 | Maintainer/releaser authority, accepted RFCs/PEPs, official adoption, ecosystem interfaces. |
| Community leverage | 15 | Contributor growth, reviews, responsiveness, contributor conversion, reduced bus factor. |
| Knowledge diffusion | 10 | Durable technical education, referenced documentation, examples, courses, or practices. |
| Durable reach | 5 | Multi-year relevance, retained users, supported versions, continued downstream dependence. |

Calculate I only after project-level influence is multiplied by verified
individual attribution. Attention-only evidence may contribute at most 5 points
to I unless corroborated by adoption, authority, or downstream use.

## 4. Development trajectory (T) — 0–100

T describes direction and momentum, not realized impact or employment level.

| Subdimension | Weight | What to evaluate |
|---|---:|---|
| Difficulty progression | 30 | Whether recent work moves toward harder constraints and more central code paths. |
| Independent external validation | 25 | Review quality, acceptance, maintainer trust, promotion, or repeated upstream success. |
| Learning and follow-through | 25 | Response to feedback, iteration quality, regression follow-up, closure after setbacks. |
| Scope expansion | 20 | Growth from tasks to subsystems, implementation to design, or individual work to contributor responsibility. |

Compare 6-, 12-, and 24-month windows. Do not equate a burst of generated
repositories or raw commits with trajectory.

### Open-change evidence weights

Use these as navigation defaults, then inspect discussion quality:

| State | Maximum realized-work credit |
|---|---:|
| Submitted, no review | 0.15 |
| CI passes or substantive discussion | 0.35 |
| Positive maintainer feedback with requested changes | 0.55 |
| Approved, awaiting merge | 0.80 |
| Merged | 1.00 |
| Released or demonstrably adopted | Add impact evidence separately |

Unmerged work may raise T and provide partial E evidence. It does not create
realized I merely because the target repository is famous.

## 5. Technology scarcity (R) — optional, 0–100

R is cohort-relative and time-sensitive. It is not an engineering score.

| Subdimension | Weight | What to evaluate |
|---|---:|---|
| Supply scarcity | 25 | Estimated availability of developers with comparable verified depth. |
| Learning and infrastructure barriers | 25 | Toolchains, hardware, data, environments, and time required to become effective. |
| Cross-domain coupling | 20 | Need to combine multiple technical domains correctly. |
| Failure and feedback cost | 20 | Cost, latency, safety, or difficulty of reproducing and validating failures. |
| Substitution difficulty | 10 | How readily adjacent skills can replace the demonstrated specialty. |

Requirements:

- Define the cohort, date, region if relevant, and evidence source.
- Normalize within role and ecosystem.
- Report R as unknown when the cohort cannot be credibly estimated.
- Never infer market demand from GitHub rarity.
- Never add R to E.

## 6. Confidence (C)

Report four confidence components:

| Component | Question |
|---|---|
| Evidence coverage | Were code, tests, history, reviews, releases, and impact surfaces sampled? |
| Attribution | Is the person's role distinguishable from upstream, teammates, bots, and agents? |
| Sampling stability | Would a different reasonable project or PR sample likely change the result? |
| Identity certainty | Is the account linkage clear? |

Assign an overall confidence:

- **High**: Multiple independent evidence types, direct code inspection,
  verified contribution, stable sampling, little identity ambiguity.
- **Medium**: Direct evidence exists but important axes, authorship, or project
  history remain incomplete.
- **Low**: Mostly profile-level signals, sparse artifacts, unclear attribution,
  or inaccessible work.

For low confidence, prefer bands and qualitative ranges over precise totals.

## 7. Interpretation rules

### Criterion-referenced versus relative output

- E and S are criterion-referenced.
- I is evidence-based but ecosystem-normalized.
- T is time-window-relative to the person's earlier evidence.
- R and cohort percentile are explicitly relative.
- A comparison set must not alter E or S.

### Missing versus negative evidence

- Missing evidence: unknown, inaccessible, or outside GitHub. Do not score as a
  demonstrated strength or weakness.
- Negative evidence: an inspectable failure, regression pattern, abandoned
  compatibility promise, poor review behavior, or missing validation that the
  project context reasonably required.

### Domain fairness

Evaluate validation proportionally:

- Libraries may require compatibility matrices and type/API tests.
- Applications may emphasize integration, migration, and operational paths.
- Hardware may rely on measurements, test fixtures, schematics, revisions, and
  hardware-in-the-loop evidence rather than conventional unit tests alone.
- Kernels and compilers may rely on regression suites, architecture matrices,
  benchmarks, and formal interface constraints.
- Educational projects may demonstrate knowledge diffusion and developer
  experience but need separate code or governance evidence for high E/S scores.

### No automatic market-value score

Market value depends on capability, role fit, scarcity, demand, location,
industry, and business impact. GitHub alone does not establish these inputs.
Only estimate it when the user supplies or authorizes current external market
data, and label the result separately from E/S/I/T/R.
