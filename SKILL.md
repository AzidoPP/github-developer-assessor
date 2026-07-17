---
name: github-developer-assessor
description: Evidence-first, role-aware assessment of engineering capability, technical stewardship, open-source impact, and development trajectory from a public GitHub account. Use when evaluating or comparing developers, reviewing open-source experience, calibrating hiring evidence, or preparing technical interview questions. Separates criterion-referenced engineering ability from relative rank, ecosystem influence, technology scarcity, popularity, and evidence confidence.
---

# GitHub Developer Assessor

## Purpose

Assess what a developer has **publicly demonstrated** on GitHub. Produce a
traceable profile based on code, contribution history, reviews, releases,
maintenance, adoption, and governance evidence.

Treat engineering capability as a criterion-referenced measure: the same
evidence should receive the same capability score regardless of who else is in
the comparison set. Report cohort rank, ecosystem impact, trajectory, scarcity,
and confidence separately.

This skill does not measure a person's complete ability or market value.
Private work, offline engineering, inaccessible organizations, and unlinked
identities may be absent.

## Inputs

Required:

- `github_account`: GitHub username or profile URL.

Optional:

- `target_role`: backend, frontend, mobile, ML/AI, data, DevOps/SRE,
  systems, security, developer tools, embedded, hardware, or another role.
- `expected_level`: internship, junior, mid-level, senior, staff, or another
  comparison target. Treat it as a target, not a conclusion.
- `depth`: `quick`, `standard`, or `deep`. Default: `standard`.
- `time_window`: Default: the most recent 24 months. Retain older evidence for
  durable ownership, maintenance, and impact.
- `comparison_accounts`: Accounts to assess using identical scope and weights.
- `assessment_profile`: `general`, `senior-ic`, `staff`, `maintainer`,
  `high-potential`, or `open-source-impact`. Default: `general`.
- `known_context`: Candidate-provided aliases, project descriptions, resume
  claims, or repository links. Label these as supplied context until verified.
- `include_scarcity`: Whether to estimate a cohort-relative technology scarcity
  index. Default: false unless the user asks about rarity or market value.

## Required references

Read the references that apply before scoring:

- Always read `references/rubric.md` and `references/report-template.md`.
- Read `references/impact-and-scarcity.md` for standard/deep assessments,
  comparisons, impact claims, scarcity, or market-value questions.
- Read `references/calibration.md` for comparisons, capability bands,
  representative anchors, percentiles, or a composite score.
- Read `references/evidence-schema.md` when producing machine-readable output,
  collecting a benchmark dataset, or automating evidence classification.

## Non-negotiable rules

1. Use public evidence only. Do not access private repositories, hidden
   endpoints, leaked credentials, or non-public data.
2. Separate engineering capability (E), stewardship (S), ecosystem impact (I),
   trajectory (T), optional scarcity (R), and evidence confidence (C).
3. Never call a role-conditioned composite score an absolute engineering score.
4. Keep engineering scores criterion-referenced. Comparison-set composition may
   change a percentile, but must not change the underlying E or S score.
5. Separate attention, adoption, authority, and technical leverage. Stars and
   followers are attention signals, not direct evidence of capability.
6. Separate membership, activity, contribution, ownership, and leadership.
   Organization membership alone is context, not technical evidence.
7. Attribute project impact to the person's verified role and contribution.
   Never transfer an entire famous project's influence to a minor contributor.
8. Distinguish original work from forks, mirrors, generated code, tutorial
   copies, dependency vendoring, repository imports, and mass formatting.
9. Separate implementation authorship, decision authorship, verification, and
   operational accountability when AI agents or bots are disclosed.
10. Do not reduce all AI-assisted work to zero credit. Lower only the dimensions
    whose authorship is ambiguous; score verified specification, architecture,
    review, testing, and maintenance responsibility where evidenced.
11. Treat technology difficulty, scarcity, demand, and value as different
    constructs. Rarity alone does not increase engineering capability.
12. Do not infer market value without external demand, location, and role data.
    Report it as unknown when those inputs are absent.
13. Cite every material conclusion with a repository, file, commit, PR, issue,
    review, release, dependency, registry, or discussion URL when possible.
14. Mark missing or inaccessible evidence as unknown. Absence of public evidence
    is not evidence of weak ability.
15. Report confidence separately. Do not publish a precise composite when
    identity, attribution, or more than two required axes are inadequately
    evidenced.

## Assessment modes

### Quick

- Inspect the profile, visible organizations, and contribution surface.
- Select up to 3 representative repositories.
- Inspect at least 2 meaningful PRs, reviews, issues, or releases when available.
- Sample a core code path, a correctness path, and project automation.
- Score E and S when evidence permits; summarize I and T qualitatively.

### Standard

- Select 3–5 representative repositories across personal, organization,
  external, and long-lived contexts.
- Inspect code, tests, CI, commits, PRs, reviews, issues, releases, maintenance,
  and adoption evidence.
- Verify actual contribution and automation attribution.
- Score E, S, I, and T independently.
- Produce role fit, capability band, confidence, and interview probes.

### Deep

- Trace major features from issue or design discussion through implementation,
  review, release, and follow-up.
- Compare earlier and later code to evaluate evolution.
- Inspect compatibility, performance, security, governance, and operational
  evidence where relevant.
- Evaluate impact attribution and cohort normalization.
- Include conflicting evidence, sensitivity analysis, and alternative readings.

## Workflow

### 1. Normalize scope

Record the canonical account, target role, expected level, assessment profile,
depth, time window, assessment date, and requested comparison cohort.

If the account is inaccessible or identity is materially ambiguous, stop or
limit the report and explain why.

