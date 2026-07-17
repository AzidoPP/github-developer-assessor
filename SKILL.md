---
name: github-developer-assessor
description: Evidence-first assessment of a developer's publicly demonstrated engineering capability from a GitHub account. Use when evaluating an account, comparing candidates, reviewing open-source experience, or preparing technical interview questions. Examines personal repositories, organization contributions, code, commits, pull requests, reviews, issues, tests, releases, and maintenance history without treating popularity metrics as proof of skill.
---

# GitHub Developer Assessor

## Purpose

Assess what a developer has **publicly demonstrated** on GitHub. Produce a traceable, role-aware report based on concrete evidence rather than stars, followers, contribution counts, organization badges, or polished README files alone.

This skill does not claim to measure a person's complete ability. Private work, unlinked identities, inaccessible organization repositories, and offline engineering experience may be absent.

## Use this skill when

- A user asks how strong a developer appears from a GitHub account.
- A recruiter or hiring manager wants an evidence-based technical screen.
- A maintainer wants to understand a potential contributor's experience.
- A user wants to compare two or more GitHub accounts.
- A developer wants feedback on how their public profile communicates engineering ability.

Do not use it to infer protected traits, personal ideology, health, financial status, or other sensitive personal characteristics.

## Inputs

Required:

- `github_account`: GitHub username or profile URL.

Optional:

- `target_role`: e.g. backend, frontend, mobile, ML, data, DevOps/SRE, systems, security, developer tools.
- `expected_level`: e.g. internship, junior, mid-level, senior, staff. Treat this only as a comparison target, not a conclusion.
- `depth`: `quick`, `standard`, or `deep`. Default: `standard`.
- `time_window`: Default: the most recent 24 months, while retaining older projects that show substantial ownership or influence.
- `comparison_accounts`: Other GitHub accounts to assess under the same rubric.
- `known_context`: Candidate-provided project descriptions, resume claims, aliases, or repository links.

## Non-negotiable rules

1. Use public evidence only. Do not attempt to access private repositories, leaked credentials, hidden endpoints, or non-public data.
2. Separate **membership**, **activity**, **contribution**, **ownership**, and **leadership**. They are not equivalent.
3. Organization membership alone is weak evidence. Inspect actual commits, pull requests, reviews, issues, releases, or ownership in organization repositories.
4. Do not treat stars, followers, green contribution graphs, repository count, or raw lines of code as direct skill scores.
5. Distinguish original work from forks, mirrors, generated code, tutorial copies, dependency vendoring, mass formatting, and repository imports.
6. Cite every material conclusion with a repository, commit, pull request, issue, review, release, file, or discussion URL when tools allow.
7. Mark missing or inaccessible evidence as unknown. Never convert absence of public evidence into a negative claim about the person.
8. Do not merge identities across accounts unless the linkage is explicit or strongly evidenced. State any identity uncertainty.
9. Evaluate code in project context. Small scripts do not require enterprise architecture; large services do.
10. Report confidence separately from score. A high score based on sparse evidence is not acceptable.

## Assessment modes

### Quick

Use for a first-pass screen.

- Inspect the profile, organizations, and contribution surface.
- Select up to 3 representative repositories.
- Inspect recent commits and at least 2 meaningful PRs or issues where available.
- Sample core code, tests, and CI configuration.
- Produce a compact scorecard, evidence summary, and uncertainties.

### Standard

Use by default.

- Select 3–5 representative repositories across personal, organization, and external contribution contexts.
- Inspect code, commit history, PRs, reviews, issues, releases, tests, CI, and maintenance activity.
- Verify the person's actual contribution to each selected project.
- Apply the role-specific lens and full scoring rubric.
- Produce interview probes tied to observed evidence.

### Deep

Use for high-stakes evaluation or maintainer due diligence.

- Trace major features across issues, design discussions, commits, PRs, reviews, and releases.
- Compare earlier and later code to evaluate technical evolution.
- Inspect cross-repository contributions and organization influence.
- Analyze architecture, reliability, compatibility, performance, security, and governance signals where relevant.
- Include conflicting evidence and alternative interpretations.

## Workflow

### Step 1: Normalize scope

Record:

- Canonical account URL and username.
- Target role and expected level, if provided.
- Assessment depth and time window.
- Whether the report evaluates general engineering ability or role-specific evidence.

If the account no longer exists, is private, or is mostly inaccessible, stop and explain the limitation.

### Step 2: Build an evidence map

Collect candidate evidence from:

- Pinned repositories.
- Recently active non-fork repositories.
- Repositories with sustained maintenance.
- Repositories where the account is a major contributor but not the owner.
- Organization repositories with actual contributions.
- External pull requests and reviews.
- Issue triage, discussions, release work, and governance activity.

Classify each repository:

