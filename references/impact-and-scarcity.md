# Impact, Attribution, and Scarcity

Use this reference for ecosystem impact, popularity, technology scarcity,
AI-assisted development, and project-level attribution.

## Contents

1. Influence concepts
2. Evidence hierarchy
3. Project-to-person attribution
4. Normalization and aggregation
5. AI and automation attribution
6. Scarcity and market value
7. Failure modes

## 1. Influence concepts

Keep these constructs separate:

| Construct | Meaning | Example signals |
|---|---|---|
| Attention | People noticed or bookmarked the work. | Stars, followers, views, mentions. |
| Adoption | People actively use or depend on the work. | Reverse dependencies, installs, active integrations. |
| Authority | The person can shape accepted technical direction. | Maintainer/releaser role, merged RFCs, standards. |
| Technical leverage | The work enables or changes other engineering work. | Tooling, APIs, compilers, shared infrastructure. |
| Community leverage | The person helps others contribute and assume responsibility. | Reviews, contributor conversion, mentoring, governance. |
| Knowledge diffusion | Technical understanding spreads through reusable material. | Referenced docs, courses, examples, talks, curricula. |

Attention may help discover impact evidence. It is not a proxy for engineering
capability and receives only capped impact credit without corroboration.

## 2. Evidence hierarchy

### Strong adoption evidence

- Reverse dependencies or imports in active downstream projects.
- Sustained package, extension, image, or application usage from a credible
  registry or store.
- Official integration into established frameworks, standards, or documentation.
- Multiple independent organizations relying on the work.
- User-reported production use tied to inspectable issues or integrations.

### Strong authority evidence

- Public maintainer, committer, reviewer, or releaser responsibility supported
  by actual actions.
- Accepted RFC, PEP, specification, API, or compatibility policy.
- Repeated high-quality review of core changes.
- Release, migration, deprecation, or incident responsibility.

### Strong leverage evidence

- A tool or library removes repeated work for downstream developers.
- A contribution changes a core interface used across modules or repositories.
- Documentation or education becomes a durable reference and changes practice.
- Contributor workflows convert users into repeat contributors or maintainers.

### Weak standalone evidence

- Stars, followers, views, repository count, forks without active divergence.
- Organization membership without verified responsibility.
- A trivial contribution to a famous repository.
- Downloads that may be dominated by CI or mirrors and lack corroboration.
- Marketing claims without an inspectable downstream artifact.

## 3. Project-to-person attribution

Estimate attributable impact for each project:

`attributed_project_impact = project_influence × attribution × depth × responsibility × relevance`

Where:

- `project_influence` — adoption, leverage, authority, community, and
  durable reach; normalize before combining.
- `attribution` — authorship and ownership attribution, 0–1.
- `depth` — contribution depth, 0–1.
- `responsibility` — sustained responsibility, 0–1.
- `relevance` — current relevance or time factor, 0–1.

Use the formula as a reasoning scaffold, not false precision.

### Attribution anchors

| Verified role | Typical A range |
|---|---:|
| Organization member, no verified work | 0 |
| Formatting or isolated documentation fix | 0.01–0.05 |
| Scoped merged implementation | 0.05–0.20 |
| Major feature or repeated subsystem work | 0.20–0.50 |
| Module owner, recurring reviewer, or releaser | 0.50–0.80 |
| Original creator with sustained active stewardship | 0.70–1.00 |

Adjust within a range using direct evidence. Do not infer an exact share from
lines of code or commit count alone.

### Depth anchors

- 0.05: Cosmetic, generated, or mechanical change.
- 0.20: Narrow fix with limited effect radius.
- 0.40: Meaningful feature or bug fix with tests.
- 0.60: Core subsystem change or cross-module refactor.
- 0.80: Architecture, public API, compatibility, or release-shaping work.
- 1.00: Durable technical direction across a major system or ecosystem.

## 4. Normalization and aggregation

### Normalize within a credible cohort

Account for:

- language and package ecosystem;
- project type: library, application, tutorial, hardware, kernel, standard;
- project age and observation window;
- geographic or market scope only when explicitly relevant;
- bot, mirror, CI, and registry-specific noise.

Use logarithmic compression, percentile ranks, winsorization, or Bayesian
shrinkage when calculating numeric features. Never compare raw downloads or
stars across unrelated ecosystems as if they were equivalent.

### Apply diminishing returns across projects

Do not reward portfolio size linearly. A practical aggregation is:

`I_projects = p1 + 0.6p2 + 0.4p3 + 0.25 × sum(p4...)`

where projects are sorted by attributable impact. Normalize the result to the
0–100 I rubric. This prevents dozens of tutorial or generated repositories from
overwhelming one deeply influential project.

### Prevent double counting

- A reverse dependency may support adoption and leverage, but count the same
  downstream only once in the project ledger.
- Maintainer status supports authority; the related merge actions should not be
  added again as independent authority points without new information.
- Educational reach may support knowledge diffusion, not implementation quality.
- A famous upstream project increases potential effect radius only after the
  person's actual contribution depth is verified.

## 5. AI and automation attribution

Record four independent roles:

| Role | Evidence |
|---|---|
| Implementation authorship | Commit authors, co-authors, disclosures, bot accounts, generated files. |
| Decision authorship | Issue specification, design rationale, constraints, rejected alternatives. |
| Verification authorship | Test strategy, review comments, failure analysis, requested revisions. |
| Accountability | Merge, release, maintenance, incident response, user support, rollback. |

Rules:

- Do not infer AI use without disclosure or direct evidence.
- Do not assign full direct-code credit when an agent or bot authored the change.
- Do not erase architecture, verification, stewardship, or impact credit merely
  because implementation was automated.
- Raise confidence when the person documents constraints, reviews diffs,
  validates failures, and handles post-release consequences.
- Lower attribution confidence when large self-merged generated changes have no
  inspectable design, review, or validation trail.

## 6. Scarcity and market value

Scarcity describes supply, not capability or demand.

Before assigning R, define:

- the skill bundle, not a single technology keyword;
- minimum demonstrated depth;
- relevant ecosystem, region, and date;
- comparison cohort and data source;
- adjacent skills that could substitute.

Distinguish:

- **difficulty**: handled in E through constraint depth;
- **scarcity**: optional R based on relative supply;
- **demand**: external market or organizational need;
- **value**: interaction of capability, role fit, scarcity, demand, and impact.

Do not calculate market value from GitHub alone. If current market data is
available, report a separate role-value analysis with source date and region.

## 7. Failure modes

- Celebrity bias: allowing followers to influence E or S.
- Fame inheritance: crediting a contributor with the entire upstream project's
  impact.
- Ecosystem bias: comparing raw JavaScript adoption with a niche compiler or
  hardware project.
- Age bias: rewarding old projects without checking current relevance, or
  penalizing young projects without a separate trajectory measure.
- Automation bias: treating agent use as either automatic excellence or
  automatic disqualification.
- Hardware blindness: requiring software-style unit tests while ignoring
  measurement, fixtures, revisions, safety, and hardware-in-the-loop evidence.
- Open-PR inflation: treating ambitious unmerged work as realized impact.
- Portfolio inflation: summing forks, generated repositories, tutorials, and
  mirrors as independent projects.