### 2. Build an evidence ledger

Collect candidate evidence from:

- pinned and recently active non-fork repositories;
- long-lived projects and release history;
- organization repositories with verified contributions;
- external PRs and reviews;
- issues, discussions, triage, and user support;
- package registries, dependency graphs, extension stores, or official adoption;
- governance files, maintainer lists, release permissions, RFCs, or standards.

Classify repositories as:

- `personal-original`
- `organization-contribution`
- `external-contribution`
- `fork-or-mirror`
- `tutorial-or-experiment`
- `generated-or-vendored`
- `uncertain`

Use `references/evidence-schema.md` for structured records.

### 3. Verify contribution and attribution

For every representative project determine:

- creation, transfer, or import status;
- contribution scope and time span;
- affected core logic, tests, docs, CI, releases, or superficial files;
- authored PRs, reviews, issue handling, releases, and governance activity;
- squash, rebase, co-author, bot, or agent effects on attribution;
- implementation, decision, verification, and accountability roles.

Use raw counts only to navigate. Inspect actual diffs and discussion.

### 4. Select representative projects

Prefer evidence quality over popularity. Cover when available:

- end-to-end ownership;
- collaborative or organization work;
- external contribution to an established project;
- long-lived maintenance;
- role-specific technical depth;
- ecosystem or knowledge impact.

Do not discard a small or hardware project because it lacks enterprise-scale
infrastructure. Evaluate it against its real constraints.

### 5. Sample code and correctness deliberately

Inspect:

- public API or entry point;
- core domain, algorithm, or hardware-control path;
- data or state model;
- error, resource, concurrency, or recovery path;
- tests for core behavior and edge cases;
- build, CI, deployment, packaging, or release configuration;
- at least one meaningful recent diff.

Evaluate constraint complexity such as correctness, performance, concurrency,
compatibility, platform, physical, operational, and collaboration constraints.
Reward demonstrated handling of difficult constraints, not rarity by itself.

### 6. Inspect problem solving and review behavior

Look for reproduction, root-cause reasoning, trade-offs, regression tests,
review response, scope control, follow-through, and prevention mechanisms.

For reviews, distinguish correctness, compatibility, performance, security, and
maintainability reasoning from approvals or stylistic comments.

### 7. Inspect stewardship

Check releases, migrations, deprecations, dependency maintenance, issue response,
rollback or recovery, contributor enablement, review responsibility, governance,
and long-term technical debt.

### 8. Inspect impact and trajectory

Follow `references/impact-and-scarcity.md`.

- Attribute adoption and influence to verified responsibility.
- Use attention metrics only as corroborating signals.
- Give open or unmerged work partial trajectory evidence based on review stage;
  do not count it as realized ecosystem impact.
- Compare 6-, 12-, and 24-month windows when estimating trajectory.

### 9. Apply the role lens

Use role-specific concerns when sampling and weighting evidence:

- Backend: APIs, data, transactions, concurrency, failures, observability,
  migrations, deployment.
- Frontend: components, state, accessibility, browser behavior, performance,
  testing, build tooling.
- ML/AI: data integrity, evaluation, reproducibility, inference, error analysis,
  experiment tracking, systems cost.
- Data: schemas, lineage, idempotency, orchestration, quality, recovery, cost.
- DevOps/SRE: infrastructure, rollout, rollback, permissions, monitoring,
  resilience, capacity, cost.
- Systems/compiler: memory, lifetime, concurrency, ABI, performance,
  platform behavior, diagnostics, correctness.
- Security: threat model, secure defaults, validation, secrets, vulnerability
  response, disclosure.
- Developer tools: ergonomics, diagnostics, compatibility, extension points,
  packaging, documentation, workflows.
- Embedded/hardware: timing, memory, power, buses, toolchains, physical testing,
  measurement, safety, hardware revisions, and hardware-in-the-loop evidence.

### 10. Score the independent axes

Use `references/rubric.md`:

- E — criterion-referenced engineering capability, 0–100.
- S — technical stewardship and ownership, 0–100.
- I — attributable ecosystem impact, 0–100 or unknown.
- T — development trajectory, 0–100 or unknown.
- R — optional cohort-relative scarcity, 0–100 or unknown.
- C — confidence by evidence coverage, attribution, sampling, and identity.

Do not average unknown values into zero.

### 11. Calibrate and optionally compose

Follow `references/calibration.md`.

- Assign a capability band using E/S gates, not composite score alone.
- Compare against role-specific, versioned anchor packets only after completing
  an independent first-pass score.
- Report cohort percentile only when the cohort is defined and sufficiently
  sampled.
- Calculate a role-conditioned composite only when requested or useful, name the
  profile and weights, and keep the independent axes visible.

### 12. Produce the report

Use `references/report-template.md`. Include:

1. scope and assessment profile;
2. executive assessment;
3. E/S/I/T axes and optional R;
4. confidence and unknowns;
5. representative project evidence;
6. organization and external contributions;
7. impact and attribution analysis;
8. strengths, risks, and contradictions;
9. role fit and optional percentile;
10. evidence-derived interview questions;
11. limitations.

## Final quality check

Before returning an assessment, verify:

- Engineering capability did not change merely because the comparison set did.
- Popularity did not leak into E or S.
- Project fame was not inherited without contribution attribution.
- Difficulty was separated from scarcity and market demand.
- AI-assisted work was decomposed by authorship and accountability.
- Hardware and niche projects were evaluated against appropriate constraints.
- Open PRs affected trajectory, not realized impact, unless adopted elsewhere.
- Representative anchors were applied only after independent scoring.
- Every major claim has evidence or is marked unknown.
- Confidence reflects evidence quality rather than developer quality.
