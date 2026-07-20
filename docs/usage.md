# Usage and Runtime Notes

This is the operator-facing guide for running GitHub Developer Assessor.
Normative assessment rules remain in [SKILL.md](../SKILL.md), and scoring
definitions remain in the linked methodology references.

## Minimum input and defaults

Only `github_account`, as a username or profile URL, is required. Defaults are:

- role lens: general engineering;
- expected level: no preset target;
- depth: `standard`;
- time window: the most recent 24 months, while retaining older evidence for
  durable ownership, maintenance, and impact;
- assessment profile: `general`;
- cohort and scarcity: not assessed unless they can be defined credibly.

Optional inputs include a target role, expected level, depth, time window,
comparison accounts, assessment profile, known context, and a named cohort.
Private access additionally requires current-session authorization and an
explicit repository selection.

## Choose an assessment depth

| Depth | Best used for | Evidence scope |
|---|---|---|
| `quick` | Orientation or deciding where deeper inspection is worthwhile | An unscored Quick Evidence Scan: verified facts, evidence map, attribution clarity, unknowns, and recommended next inspection |
| `standard` | A normal GitHub behavior and responsibility assessment | Multiple repositories plus PR/issue discussion, subject-authored reviews, CI outcomes, maintenance, release, governance, adoption, and trajectory; no evaluator-side source or diff inspection |
| `deep` | Source-level engineering review, high-stakes decisions, difficult attribution, or close comparisons | Standard evidence plus targeted source/diff/test inspection, feature life cycles, historical evolution, contradictions, and sensitivity analysis |

The exact sampling requirements for each mode are defined in
[Assessment modes](../SKILL.md#assessment-modes).

`quick` does not publish numeric axes, a capability band, or a profile score.
In `standard`, Implementation quality is `not_assessed`, so E is an interval or
`unknown`, never a point. Use `deep` for code quality, source-level correctness,
or implementation-quality conclusions.

## Prompt examples

> Assess `https://github.com/example` using the defaults.

> Run a quick evidence scan for `example`. Identify the strongest attributable
> artifacts and recommend whether standard or deep assessment is worthwhile.

> Assess `example` for a senior backend role. Use standard depth, focus on the
> last 24 months, inspect organization contributions, and cite the strongest
> evidence.

> Assess `example` at deep depth for backend code quality. Create targeted
> source review packets and keep unsampled code outside the conclusion.

> Compare A and B for an open-source maintainer role at deep depth. Use the same
> snapshot, evidence window, and source-inspection protocol, report E/S/I/T
> separately, then apply the maintainer profile and test whether the ordering is
> stable.

> Assess an embedded developer’s absolute capability separately from the
> scarcity of their verified hardware and firmware skill combination.

> Assess `example` and include private repositories. I will provide a GitHub
> token; first list the private repositories I can choose from.

## Evidence access

### Public evidence

Public-only assessment is the default and requires no token. In `quick` and
`standard`, the agent may browse commit and PR metadata, PR descriptions and
discussion, subject-authored reviews, issues, RFCs, CI outcomes, releases,
governance, and downstream evidence, but it must not inspect source files or
diff contents or run project checks. `deep` additionally inspects targeted code,
diffs, tests, and history under the dedicated source-inspection protocol.
GitHub API or CLI access improves coverage, but the assessment remains usable
without it; confidence may be lower.

### Selected private repositories

A user may supply a GitHub token in the current conversation. If repository
names are included in the same request, those names are the authorized
selection. Otherwise, the skill lists accessible private repositories and
waits for the user to choose before inspecting any private contents.

Only selected repositories enter the evidence boundary. Every private artifact
must retain a stable repository, commit, pull request, issue, release, or
evidence identifier and be marked private. The token itself must never appear
in a report, command shown to the user, saved artifact, dataset, or calibration
packet. See the full [private repository workflow](../SKILL.md#optional-private-repository-workflow).
The same mode boundary applies to private repositories: `quick` and `standard`
may inspect authorized discussion and lifecycle records but not private source
or diffs.

## Personally observed runtime

The following is one user’s end-to-end observation for this workflow, recorded
on 2026-07-19:

| Surface | Evidence access | Reasoning effort | Observed elapsed time |
|---|---|---|---|
| ChatGPT on the web | Official GitHub connector | `xhigh` | 15–20 minutes |
| Codex desktop | Clone or pull the Git repository with commands, then inspect it locally | `max` | 20–30 minutes |

These figures are personal observations, not controlled benchmarks or a fixed
SLA. Repository count, history size, cache state, network conditions, evidence
depth, and model or tool configuration can materially change elapsed time.
They predate the current source-inspection mode boundary and are not mode-
specific Quick, Standard, or Deep benchmarks.
Because the two access paths and reasoning settings differ, the table should
not be read as a direct product-speed comparison. A Deep local inspection can
include more repository history, code paths, tests, and configuration than a
connector run, while connector access avoids local clone and indexing startup.
