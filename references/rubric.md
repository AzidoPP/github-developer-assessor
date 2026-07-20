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
| 0 | Applicable evidence was inspected and shows no credited behavior, a material counterexample, or work wholly attributable elsewhere. Mere absence is `unknown`, not 0. |
| 1 | Exploratory, copied, fragile, or narrowly supervised evidence. |
| 2 | Completes ordinary scoped work; important boundaries remain weak. |
| 3 | Independently handles meaningful work with appropriate quality. |
| 4 | Handles difficult constraints, cross-module effects, and sustained responsibility. |
| 5 | Repeatedly shapes major systems, practices, or ecosystems with durable judgment. |

`unknown` is a status outside the scale. Use it when evidence is missing,
inaccessible, inapplicable to the sampled context, or too ambiguous to support a
judgment. Never convert `unknown` to 0.

`not_assessed` is also outside the scale. Use it when the selected assessment
mode intentionally excludes a subdimension. It differs from `unknown`: no
applicable inspection was attempted. Never convert `not_assessed` to 0 or treat
it as negative evidence.

### Scoring and evidence rules

- Score a subdimension only after inspecting applicable evidence and verifying
  at least weak attribution to the subject.
- Score only evidence types permitted by the selected assessment mode. A
  `quick` or `standard` assessment must not turn source-dependent impressions
  into scored evidence.
- Attach at least one concrete evidence item and an attribution rationale to
  every scored subdimension.
- Use only whole or half anchors. A half point requires evidence of meaningful
  behavior from both adjacent anchors; do not use arbitrary decimals.
- One substantive artifact normally caps a subdimension at 3. Multiple
  independent behaviors within one artifact may justify an exception, but the
  report must identify them and explain why the artifact is unusually
  information-dense.
- Repeated artifacts from one repository may support 4 when they demonstrate
  distinct constraints, decisions, or lifecycle stages rather than duplicate
  the same behavior.
- A 5 normally requires repeated evidence across time plus independent external
  validation, cross-project transfer, or project-wide responsibility. A single
  famous contribution never earns 5 by reputation alone.
- Evidence quantity does not add linearly. Prefer a few independent,
  high-information artifacts over many mechanical or correlated artifacts.

### Axis completeness

Calculate `known_weight` as the sum of weights for scored subdimensions.
Both `unknown` and `not_assessed` contribute zero known weight, retain their
distinct explanations, and remain bounded by 0–5 only for the mathematical
axis interval.

- `known_weight < 60`: report the axis as `unknown` and explain the missing
  evidence.
- `60 <= known_weight < 100`: report an interval, not a point estimate. The
  lower and upper bounds preserve the scored contribution and bound each
  unknown subdimension to 0–5; do not silently renormalize known weights. With
  `known_contribution = sum(scored_anchor / 5 * weight)`, report the mathematical
  interval `[known_contribution, known_contribution + (100 - known_weight)]`.
  Its lower bound is not an assertion that unknown dimensions deserve 0.
- `known_weight = 100`: a point estimate is allowed. Display it as a whole
  number while retaining half-anchor inputs internally.
- Low overall confidence overrides numerical completeness: prefer an interval
  or qualitative result even when every subdimension has a score.

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

### Source-inspection eligibility

- Implementation quality requires direct inspection of source or diff contents
  under the Deep Source Inspection Protocol. Mark it `not_assessed` in `quick`
  and `standard` mode.
- In `standard`, score Architecture and interfaces, Problem solving and
  debugging, Correctness and reliability, or Constraint depth only from
  explicit non-source evidence such as RFCs, issue and PR reasoning,
  subject-authored reviews, CI and release outcomes, migrations, incidents, and
  downstream consequences. Limit each claim to what that evidence establishes.
- Evidence surface is inherited. A source-derived conclusion remains source-
  derived when quoted in a summary, prior assessment, or calibration packet.
  Standard must re-derive each E anchor from explicitly eligible non-source
  observations; otherwise mark that subdimension `unknown`.
- A passing CI run, test count, coverage number, linter result, release, or lack
  of reported incidents does not by itself establish source-level correctness
  or implementation quality.
- Because Implementation quality is intentionally not assessed in `standard`,
  Standard E is always an interval or `unknown`; do not report a point estimate
  or renormalize the remaining 80 weight.
- In `deep`, use source review packets from `source-inspection.md` for every
  source-dependent score. Targeted source sampling still does not establish
  whole-repository quality.

### Engineering behavioral anchors

