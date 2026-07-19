# GitHub Developer Assessor

An evidence-first Agent Skill for assessing what a GitHub account demonstrates:
engineering capability, stewardship, attributable ecosystem impact, development
trajectory, and—when a credible cohort exists—technology scarcity.

[Evidence Lab](https://minsecrus.github.io/github-developer-assessor/) ·
[Usage and runtime notes](docs/usage.md) · [Assessment workflow](SKILL.md)

## What it reports

| Axis | Meaning | Reference frame |
|---|---|---|
| E — Engineering capability | Implementation, architecture, debugging, reliability, and constraint depth | Criterion-referenced |
| S — Stewardship and ownership | Delivery, maintenance, review, releases, governance, and contributor leverage | Criterion-referenced |
| I — Ecosystem impact | Attributable adoption, authority, downstream leverage, community leverage, and knowledge diffusion | Ecosystem-normalized |
| T — Development trajectory | Recent growth in difficulty, validation, follow-through, and scope | Compared with the subject’s earlier evidence |
| R — Technology scarcity | Supply, entry barriers, cross-domain coupling, failure cost, and substitutability | Optional, cohort-relative, and time-sensitive |
| C — Confidence | Coverage, attribution, sampling stability, and identity certainty | Evidence quality |

The axes remain visible. A role-conditioned profile score may support a specific
selection question, but it is never presented as an absolute engineering score,
and scarcity is never added to capability.

## Quick start

Only a GitHub username or profile URL is required. Unless the request says
otherwise, the skill uses a general-engineering lens, standard depth, the most
recent 24 months, no preset expected level, and no scarcity estimate.

> Assess `https://github.com/example` using the defaults.

> Assess `example` for a senior backend role. Focus on the last 24 months,
> inspect organization contributions, and cite the strongest evidence.

> Compare A and B for an open-source maintainer role using the same snapshot,
> evidence boundary, and scoring profile.

See [Usage and Runtime Notes](docs/usage.md) for every input, more prompt
examples, public and selected-private evidence workflows, tool requirements,
and personally observed runtime.

## Evidence boundaries

- Public evidence is the default. Private repositories enter an assessment only
  when the user authorizes access and explicitly selects them.
- Observations, attribution, inference, and scores remain separate and
  traceable to inspectable artifacts.
- Stars, followers, raw activity, organization membership, and project fame are
  navigation or context signals—not direct proof of capability.
- Missing or inaccessible evidence is `unknown`, not zero.
- AI or bot assistance changes attribution; it does not automatically erase
  evidenced specification, decisions, verification, or accountability.
- Technology scarcity is optional and cohort-relative. It is not capability,
  market demand, compensation, or personal value.

The executable procedure and hard rules live in [SKILL.md](SKILL.md). Detailed
anchors, completeness rules, calibration, and output structure live in the
references below.

## Documentation

- [Usage and Runtime Notes](docs/usage.md) — inputs, examples, access
  paths, tool requirements, and personal timing observations.
- [Assessment workflow](SKILL.md) — complete procedure and non-negotiable rules.
- [Multi-Axis Assessment Rubric](references/rubric.md) — E/S/I/T/R dimensions,
  weights, completeness rules, and behavioral anchors.
- [Impact, Attribution, and Scarcity](references/impact-and-scarcity.md) — impact
  normalization, AI and project attribution, and scarcity safeguards.
- [Calibration, Bands, and Comparison Protocol](references/calibration.md) —
  capability bands, profile weights, cohort comparisons, and sensitivity tests.
- [Provisional Candidate Anchor Packets](references/candidate-anchor-packets.md)
  — evidence-linked candidate packets pending independent activation review.
- [Evidence Schema and Learning-Ready Data](references/evidence-schema.md) —
  machine-readable records and assisted-labeling guidance.
- [Report Template](references/report-template.md) — reusable multi-axis output
  structure.
- [Contributing](CONTRIBUTING.md) — contribution and validation guidance.
- [Changelog](CHANGELOG.md) — release history and migration notes.

## Limits and privacy

The assessor describes demonstrated evidence within a stated boundary; it does
not measure a person’s complete ability or infer protected personal traits.
Unselected private work, offline engineering, inaccessible organizations, and
unlinked identities may be absent.

Tokens must not be reproduced in reports, commands shown to the user, saved
files, datasets, or calibration packets. Private visibility neither raises nor
lowers the technical strength of an artifact.

## License

MIT License. Copyright (c) 2026 Minsecrus. See [LICENSE](LICENSE).
