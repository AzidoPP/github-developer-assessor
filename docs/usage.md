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
| `quick` | Orientation or deciding where deeper inspection is worthwhile | A small representative sample with qualitative I/T when needed |
| `standard` | A normal single-account assessment | Multiple representative repositories plus code, review, maintenance, release, and adoption evidence |
| `deep` | High-stakes review, difficult attribution, or close comparisons | Feature life cycles, historical evolution, contradictions, and sensitivity analysis |

The exact sampling requirements for each mode are defined in
[Assessment modes](../SKILL.md#assessment-modes).

## Prompt examples

> Assess `https://github.com/example` using the defaults.

> Assess `example` for a senior backend role. Use standard depth, focus on the
> last 24 months, inspect organization contributions, and cite the strongest
> evidence.

> Compare A and B for an open-source maintainer role. Use the same snapshot and
> evidence window, report E/S/I/T separately, then apply the maintainer profile
> and test whether the ordering is stable.

> Assess an embedded developer’s absolute capability separately from the
> scarcity of their verified hardware and firmware skill combination.

> Assess `example` and include private repositories. I will provide a GitHub
> token; first list the private repositories I can choose from.

## Evidence access

### Public evidence

Public-only assessment is the default and requires no token. The agent works
best when it can browse GitHub, search commits, issues, pull requests, reviews,
and releases, and inspect code and diffs. GitHub API or CLI access improves
coverage, but the assessment remains usable without it; confidence may be
lower.

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
Because the two access paths and reasoning settings differ, the table should
not be read as a direct product-speed comparison. Local inspection can include
more repository history, code paths, tests, and configuration than a connector
run, while connector access avoids local clone and indexing startup.