| Subdimension | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Implementation quality | Mostly copied, monolithic, fragile, or happy-path implementation. | Completes ordinary implementation, but abstractions, error handling, or change discipline have material gaps. | Produces clear, proportionate implementation with sensible failure handling and reviewable changes. | Improves difficult core code across modules while preserving behavior, resource safety, and maintainability. | Repeatedly establishes implementation patterns that improve complex systems and are adopted or sustained by others. |
| Architecture and interfaces | Boundaries are unclear, accidental, or tightly coupled. | Introduces useful structure, but contracts, evolution, or effect radius remain weakly handled. | Designs modules and interfaces appropriate to project scale and expected change. | Coordinates cross-module architecture under compatibility, migration, or ecosystem constraints. | Repeatedly shapes durable system or ecosystem interfaces with externally validated technical judgment. |
| Problem solving and debugging | Applies symptom patches without traceable reasoning. | Reproduces ordinary failures but root-cause reasoning or prevention is incomplete. | Reproduces, narrows, fixes, and validates meaningful problems. | Resolves ambiguous cross-layer, performance, concurrency, or lifecycle failures and adds prevention. | Repeatedly leads difficult diagnosis, improves project-wide debugging practice, and prevents recurrence across contexts. |
| Correctness and reliability | Provides little validation beyond manual happy paths. | Adds basic tests or checks, but important boundaries, regressions, or environment differences remain exposed. | Validates core behavior and important regressions appropriately for the project type. | Handles difficult failure, concurrency, compatibility, recovery, release, or physical-validation paths across modules. | Repeatedly establishes project-wide correctness, release-safety, compatibility, incident-prevention, or validation systems. |
| Constraint depth | Uses frameworks or technologies without demonstrating difficult constraints. | Handles one modest role-relevant constraint with limited interaction or consequence. | Demonstrates solid depth in at least one non-trivial correctness, performance, platform, physical, operational, or domain constraint. | Handles multiple coupled constraints with explicit trade-offs and validation. | Repeatedly resolves tightly coupled constraints across systems or domains and transfers that judgment to new contexts. |

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

### Stewardship behavioral anchors

| Subdimension | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Ownership and delivery | Shows isolated uploads or incomplete work without visible follow-through. | Delivers scoped tasks or a small project but relies on narrow context or limited lifecycle responsibility. | Repeatedly delivers a meaningful project or subsystem end to end. | Coordinates delivery across modules, contributors, or operational boundaries and owns consequences. | Repeatedly establishes direction and durable accountability for major shared systems. |
| Maintenance and release | Shows little follow-up after initial implementation. | Performs occasional fixes, dependency updates, or informal releases with limited compatibility planning. | Sustains releases, regressions, dependencies, and technical debt for a meaningful project or subsystem. | Manages migrations, deprecations, recovery, compatibility, or release risk across versions and consumers. | Repeatedly shapes durable maintenance, compatibility, release, and incident-response practices across an ecosystem or major system. |
| Collaboration and review | Interaction is absent, superficial, or resistant to substantive feedback in inspected applicable evidence. | Responds constructively to ordinary feedback or supports narrowly scoped contributors. | Provides useful technical review, design discussion, issue support, and follow-through. | Repeatedly improves correctness or design across contributors and helps difficult changes succeed. | Establishes high-quality review culture and multiplies the judgment and effectiveness of other contributors over time. |
| Governance and contributor leverage | Shows no credited governance behavior in inspected contexts where it was applicable. | Performs occasional triage, merge, release, or contributor guidance without durable process ownership. | Holds recurring merge, release, roadmap, standards, mentoring, or contributor-pathway responsibility. | Coordinates governance across contributors, reduces bus factor, and makes technical decision processes durable. | Repeatedly develops maintainers or institutions and shapes durable governance beyond personal execution. |

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

### Impact behavioral anchors

| Subdimension | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Adoption | Attention or isolated self-reported use without sustained independent adoption. | Limited verified use by a small number of independent users or projects. | Sustained verified use across multiple active downstreams or one meaningful organization. | Broad or strategically important adoption across independent organizations, ecosystems, or production contexts. | Durable, ecosystem-shaping adoption with continued dependence across major independent consumers. |
| Downstream technical leverage | Helps a narrow local workflow with little verified downstream effect. | Saves repeated work for a small set of external users or projects. | Enables meaningful downstream engineering through a reusable API, tool, library, or practice. | Changes workflows or system capabilities across multiple independent teams or projects. | Repeatedly establishes foundational technical leverage across a major ecosystem or class of systems. |
| Authority and standards | Informal influence or membership without verified decision responsibility. | Occasional accepted decisions, releases, or scoped authority. | Recurring maintainer, releaser, reviewer, RFC, or interface authority supported by actual actions. | Shapes important technical direction, compatibility, standards, or accepted interfaces across contributors. | Holds durable, independently recognized authority that repeatedly shapes ecosystem-level technical direction. |
| Community leverage | Provides isolated support without visible contributor progression. | Helps users or occasional contributors complete scoped work. | Repeatedly reviews, mentors, or converts users into successful contributors. | Builds contributor pathways, distributes ownership, and reduces bus factor across a project. | Repeatedly develops maintainers or durable contributor communities across projects or years. |
| Knowledge diffusion | Publishes useful material with limited evidence of reuse. | Material is referenced or reused by a small external audience. | Produces durable documentation, examples, courses, or explanations adopted in real technical practice. | Material becomes a widely reused reference or measurably changes practice across communities. | Repeatedly establishes enduring educational or technical references that shape ecosystem understanding. |
| Durable reach | Evidence is recent, transient, or not yet sustained. | Use or responsibility persists beyond an initial release or activity burst. | Verified relevance, users, or supported versions persist across a meaningful multi-release period. | Important downstream dependence or authority survives ecosystem and version changes over several years. | The contribution remains foundational and actively depended upon across major transitions and long time horizons. |

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

