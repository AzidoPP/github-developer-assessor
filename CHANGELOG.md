# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

### Added

- Separate engineering capability (E), stewardship (S), ecosystem impact (I), development trajectory (T), technology scarcity (R), and confidence (C) axes.
- Attributable-impact model that distinguishes attention, adoption, authority, technical leverage, community leverage, and knowledge diffusion.
- Project attribution ranges, diminishing returns, ecosystem normalization, and anti-double-counting rules.
- Capability-band gates, high-depth specialist handling, role-conditioned profile scores, cohort comparison rules, and rank-sensitivity checks.
- Versioned calibration-packet protocol and an initial registry of candidate—not yet normative—representative accounts from the pilot assessments.
- Machine-readable evidence and assessment schemas designed for weak supervision, pairwise labeling, active learning, and axis-specific models.
- Explicit attribution guidance for AI- or bot-assisted implementation.
- Domain-fair validation guidance for embedded, hardware, systems, compiler, application, library, and educational work.

### Changed

- Replaced the 1.x single weighted total with a multi-axis v2 report. Earlier totals remain readable but are not directly comparable with v2 axes or profile scores.
- Made impact a scored, attributable construct instead of treating all popularity signals only as navigation hints.
- Made technology scarcity optional and cohort-relative, separate from engineering difficulty, demand, compensation, and market value.
- Expanded the report template to expose dimension evidence, attribution, confidence components, unknowns, profile weights, and comparison stability.

### Fixed

- Prevented high-impact maintainers, educators, and fast-growing contributors from being systematically understated by a capability-only total.
- Prevented famous projects, organization membership, and raw attention from automatically inflating engineering scores.

## 1.0.0 - 2026-07-17

### Added

- Evidence-first workflow for assessing publicly demonstrated engineering capability from a GitHub account.
- Quick, standard, and deep assessment modes.
- Role-specific evaluation lenses and a weighted scoring model.
- Detailed scoring anchors in `references/rubric.md`.
- Reusable assessment structure in `references/report-template.md`.
- Guidance for organization contributions, code review, maintenance, confidence, uncertainty, and ethical limits.
- Project documentation, contribution guidance, and MIT licensing.