- `personal-original`
- `organization-contribution`
- `external-contribution`
- `fork-or-mirror`
- `tutorial-or-experiment`
- `uncertain`

Do not discard small repositories automatically. A small repository may contain strong systems, algorithmic, testing, or tooling evidence.

### Step 3: Verify actual contribution

For each selected repository, determine:

- Whether the account created or imported the repository.
- Approximate contribution scope and time span.
- Whether commits touch core logic, tests, documentation, CI, release tooling, or only superficial files.
- Whether the account authored major PRs, reviewed others, handled issues, or published releases.
- Whether commits were squashed, rebased, co-authored, or migrated in a way that makes raw counts unreliable.

Use commit counts only as navigation hints. Prefer direct inspection of diffs and discussion history.

### Step 4: Inspect organizations

For each visible organization:

1. Check whether the organization is active and technically substantive.
2. Find repositories where the account has verifiable activity.
3. Inspect the person's role through evidence, not badges:
   - contributor
   - recurring contributor
   - module owner
   - reviewer
   - releaser
   - maintainer
   - organization owner, only when public and relevant
4. Evaluate the impact radius of contributions:
   - documentation or formatting
   - isolated implementation
   - core module changes
   - cross-module refactoring
   - architecture or API design
   - release, governance, or maintenance responsibility

Organization membership without visible work must be reported as context only, not scored as technical evidence.

### Step 5: Select representative projects

Prefer projects that maximize evidence quality, not popularity.

A representative set should cover, when available:

- One project showing end-to-end ownership.
- One collaborative or organization project.
- One external contribution to an established codebase.
- One long-lived project showing maintenance and evolution.
- One role-specific project relevant to the requested position.

For each project, record:

- Problem solved and apparent users.
- Person's role and evidence of ownership.
- Technical complexity.
- Code quality and architecture.
- Tests and reliability practices.
- Release and maintenance history.
- Collaboration evidence.
- Important limitations or ambiguity.

### Step 6: Sample code deliberately

Do not read random files only. Sample:

- Entry point or public API.
- Core domain or algorithm module.
- Data model or state-management layer.
- Error-handling path.
- Tests for core behavior and edge cases.
- Build, CI, deployment, or packaging configuration.
- At least one recent meaningful diff.

Evaluate proportionally to project size:

- Clarity of module boundaries.
- Appropriateness of abstractions.
- Naming and readability.
- Handling of invalid input and failure paths.
- Concurrency, resource lifecycle, transaction, or state correctness when relevant.
- Compatibility and migration awareness.
- Security-sensitive handling when relevant.
- Test quality rather than test count alone.
- Whether comments explain rationale rather than restating code.

### Step 7: Inspect problem-solving behavior

Use issues, PRs, discussions, and commits to determine whether the account can:

- Reproduce and narrow problems.
- Identify root causes rather than patch symptoms.
- Explain trade-offs.
- Add regression tests.
- Respond to review feedback constructively.
- Challenge suggestions with technical reasoning.
- Break large work into reviewable changes.
- Follow through after merge when regressions or compatibility issues arise.

A polished final diff is weaker evidence than a traceable problem-solving process.

### Step 8: Inspect collaboration and review quality

Look for:

- Reviews given to other contributors.
- Design feedback and API reasoning.
- Identification of correctness, compatibility, performance, security, or maintainability issues.
- Ability to distinguish blocking concerns from stylistic preferences.
- Clear, respectful communication.
- Issue triage, labeling, reproduction, and user support.

Review quality can be a stronger seniority signal than code volume.

### Step 9: Inspect maintenance and delivery

Check whether projects have lived beyond an initial demo:

- Multiple releases or meaningful version history.
- Changelogs and migration notes.
- Dependency upgrades.
- Backward-compatibility decisions.
- CI stability and release automation.
- Bug fixes after user reports.
- Deprecation, rollback, or recovery practices.
- Documentation updates accompanying behavior changes.

Do not punish a project for lacking infrastructure that is unnecessary at its scale.

### Step 10: Apply the role-specific lens

#### Backend

Emphasize API boundaries, data modeling, transactions, concurrency, caching, failure handling, observability, migrations, and deployment.

#### Frontend

Emphasize component boundaries, state management, accessibility, performance, interaction quality, testing, build tooling, and browser behavior.

#### ML/AI

Emphasize data integrity, leakage prevention, baselines, reproducibility, evaluation design, error analysis, inference behavior, experiment tracking, and whether core methods are understood rather than merely called.

#### Data engineering

Emphasize schemas, lineage, idempotency, orchestration, data quality, incremental processing, cost, failure recovery, and observability.

#### DevOps/SRE/Platform

Emphasize infrastructure as code, deployment safety, rollback, monitoring, alert quality, permissions, secrets, capacity, resilience, and operational cost.

#### Systems

Emphasize memory and resource safety, concurrency, performance measurement, platform behavior, low-level correctness, testing strategy, and interface design.

