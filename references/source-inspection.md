# Deep Source Inspection Protocol

Use this protocol only for a `deep` assessment. It governs evaluator-side
inspection of source files, diffs, tests, build configuration, and local checks.
A subject's own review comments remain review evidence and may be inspected in
`quick` or `standard` mode without performing source inspection.
Treat code fragments quoted inside those discussions as discussion context, not
as inspected implementation evidence.

## Mode boundary

- Do not inspect source files, diff contents, or test implementation in `quick`
  or `standard` mode.
- Do not run builds, tests, linters, static analysis, or benchmarks in `quick`
  or `standard` mode.
- When a request asks for code quality, source-level correctness, or
  implementation quality without naming a depth, select `deep`.
- When the user explicitly requests `standard`, preserve that boundary and mark
  source-dependent claims `not_assessed`; do not silently upgrade the mode.
- Treat every source inspection as targeted sampling, never as proof of whole-
  repository or production quality.

## Source review packet

Create one packet for each independently inspected change or code path. Record:

- packet ID and stable repository, commit, or PR reference;
- base and head revisions when inspecting a change;
- role lens, language, project type, and relevant constraints;
- subject attribution for implementation, decision, verification, and
  accountability;
- inspected source, error, resource, concurrency, recovery, and test paths;
- before-and-after observations when history is available;
- checks attempted, exact commands when local execution is used, and results;
- review, CI, release, regression, rollback, or downstream follow-up;
- supported E subdimensions and the precise claim each artifact supports;
- contradictory evidence, unavailable context, and confidence.

## Inspection procedure

1. Select one to three high-information changes tied to verified subject
   attribution. Prefer a feature or fix with discussion, validation, and a
   visible outcome over an isolated code snapshot.
2. Establish the local project conventions and the constraint being solved
   before judging the implementation.
3. Inspect the relevant before-and-after diff, current core path, failure path,
   tests, and build or release configuration. Stay within the selected artifact
   rather than expanding into a repository-wide review without a reason.
4. Run existing targeted checks only when a local checkout is available, the
   commands are safe and proportionate, and no external state change is needed.
   Record failures as observations; do not repair the project during an
   assessment unless the user separately requests a fix.
5. Inspect review and lifecycle evidence for rejected alternatives, regression
   prevention, release consequences, and later corrections.
6. Map observations to the unchanged E anchors in `rubric.md`. Keep observation,
   attribution, inference, score, and confidence separate.

## Claim limits

- Require direct source or diff inspection before scoring Implementation
  quality.
- Do not treat a passing CI run, test count, coverage percentage, linter result,
  or static metric as code-quality proof by itself.
- Use complexity, dependency, churn, and code-size metrics only to navigate or
  corroborate a contextual observation; never convert them directly to anchor
  points.
- Do not infer production reliability from repository tests alone. Separate
  implementation correctness, verification discipline, and observed outcomes.
- Apply the normal single-artifact cap and repeated-evidence requirements. One
  source review packet does not establish stable whole-person quality.
- Reduce only the attribution components made ambiguous by generated or
  AI-assisted implementation. Preserve separately evidenced decisions,
  verification, and accountability.
- Mark a source-dependent subdimension `unknown` when inspection was attempted
  but remained insufficient. Use `not_assessed` only when the mode intentionally
  excluded source inspection.