### Trajectory behavioral anchors

Score change relative to the subject's earlier inspectable evidence, not
distance from a prestige benchmark. If two comparable periods are unavailable,
report T as `unknown`.

| Subdimension | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Difficulty progression | Recent work is less demanding or remains at the same exploratory level without visible consolidation. | Shows modest movement toward harder tasks or constraints, with inconsistent validation. | Shows clear progression toward more difficult constraints and central code paths. | Progresses across multiple constraint classes or from scoped work to difficult system-level problems. | Demonstrates sustained, externally validated progression into substantially harder and broader technical responsibility. |
| Independent external validation | Work receives little substantive external validation or repeatedly fails to address review concerns. | Receives occasional acceptance or useful feedback on scoped work. | Earns repeated substantive review acceptance, maintainer trust, or successful upstream outcomes. | Gains responsibility for important changes through repeated high-quality external validation. | External maintainers or users repeatedly rely on the subject's judgment for major technical direction or difficult work. |
| Learning and follow-through | Repeats avoidable problems or leaves substantive feedback and failures unresolved. | Responds to some feedback but follow-through or prevention remains inconsistent. | Incorporates feedback, closes meaningful work, and adds regression or process improvements. | Converts setbacks into durable technical or workflow improvements across later work. | Repeatedly demonstrates rapid, durable learning that changes project practice or enables qualitatively harder responsibility. |
| Scope expansion | Scope remains narrow or shifts without evidence of increased responsibility. | Expands from isolated tasks to small features or limited ownership. | Moves from tasks to subsystems, implementation to design, or isolated work to recurring collaboration. | Expands across system boundaries, lifecycle stages, or contributor responsibility while maintaining quality. | Sustains major expansion into technical direction, cross-system ownership, or contributor multiplication with external validation. |

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

### Scarcity behavioral anchors

These anchors are valid only within a named, dated, and credibly sampled cohort.
Without that frame, report R as `unknown` regardless of perceived niche status.

| Subdimension | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Supply scarcity | Comparable verified depth is common in the defined cohort. | Supply is somewhat constrained but adjacent candidates are readily available. | Comparable verified depth is meaningfully uncommon in the cohort. | Few cohort members demonstrate the full required depth or combination. | Comparable verified depth is exceptionally rare under a credible sampling frame. |
| Learning and infrastructure barriers | Skills and validation environments are broadly accessible with short feedback cycles. | Requires some specialized setup or sustained learning beyond common practice. | Requires material toolchain, hardware, data, environment, or time investment. | Requires difficult-to-access infrastructure or prolonged learning with costly feedback. | Requires exceptional accumulated practice and infrastructure that is rarely reproducible in the cohort. |
| Cross-domain coupling | Work is contained within one common domain. | Requires limited coordination with an adjacent domain. | Requires competent integration of multiple technical domains. | Requires deep judgment across several tightly coupled domains. | Requires rare, sustained mastery of a combination whose parts cannot be separated safely or effectively. |
| Failure and feedback cost | Failures are cheap, safe, and quickly reproducible. | Some failures require non-trivial environments or delayed feedback. | Validation has meaningful cost, latency, safety, or reproduction difficulty. | Failures are expensive, slow, safety-relevant, or difficult to isolate across systems. | Feedback is exceptionally costly or hazardous and demands rare prevention and validation discipline. |
| Substitution difficulty | Common adjacent skills substitute with little ramp-up. | Substitution is practical with modest onboarding. | Adjacent experts require material ramp-up or support to perform effectively. | Few adjacent profiles can substitute without major capability or infrastructure gaps. | The verified combination has almost no credible short-term substitutes in the defined cohort. |

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
An assessment that intentionally omits source inspection has lower source-
coverage completeness, not a lower developer score. Record the omitted surface
as `not_assessed` and reflect it in C.

## 7. Interpretation rules

### Criterion-referenced versus relative output

- E and S are criterion-referenced.
- I is evidence-based but ecosystem-normalized.
- T is time-window-relative to the person's earlier evidence.
- R and cohort percentile are explicitly relative.
- A comparison set must not alter E or S.

### Missing versus negative evidence

- Intentionally excluded evidence: `not_assessed` under the selected mode. Do
  not treat it as attempted inspection or developer weakness.
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