#### Security

Emphasize threat modeling, secure defaults, input validation, dependency risk, secrets handling, vulnerability response, disclosure practices, and avoidance of unsupported security claims.

#### Developer tools

Emphasize ergonomics, diagnostics, compatibility, extension points, documentation, packaging, release discipline, and support for real workflows.

### Step 11: Score with evidence anchors

Use the detailed anchors in `references/rubric.md`.

Default weighted dimensions:

| Dimension | Weight |
|---|---:|
| Project ownership and delivery | 20 |
| Code quality and architecture | 20 |
| Problem solving and debugging | 15 |
| Testing, correctness, and reliability | 15 |
| Collaboration and code review | 10 |
| Maintenance and release discipline | 10 |
| Role relevance and technical depth | 10 |

Score each dimension from 0 to 5, then calculate:

`weighted_score = sum(dimension_score / 5 * dimension_weight)`

Round only after all dimensions are scored.

Do not calculate a total when more than three dimensions lack adequate evidence. In that case, provide a qualitative assessment only.

### Step 12: Assign an evidence confidence

Use:

- `High`: Multiple independent evidence types, direct code inspection, verified contribution scope, and little identity ambiguity.
- `Medium`: Some direct evidence but important areas remain sparse, inaccessible, or ambiguous.
- `Low`: Mostly profile-level signals, few inspectable contributions, unclear authorship, or substantial inaccessible work.

Confidence is not a measure of developer skill. It measures the quality of the assessment.

### Step 13: Map to a capability band

Use these labels only for public evidence, not employment seniority:

1. `Exploratory`: Learning artifacts, experiments, or narrow contributions dominate.
2. `Contributor`: Can complete scoped changes in existing projects.
3. `Independent builder`: Can design, implement, test, and ship meaningful projects or subsystems.
4. `System owner`: Demonstrates sustained ownership, architecture judgment, reliability, and cross-contributor responsibility.
5. `Maintainer / technical leader`: Demonstrates broad technical stewardship, high-quality reviews, releases, governance, and durable project influence.

Use cautious phrasing such as “public evidence is consistent with…” rather than “this person is…”.

## Evidence interpretation rules

### Strong evidence

- Major code authored and maintained over time.
- Substantial PRs merged into established projects.
- High-quality reviews of other contributors.
- Root-cause analysis plus regression tests.
- Release, compatibility, migration, or operational ownership.
- Repeated contribution to the same subsystem.
- Design discussions tied to implemented outcomes.

### Moderate evidence

- Well-structured personal projects with tests and releases.
- Repeated bug fixes in a collaborative repository.
- Useful issue triage and reproduction work.
- Consistent documentation tied to code understanding.
- CI, packaging, deployment, or benchmark improvements.

### Weak evidence

- Organization membership alone.
- Repository stars or follower count.
- Green contribution graph.
- Raw commit count.
- Large repository count.
- Attractive screenshots or README alone.
- Technology buzzwords without inspectable implementation.
- Unmerged PRs without evidence that rejection was unrelated to quality.

## Common traps

- A transferred repository may make ownership unclear.
- A squash merge may hide individual commits.
- A monorepo can make contribution graphs misleading.
- Generated code, vendored dependencies, lockfiles, and formatting changes inflate diffs.
- A popular project may reward timing and distribution more than engineering depth.
- A low-public-activity account may reflect private employment work.
- A highly active account may contain automated commits.
- A rejected PR may still demonstrate strong engineering; inspect the discussion.
- A merged PR may be trivial; inspect the diff.
- Do not infer use of AI-generated code unless it is disclosed or directly evidenced.

## Output requirements

Use `references/report-template.md`.

Every report must include:

1. Scope and target role.
2. One-paragraph executive assessment.
3. Confidence level and why.
4. Evidence-backed scorecard or qualitative rubric.
5. Representative project analysis.
6. Organization contribution analysis.
7. Collaboration and review evidence.
8. Strongest demonstrated capabilities.
9. Risks, gaps, and unknowns.
10. Interview or verification questions derived from observed evidence.
11. Explicit limitations.

When comparing accounts:

- Apply the same role, time window, depth, and rubric.
- Compare evidence quality as well as scores.
- Avoid false precision when confidence differs.
- Explain where one account has stronger public evidence but not necessarily stronger overall ability.

## Final quality check

Before returning the assessment, verify:

- Every major conclusion has concrete evidence.
- Organization membership was not mistaken for contribution.
- Forks, mirrors, generated code, and imports were identified.
- At least one core code path and one test path were inspected when available.
- Collaboration evidence was considered, not just personal repositories.
- Role relevance was applied.
- Unknowns are clearly separated from weaknesses.
- Confidence reflects evidence quality.
- The conclusion says “publicly demonstrated capability,” not total personal ability.
