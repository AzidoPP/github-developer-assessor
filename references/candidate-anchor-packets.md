# Provisional Candidate Anchor Packets

Use this reference only when applying or auditing a named candidate anchor from
`calibration.md`.

## Status and scoring boundary

- Rubric: GitHub Developer Assessor v2, unreleased snapshot.
- Evidence snapshot: 2026-07-18.
- Default recent window: 2024-07-18 through 2026-07-18; older public evidence
  is used only for durability and trajectory baselines.
- Boundary: public GitHub evidence plus explicitly linked public package
  registries, project sites, course pages, and library catalogs. Profile
  followers, stars, forks, and views are attention signals, not engineering or
  adoption evidence by themselves.
- Source-inspection boundary: targeted public source, diff, test, and build
  evidence was used where cited. Treat these as Deep-compatible legacy packets,
  not exact Standard E comparators, until a second reviewer records the current
  source-inspection metadata.
- Status: provisional candidate packets. They have not completed the formal
  independent activation review below and are not normative anchors.
- Calculation: scored axes have `known_weight = 100`. Displayed scores are
  rounded whole-number results from the listed whole or half anchors. Low
  confidence still overrides numerical completeness: candidate R values marked
  `unknown` retain their mechanical results only as diagnostic hypotheses.
- R warning: every R value uses its own named role cohort. It describes scarcity
  within that cohort, not capability, market demand, compensation, or a
  cross-row ranking.

The compact notation follows the rubric order:

- E: implementation, architecture, problem solving, reliability, constraints.
- S: ownership, maintenance, collaboration, governance.
- I: adoption, downstream leverage, authority, community, knowledge, durability.
- T: difficulty progression, external validation, learning, scope expansion.
- R: supply, barriers, cross-domain coupling, failure cost, substitution.

## Scorecard

| Candidate | E anchors | E | S anchors | S | I anchors | I | T anchors | T | R anchors | R | Confidence |
|---|---|---:|---|---:|---|---:|---|---:|---|---:|---|
| `torvalds` | 5 / 5 / 5 / 4.5 / 5 | 98 | 5 / 5 / 4.5 / 5 | 98 | 4.5 / 5 / 5 / 4.5 / 4 / 5 | 94 | 2.5 / 5 / 4 / 2.5 | 70 | 4.5 / 4 / 5 / 4.5 / 4.5 | 90 | High |
| `gaogaotiantian` | 4.5 / 4.5 / 4.5 / 4 / 5 | 90 | 4.5 / 4.5 / 5 / 4.5 | 93 | 4.5 / 4.5 / 5 / 4 / 3.5 / 4.5 | 89 | 4.5 / 5 / 4.5 / 5 | 95 | 4.5 / 4 / 5 / 4 / 4.5 | 88 | High |
| `mattpocock` | 4 / 4 / 4 / 3.5 / 4 | 78 | 4.5 / 4 / 4 / 4 | 83 | 4.5 / 4.5 / 4 / 4 / 5 / 4 | 87 | 4 / 4 / 4.5 / 4.5 | 85 | 3.5 / 3 / 3.5 / 2.5 / 3 | 63 | Medium |
| `lvy010` | 3.5 / 4 / 3.5 / 3.5 / 4 | 74 | 3.5 / 2.5 / 3 / 1 | 53 | 2.5 / 3 / 2 / 1.5 / 1.5 / 1.5 | 44 | 4 / 4 / 4 / 4 | 80 | 3.5 / 3.5 / 4 / 3 / 3.5 | unknown (70 diagnostic) | Medium |
| `liyupi` | 3 / 3 / 2.5 / 2 / 3 | 54 | 4 / 3 / 2.5 / 3.5 | 66 | 3 / 3 / 3 / 2.5 / 3.5 / 3.5 | 60 | 3.5 / 2.5 / 2.5 / 3.5 | 60 | 4 / 2.5 / 3.5 / 2 / 3 | 61 | Medium |
| `Sunrisepeak` | 3.5 / 4 / 4 / 3.5 / 4.5 | 78 | 4 / 4 / 4 / 3.5 | 78 | 3 / 3 / 3.5 / 3 / 4 / 3 | 64 | 4 / 3.5 / 4 / 4 | 78 | 3.5 / 3.5 / 4 / 3 / 3 | unknown (69 diagnostic) | Medium |
| `sheepbox8646` | 3.5 / 4 / 4 / 3 / 4 | 74 | 4 / 4 / 3 / 3.5 | 73 | 3.5 / 3.5 / 3.5 / 4 / 2.5 / 2.5 | 69 | 4 / 3 / 3.5 / 4 | 73 | 3.5 / 3.5 / 4 / 3.5 / 3 | unknown (71 diagnostic) | Medium |
| `bagder` | 4.5 / 5 / 5 / 4.5 / 5 | 96 | 5 / 5 / 4.5 / 5 | 98 | 4.5 / 5 / 5 / 4.5 / 5 / 5 | 96 | 2.5 / 5 / 4 / 2.5 | 70 | 4.5 / 4 / 5 / 4.5 / 4.5 | 90 | High |
| `BurntSushi` | 4.5 / 5 / 4.5 / 4.5 / 5 | 94 | 5 / 4.5 / 4 / 3.5 | 87 | 5 / 5 / 4.5 / 3.5 / 4.5 / 5 | 93 | 4 / 4.5 / 5 / 4 | 88 | 4.5 / 4 / 4.5 / 3 / 4.5 | 82 | High |
| `FiloSottile` | 5 / 5 / 4 / 5 / 5 | 96 | 5 / 5 / 4.5 / 4 | 94 | 4.5 / 5 / 5 / 4.5 / 4 / 5 | 94 | 4.5 / 5 / 5 / 4.5 | 95 | 4.5 / 4.5 / 5 / 5 / 4 | 93 | High |
| `yyx990803` | 4.5 / 5 / 4.5 / 4.5 / 4.5 | 93 | 5 / 5 / 4 / 4.5 | 93 | 5 / 5 / 5 / 4.5 / 4 / 5 | 97 | 4 / 4 / 4.5 / 4.5 | 85 | 4.5 / 4 / 4.5 / 3 / 4.5 | 82 | High |
| `mitchellh` | 4.5 / 4.5 / 5 / 4.5 / 5 | 94 | 5 / 4.5 / 4 / 4.5 | 91 | 4.5 / 5 / 5 / 4 / 4 / 5 | 92 | 5 / 4.5 / 4 / 5 | 93 | 4.5 / 4.5 / 5 / 4.5 / 4 | 91 | High |
| `simonw` | 4 / 4.5 / 4.5 / 4 / 4 | 85 | 5 / 5 / 3.5 / 4 | 89 | 4.5 / 4.5 / 4.5 / 4 / 4.5 / 4.5 | 89 | 4 / 3.5 / 5 / 5 | 87 | 3.5 / 3 / 4 / 3 / 3.5 | unknown (68 diagnostic) | Medium |

The rows from `bagder` through `simonw` are the first external calibration
batch. They were scored against the rubric before being compared with the
earlier pilot rows; table order is not a ranking and this is not the separate
activation review required below. The comparison pass is deliberately moderate:
it reserves more 5-level subdimensions for cross-context ceilings while keeping
these established maintainers above the earlier mid-range packets rather than
normalizing them toward the center.

## `torvalds`

- Role lens: general-purpose kernel integration and technical leadership.
- Capability interpretation: Maintainer / technical leader.
- R cohort: top-level mainline integration and release leaders with at least
  five years of public responsibility across architectures, core subsystems,
  maintainer chains, and stabilization for general-purpose open-source kernels.
  The comparison frame samples Linux, FreeBSD, and NetBSD governance and release
  records as of the snapshot date.

Representative evidence:

- [Linux repository](https://github.com/torvalds/linux), its
  [MAINTAINERS file](https://github.com/torvalds/linux/blob/master/MAINTAINERS),
  [official release record](https://www.kernel.org/releases.html), and the
  [documented integration process](https://docs.kernel.org/process/2.Process.html)
  jointly show repeated cross-subsystem integration, release responsibility,
  compatibility judgment, and a contributor institution that persists across
  major transitions.
- Recent directly attributable fixes cover refcount and concurrency lifecycles
  ([eventpoll](https://github.com/torvalds/linux/commit/8c2e52ebbe885c7eeaabd3b7ddcdc1246fc400d2)),
  RCU lifetime
  ([keyrings](https://github.com/torvalds/linux/commit/43a1e3744548e6fd85873e6fb43e293eb4010694)),
  and preventive error handling
  ([shadow stack](https://github.com/torvalds/linux/commit/52f657e34d7b21b47434d9d8b26fa7f6778b63a0)).
- Linux and Git supply foundational downstream leverage and durable dependence.
  Credit is assigned to verified creation, integration, and release roles, not
  inherited from project fame or the work of the wider contributor community.

Contradictions and blind spots:

- T is intentionally 70 rather than a ceiling score. The recent public window
  shows sustained apex-level responsibility and external reliance, but little
  difficulty or scope expansion relative to the subject's own earlier baseline.
  Recent hardware and audio experiments broaden the learning surface without
  yet becoming new shared-system responsibility.
- Much kernel review happens on mailing lists rather than GitHub. This packet
  samples the public mirror and maintainer artifacts and should be independently
  cross-checked against mailing-list evidence before activation.
- Linux implementation, testing, and adoption belong to a very large community.
  Reliability, adoption, and community leverage are therefore held at 4.5 where
  the individual attribution does not justify transferring the project's full
  outcome to one person.

## `gaogaotiantian`

- Role lens: Python runtime, debugger, profiling, and diagnostics maintainer.
- Capability interpretation: Maintainer / technical leader.
- R cohort: public maintainers who simultaneously hold CPython runtime or
  debugger interface and merge responsibility, Apache Spark Python/runtime or
  release-infrastructure committer-level review responsibility, and ownership
  of a cross-platform native profiler or debugger. The public sampling frame is
  the Python core-team/expert lists and the Spark/ASF committer lists; it is not
  a labor-market sample.

Representative evidence:

- [VizTracer](https://github.com/gaogaotiantian/viztracer) has a multi-year
  release history and native code with daily and wheel CI across Python 3.10–3.14,
  free-threading, Ubuntu, macOS Intel/ARM, and Windows/ARM
  ([CI](https://github.com/gaogaotiantian/viztracer/blob/master/.github/workflows/python-package.yml),
  [wheels](https://github.com/gaogaotiantian/viztracer/blob/master/.github/workflows/wheels.yml)).
  Public package telemetry recorded about 1.19 million VizTracer and 1.02
  million objprint downloads in the month preceding the snapshot
  ([VizTracer telemetry](https://pypistats.org/api/packages/viztracer/recent),
  [objprint telemetry](https://pypistats.org/api/packages/objprint/recent)).
- The subject is listed in the official
  [Python core-team log](https://devguide.python.org/core-team/team-log/) and as
  a [pdb expert](https://devguide.python.org/core-team/experts/index.html).
  [PEP 667](https://peps.python.org/pep-0667/) is Final and names the subject as
  co-author; its implementation
  ([CPython #115153](https://github.com/python/cpython/pull/115153)) went through
  extensive multi-reviewer iteration. Public search at the snapshot found about
  213 merged CPython PRs authored and 194 PRs reviewed by the subject.
- The subject is also an official
  [Apache Spark committer](https://spark.apache.org/committers.html). Public
  search found about 174 Spark PRs reviewed; representative infrastructure work
  addressed requested scope changes before approval and records no AI use
  ([Spark #57093](https://github.com/apache/spark/pull/57093)).

Contradictions and blind spots:

- Package download telemetry includes CI, mirrors, and repeat installation; it
  supports broad use only when combined with releases, issues, and downstream
  activity.
- PEP 667 required later ref-leak and crash corrections; broad project review
  does not transfer all CPython correctness to one individual. Personal package
  histories also remain strongly author-concentrated, limiting community
  leverage and bus-factor claims.
- T=95 reflects a public progression from personal diagnostics tools to CPython
  core/pdb authority and then Spark committer responsibility in two independent
  governance systems. It should not be read as a permanent rate: the most recent
  slices continue at a high baseline rather than adding a new role every period.
- The packet samples representative runtime and diagnostic work rather than
  every CPython or Spark interaction. R remains medium confidence; widening the
  cohort to any senior Python maintainer would lower it materially.

## `mattpocock`

- Role lens: TypeScript type-system tooling and technical education.
- Capability interpretation: Maintainer / technical leader.
- R cohort: global public-OSS maintainers who combine advanced TypeScript
  developer-tool ownership with a durable technical curriculum. The cohort is
  role-conditioned; ordinary TypeScript application developers are not the
  denominator. The provisional comparison frame includes Matt Pocock, Orta
  Therox, Joshua K. Goldberg, Anthony Fu, Tanner Linsley, David Khourshid, Kent
  C. Dodds, Sindre Sorhus, Wes Bos, and Kyle Simpson.

Representative evidence:

- [`@total-typescript/ts-reset`](https://github.com/mattpocock/ts-reset) has
  sustained releases, tests and external contributions. The public npm endpoint
  reported about 4.81 million downloads in the month preceding the snapshot
  ([telemetry](https://api.npmjs.org/downloads/point/last-month/%40total-typescript%2Fts-reset)).
- [Evalite](https://github.com/mattpocock/evalite) shows continued tool
  ownership and release work; public npm telemetry reported about 1.12 million
  downloads in the preceding month
  ([telemetry](https://api.npmjs.org/downloads/point/last-month/evalite)).
- External accepted work includes type-safety changes in
  [Vercel AI #7917](https://github.com/vercel/ai/pull/7917) and TypeScript
  configuration guidance in
  [Microsoft's TypeScript wiki #337](https://github.com/microsoft/TypeScript-wiki/pull/337).
- [Total TypeScript](https://www.totaltypescript.com/) and its public
  repositories supply durable knowledge-diffusion evidence distinct from raw
  repository attention.
- Public issue and test history shows root-cause and regression work for
  `ts-reset` filter typing
  ([issue](https://github.com/mattpocock/ts-reset/issues/233#issuecomment-4169025883),
  [test](https://github.com/mattpocock/ts-reset/blob/81b3b2614a32e47948cd4b8d5468879c07c2b361/src/tests/filter-boolean-issue-233.ts#L12-L88)),
  while [Evalite #159](https://github.com/mattpocock/evalite/pull/159) and
  [#351](https://github.com/mattpocock/evalite/pull/351) show interface judgment
  and external-contributor closure.

Contradictions and blind spots:

- Some recent repositories include agent-authored changes, especially the
  expansion into [Sandcastle](https://github.com/mattpocock/sandcastle) and
  [skills](https://github.com/mattpocock/skills). Tool ownership,
  specification, review and release evidence are credited separately from
  direct implementation.
- Current head verification is not uniformly green: recent `ts-reset` CI and
  publish runs failed
  ([CI](https://github.com/mattpocock/ts-reset/actions/runs/23851185599),
  [publish](https://github.com/mattpocock/ts-reset/actions/runs/23851185641)),
  and an Evalite main run also failed
  ([run](https://github.com/mattpocock/evalite/actions/runs/19240591698)).
  npm download counts include CI, mirrors and repeat installation.
- S=83 is the provisional registry point. A second review scored collaboration
  and governance more conservatively, producing S=77; activation requires
  resolving that 77–83 sensitivity rather than hiding it.
- TypeScript education is broadly accessible and failures generally have short,
  low-cost feedback cycles; those facts keep R well below the specialist's I.
  Course outcomes outside public artifacts remain unverified.

## `lvy010`

- Role lens: emerging systems, developer-tooling, and open-source contributor.
- Capability interpretation: Independent builder with high-depth contributor
  and high-trajectory modifiers. E crosses the System-owner numeric threshold,
  but S=53 and the qualitative lifecycle evidence do not meet that band.
- R cohort hypothesis: public-GitHub emerging systems/developer-tool upstream
  contributors with an account history no longer than three years, at least
  three non-trivial merged upstream PRs in 24 months, and work spanning Rust,
  C/C++, build or version-control systems, and embedded or edge inference.
  Because no credible sample size or supply distribution was established, R is
  formally `unknown`; 70 is only the mechanical diagnostic vector.

Representative evidence:

- [gitmono-dev/mega #1796](https://github.com/gitmono-dev/mega/pull/1796)
  delivered a 15-commit target/build schema, migration, scheduler, worker-state,
  logging, and compatibility-API change after two human changes-requested
  rounds and a fully green test/lint/build run
  ([CI](https://github.com/gitmono-dev/mega/actions/runs/21021822496)). Later
  accepted changes include
  [#1871](https://github.com/gitmono-dev/mega/pull/1871),
  [#1878](https://github.com/gitmono-dev/mega/pull/1878), and
  [#1920](https://github.com/gitmono-dev/mega/pull/1920).
- [open-vela/packages_demos #56](https://github.com/open-vela/packages_demos/pull/56)
  and [libra-tools/libra #95](https://github.com/libra-tools/libra/pull/95)
  provide independent accepted outcomes in additional project contexts after
  configuration, documentation, timestamp-semantics, and performance feedback.
- [X-Plore](https://github.com/lvy010/X-Plore),
  [Algo-Atlas](https://github.com/lvy010/Algo-Atlas), and
  [lvynote](https://github.com/lvy010/lvynote) provide owner-project context,
  but are not counted as independent validation.

Contradictions and blind spots:

- The visible account history begins in 2024, and 375 of 408 public owner
  repositories are forks that are excluded from attribution. The 24-month
  trajectory can be scored, but long-term durability cannot. Several prominent
  PRs remain open or were closed unmerged and receive only partial or zero
  realized-work credit.
- The representative owner projects have no releases and usually no workflows;
  [penguin-vl-ncnn](https://github.com/lvy010/penguin-vl-ncnn) is a positive CI
  exception, not evidence of a general release practice. There is no recurring
  review, merge, release, roadmap, or contributor-governance responsibility.
  This keeps S and I materially below E and T.
- Automated review found many defects in the largest Mega PR. The subject's
  signed fixes, feedback response, validation and merged outcome remain
  attributable, but debugging and verification credit is shared with bots, CI,
  and human reviewers.

## `liyupi`

- Role lens: Java/TypeScript full-stack products, developer education, and
  community maintenance.
- Capability interpretation: Contributor / Independent-builder boundary. The
  E sensitivity interval is 48–60; it crosses the E=55 independent-builder
  gate while S remains above its gate.
- R cohort: Chinese-language, high-visibility developer-education product
  creators. The frozen discovery frame used four GitHub repository searches —
  `编程 学习`, `学习 路线`, `项目 教程`, and `面试 题库` — each constrained to
  `in:name,description,readme stars:>=1000 pushed:>=2024-07-18 fork:false`.
  The top 100 results per query produced 200 deduplicated user-owned repositories
  across 184 accounts. Stars selected the high-visibility cohort but did not
  enter R or any capability score.

### Engineering and attribution

- [yupi-hot-monitor's hotspot checker](https://github.com/liyupi/yupi-hot-monitor/blob/cd48b0885bfa8ae9c8043cf78ef6cfd045530bdb/server/src/jobs/hotspotChecker.ts#L40-L250)
  coordinates multiple sources, deduplication, quotas, relevance checks and AI
  fallback. A fresh-clone review found 42 passing and 11 live-AI-skipped tests,
  but both standard production builds failed and no workflow ran those tests.
- [yu-ai-code-mother's generator facade](https://github.com/liyupi/yu-ai-code-mother/blob/893918c808ce7828cd4b9372967e064ed119bbaa/src/main/java/com/yupi/yuaicodemother/core/AiCodeGeneratorFacade.java#L79-L137)
  shows non-trivial strategy, streaming and service boundaries. Its file tool
  permits unsafe absolute or traversal paths
  ([source](https://github.com/liyupi/yu-ai-code-mother/blob/893918c808ce7828cd4b9372967e064ed119bbaa/src/main/java/com/yupi/yuaicodemother/ai/tools/FileWriteTool.java#L26-L50))
  before the service runs package lifecycle scripts
  ([source](https://github.com/liyupi/yu-ai-code-mother/blob/893918c808ce7828cd4b9372967e064ed119bbaa/src/main/java/com/yupi/yuaicodemother/core/builder/VueProjectBuilder.java#L39-L68)).
- [yu-picture's WebSocket handshake](https://github.com/liyupi/yu-picture/blob/a053632c41340152bf75b66b3c543d129123d8ec/yu-picture-backend/src/main/java/com/yupi/yupicturebackend/manager/websocket/WsHandshakeInterceptor.java#L57-L102)
  validates session and space permissions, while its URL upload path lacks full
  SSRF, redirect and size controls
  ([source](https://github.com/liyupi/yu-picture/blob/a053632c41340152bf75b66b3c543d129123d8ec/yu-picture-backend/src/main/java/com/yupi/yupicturebackend/manager/upload/UrlPictureUpload.java#L27-L90)).
- [yu-rpc](https://github.com/liyupi/yu-rpc) covers protocols, SPI, discovery,
  balancing, retry and tolerance. Its TCP client can leave a response future
  unresolved after connection failure
  ([source](https://github.com/liyupi/yu-rpc/blob/574338d58b886fb7d5fb596cfa9cccec1d7daa5b/yu-rpc-core/src/main/java/com/yupi/yurpc/server/tcp/VertxTcpClient.java#L36-L88)).

Implementation attribution is mixed. `yu-rpc` and `yu-picture` have strong
direct account attribution. `ai-guide` has 47 of 252 default-branch commits,
including 168 translation-bot commits; `github-claw` has 16 subject commits,
29 Copilot commits and four Claude commits in the inspected default history.
`yu-ai-code-mother` exposes extensive Cursor branches and an explicitly
Cursor-assisted [PR #9](https://github.com/liyupi/yu-ai-code-mother/pull/9).
These reduce direct implementation credit without erasing evidenced product,
merge, or outcome responsibility.

### Stewardship, impact, and trajectory

- [codefather](https://github.com/liyupi/codefather) remains active from 2021
  through the snapshot and has several independent contributors.
  [ai-guide](https://github.com/liyupi/ai-guide) has repeated contributors and
  some distributed merge responsibility; PR
  [#15](https://github.com/liyupi/ai-guide/pull/15) shows a concrete review,
  correction, approval and merge path.
- Formal release and verification practice is uneven. `codefather` has one
  public release, many representative teaching projects have no release or CI,
  and the most recent `ai-guide` synchronization run failed
  ([run](https://github.com/liyupi/ai-guide/actions/runs/28526020536)).
- Knowledge diffusion has evidence beyond repository attention: the public
  [CodeFather community](https://www.codefather.cn/) remains active; a book
  authored under the subject's public identity has an independent
  [university-library record](https://opac.uibe.edu.cn/opac/search?field=creatorSearch&q=%E7%A8%8B%E5%BA%8F%E5%91%98%E9%B1%BC%E7%9A%AE%E8%91%97);
  a [public project course](https://www.bilibili.com/video/BV1YvmbYbEgS/) and a
  [third-party SQL tutorial](https://www.bilibili.com/video/BV14P411p7Ss) show
  continuing consumption and reuse. At least one recent `sql-mother` fork has
  material independent changes
  ([compare](https://github.com/liyupi/sql-mother/compare/master...DaemonforY:master)).
  These support I=60, but GitHub search did not establish broad multi-organization
  dependency or current external technical authority. Repository stars, forks,
  views, and profile followers are therefore not converted directly into
  adoption credit.
- Recent scope expands from interview and full-stack teaching projects into AI
  agents, GitHub Apps, automated translation and real-time monitoring. The
  account has no verified non-owner PR or review closure in the recent window;
  rapid agent-PR merges and unresolved repeated failures limit external
  validation and learning anchors.
- Of 24 non-fork repositories created in the recent window, 11 stopped receiving
  pushes within one day and 12 within seven days. This is activity, not 24
  independent maintenance contexts, and it is not linearly added to S or T.

### Scarcity sensitivity and blind spots

Only 12 of the 184 high-visibility cohort accounts had at least two matched
repositories, and manual inspection found few that combined long-lived Chinese
curriculum, runnable learning products, and visible maintenance responsibility.
That supports R=61 for the bundled educator-maintainer role. The discovery
sample is attention-biased and not a population census, so R confidence is
medium-low. If the role is reduced to the common Java/Vue/AI full-stack stack,
the same structural scoring falls to about 42.

Private commercial systems, actual learner counts, production incident history,
and undisclosed AI assistance remain outside the public boundary. These gaps
could change E/I confidence but must not be treated as negative evidence.

## `Sunrisepeak`

- Role lens: modern C++ build and package infrastructure, cross-platform
  developer tooling, and open-source community maintenance.
- Capability interpretation: Maintainer / technical leader, with material
  implementation-attribution and bus-factor sensitivity.
- General profile score: `0.55E + 0.20S + 0.15I + 0.10T = 75.9`, displayed
  as **76/100**. R is excluded.
- Confidence: medium overall. Repository, release, and account-control facts
  are high confidence; direct authorship of recent implementation and review
  reasoning is medium confidence because AI participation is explicit.
- R cohort hypothesis: global public-OSS maintainers who lead cross-platform
  C/C++ build and package infrastructure while directly handling C++20/23
  Modules graphs, multiple compiler toolchains, version or package indexes,
  isolation, and automated releases.

### Engineering evidence and attribution

The account has 32 non-fork and 31 fork repositories. Only attributable work
from non-forks, transferred projects, and accepted upstream changes is scored;
forks of Linux, XMake, ROS, and other projects do not inherit upstream credit.
The current `openxlings` and `mcpp-community` organizations postdate some of
their principal repositories, so transfers into those organizations are not
treated as independent adoption.

- [`mcpp` PR #231](https://github.com/mcpp-community/mcpp/pull/231) traced a
  Windows exit 127 through a directory-symlink escape, CJK wide-to-narrow path
  conversion, and an uncaught exception. It added three defensive layers, a
  Linux behavioral control, a regression E2E, and dump-backed diagnosis.
- [`mcpp` PR #216](https://github.com/mcpp-community/mcpp/pull/216) separates
  host and target semantics for Linux-to-Windows MinGW builds; [`#223`](https://github.com/mcpp-community/mcpp/pull/223)
  coordinates manifest, scanner, fingerprint, generated-file, and per-glob
  flag contracts with a large E2E matrix.
- [`xlings` PR #373](https://github.com/openxlings/xlings/pull/373) replaces
  timing assumptions in OSC-11 terminal probing with a DSR/CPR completion
  fence, monotonic deadline, bounded buffer, socket-pair tests, and real-PTY
  controls. [`PR #359`](https://github.com/openxlings/xlings/pull/359) follows
  a user-visible cache incident across `xlings`, `libxpkg`, `tinyhttps`, and
  package-index boundaries with staged writes, verification, locking, tests,
  release, and follow-up.

Those artifacts support E=78, not a higher result. The current
[`tinyhttps` TLS path](https://github.com/mcpplibs/tinyhttps/blob/965d805050d02fd6ed244473a6a68b6ace4bf032/src/tls.cppm#L214-L219)
sets optional certificate verification without checking the post-handshake
result, despite a `verifySsl` interface. Some download failures also leave a
pooled connection reusable
([source](https://github.com/mcpplibs/tinyhttps/blob/965d805050d02fd6ed244473a6a68b6ace4bf032/src/http.cppm#L1047-L1089)),
and a current `mcpp` release/index ordering mismatch broke the
[`hermetic-e2e` gate](https://github.com/mcpp-community/mcpp/actions/runs/29626240699).
The reasonable E sensitivity interval is 73–82.

AI assistance is directly evidenced, not inferred from activity volume.
[`xlings/.agents`](https://github.com/openxlings/xlings/blob/main/.agents/README.md)
identifies an agent workspace for designs and plans; at least 51 inspected
default-branch commits explicitly name Codex, Claude, or Copilot, including
[`76c2523`](https://github.com/openxlings/xlings/commit/76c252311c0e602ad33831b500a51114be6a3bd3).
`mcpp` documents an agent contribution workflow and one representative commit
states that it was
[`generated with Claude Code`](https://github.com/mcpp-community/mcpp/commit/35eae70f11c4afbfd1082329251cdd9a330ff24d).
One detailed `xlings` review also says it was
[`generated with Claude Code`](https://github.com/openxlings/xlings/pull/322).
Implementation, design prose, and some review reasoning therefore receive
shared attribution. Requirement selection, CI response, merge, release,
incident follow-up, and outcome accountability remain directly attributable;
unmarked commits are not assumed to be AI-generated.

### Stewardship and trajectory

- [`xlings`](https://github.com/openxlings/xlings) has been sustained since
  2024 with multi-platform CI and 73 releases. `mcpp` adds C++23 Modules,
  GCC/Clang/MSVC, cross-build, package-index, and release responsibility.
  Its 96 pre-1.0 releases in roughly 72 days demonstrate release operation,
  but are one correlated development burst rather than 96 independent
  maintenance contexts.
- Cross-contributor review is real but narrow. Examples include substantive
  change requests and closure in [`mcpp-index #64`](https://github.com/mcpplibs/mcpp-index/pull/64),
  [`cmdline #8`](https://github.com/mcpplibs/cmdline/pull/8),
  [`d2mcpp #23`](https://github.com/mcpp-community/d2mcpp/pull/23), and
  [`xlings #100`](https://github.com/openxlings/xlings/pull/100). Membership,
  CLA, team-approval, and public-task paths exist, but whole-repository
  CODEOWNERS and approval responsibility remain concentrated on Sunrisepeak.
- The concentration is a strong counterweight: all 184 inspected merged
  subject-authored `mcpp` PRs were self-merged with no review, and all 260
  inspected merged subject-authored `xlings` PRs were self-merged. High-frequency
  index and release PRs are not counted linearly.
- T=78 comes from a qualitative sequence: earlier personal C++ projects and a
  scoped [`LVGL` fix](https://github.com/lvgl/lvgl/pull/6541), then the
  multi-platform `xlings` lifecycle, then C++23 Modules/build-system ownership,
  and finally a paired ROS 2 Fish-shell feature in
  [`ament_package #164`](https://github.com/ament/ament_package/pull/164) and
  [`ros2cli #1211`](https://github.com/ros2/ros2cli/pull/1211). The ROS change
  received maintainer review, independent local testing, approval, and official
  multi-platform CI. It also explicitly disclosed Opus and Codex review, so it
  establishes external acceptance and follow-through without proving unaided
  implementation.

S and T each have a reasonable sensitivity interval of 71–82 and 73–84,
respectively. At their displayed values the packet satisfies the maintainer
band's review, release, and governance condition, but the lower S sensitivity
case would place it at System owner. This boundary should be rechecked after
independent redacted scoring.

### Impact, scarcity, and blind spots

- `xlings` release assets had about 15,250 downloads at the snapshot, and
  multiple independent accounts reported real Windows, macOS, and Linux use.
  Downloads are not unique users, and public `.xlings.json` downstreams remain
  concentrated in the subject's own organizations. Of 47 inspected forks, only
  one had a single stale independent commit.
- [`d2mcpp`](https://github.com/mcpp-community/d2mcpp) supplies the strongest
  knowledge-diffusion evidence. At least 13 of the first 100 inspected forks
  contained independent work, including a current learner's
  [completed exercise commits](https://github.com/mcpp-community/d2mcpp/compare/main...firefantasy:main).
  The curriculum also has an independent
  [HelloGitHub listing](https://hellogithub.com/en/repository/mcpp-community/d2mcpp)
  and a public video series with substantial consumption. This supports
  knowledge diffusion, not a claim that views equal engineering adoption.
- `xlings` and `mcpp` package reusable infrastructure and the subject holds
  recurring interface, merge, and release authority. However, same-owner
  organizations are one correlated ecosystem; the subject-maintained AUR
  packages have no independent popularity signal, and no official Homebrew,
  vcpkg, or Conan Center inclusion was verified. Removing either `xlings` or
  `d2mcpp` lowers I from 64 to roughly 56–57.

R remains formally `unknown`. The diagnostic anchors produce 69 for the named
role, but discovery used project lists and metadata-dependent repository
searches rather than a credibly sampled talent cohort. A broader C/C++
build-or-package-maintainer role lowers the diagnostic result to about 59; a
module-first role tailored too closely to `mcpp` raises it to about 73 and is
rejected as circular.

Private production use, unique active installations, incident history outside
public issues, undisclosed AI assistance, and independent evidence for the
profile's founder claim remain outside the boundary. These are uncertainty,
not negative evidence.

## `sheepbox8646`

- Role lens: multi-agent product platforms, persistent agent control planes,
  isolated workspaces, Computer Use, and full-stack release operation.
- Capability interpretation: System owner, adjacent to the Maintainer /
  technical-leader boundary. E=74 and S=73 both sit just below that band's
  quantitative gates, while their lower sensitivity cases remain System owner.
- General profile score: `0.55E + 0.20S + 0.15I + 0.10T = 73.0`, displayed
  as **73/100**. R is excluded.
- Confidence: medium overall. Identity, repository control, merge, CI, and
  release facts are well evidenced; recent implementation and review-reasoning
  attribution are only medium because disclosed agent participation is material.
- R cohort hypothesis: global public-OSS technical leads who combine agent
  runtime and state, multi-user control planes, container or micro-VM workspace
  isolation, browser or desktop Computer Use, and release responsibility.

### Engineering evidence and attribution

The account owns 54 public repositories: 29 are currently marked non-forks and
25 forks. The empty personal [`ChatTutor` transfer placeholder](https://github.com/sheepbox8646/ChatTutor),
forks, source snapshots, and organization membership are not scored as original
systems. The packet instead uses attributable organization work and accepted
upstream changes. In [`Memoh`](https://github.com/memohai/Memoh), the subject is
the first and largest contributor, with 585 of 1,221 inspected default-branch
commits, but several other contributors have substantial independent histories.

- [`Memoh` PR #808](https://github.com/memohai/Memoh/pull/808) carries a
  per-request execution target through database migration, history metadata,
  send/retry/edit, approval and user-input resumption, workspace routing,
  OpenAPI/SDK contracts, and regression tests. It is strong evidence of
  cross-module interface reasoning even though the `codex/` branch and
  self-merge make implementation attribution shared rather than exclusive.
- [`PR #502`](https://github.com/memohai/Memoh/pull/502) integrates a Rust
  AT-SPI command-line layer with Go tools, container desktops, musl builds, and
  CI. [`PR #539`](https://github.com/memohai/Memoh/pull/539) then traces a real
  CJK input failure to UTF-8 byte counts versus Unicode scalar counts and adds
  ASCII, CJK, mixed, emoji, and empty-input regressions.
- [`PR #581`](https://github.com/memohai/Memoh/pull/581) threads CPU, memory,
  and storage limits through persistence, APIs, backup/import, containerd,
  Docker, SDK, and UI. [`PR #586`](https://github.com/memohai/Memoh/pull/586)
  expands the same responsibility to containerd/Kata runtime selection, KVM
  preflight, workspace bridge routing, evidence validators, Compose, and CI.
- [`xsai` PR #231](https://github.com/moeru-ai/xsai/pull/231) is the cleanest
  independent upstream control: seven iterations delivered a complete streaming
  transcription package with implementation, SSE conversion, tests, docs, and
  package metadata; an upstream maintainer approved it, and the feature entered
  [the v0.4.0-beta.6 release](https://github.com/moeru-ai/xsai/releases/tag/v0.4.0-beta.6).

Those artifacts support E=74 from `3.5 / 4 / 4 / 3 / 4`. Implementation is held
at 3.5 because recent code authorship is materially shared with agents;
architecture, debugging, and constraint credit is retained where requirements,
cross-layer closure, tests, and acceptance responsibility are inspectable.
Independent engineering readings place the central case around 72–78, with a
broader attribution and validation sensitivity interval of about 66–80.

AI participation is direct evidence, not an inference from activity volume.
Of 277 inspected subject-linked default-branch commits in
[`ohmygithub`](https://github.com/ohmygit-hub/ohmygithub), 209 explicitly name a
Claude model as co-author. Memoh also has commits marked
[`Generated with Claude Code`](https://github.com/memohai/Memoh/commit/80b15d1b108519df0663bccc7626ff2efeb904e3)
or with a [Claude co-author](https://github.com/memohai/Memoh/commit/50986bf130aaac9cc2948caf034abfdc503e9bf1),
and representative branches and reviews explicitly invoke Codex, Cursor, or
Claude. Implementation and some design or review prose therefore receive shared
attribution. Product selection, merge and release authority, response to CI and
human feedback, and public outcome accountability remain directly attributable;
unmarked changes are not automatically classified as AI-generated.

Reliability is therefore 3 rather than 3.5. PR #581 omitted resource-limit
restoration before merge and PR #586 supplied the later fix. PR #586 said real
`io.containerd.kata.v2` validation required a self-hosted KVM runner, but its
[Linux/KVM E2E check was skipped](https://github.com/memohai/Memoh/actions/runs/27096985469/job/79970834091)
before the self-merge. The current Kata workflow also does not trigger on its Go
runtime or bridge paths. At the snapshot, a fresh ChatTutor install failed all
three test files: two mix [`bun:test` with a Vitest root script](https://github.com/HugeCatLab/ChatTutor/blob/7d9e9052bc5abc5239f3a44f4754b3082f765317/package.json),
and another tests an [obsolete message-resolver contract](https://github.com/HugeCatLab/ChatTutor/blob/7d9e9052bc5abc5239f3a44f4754b3082f765317/packages/shared/test/message-resolver.test.ts).
The current `sciux-kit/lib` typecheck also fails on directly attributable
[duplicate properties and setup code](https://github.com/sciux-kit/lib/blob/b3aea7e550cf507cb8a84004b96ecf5cec74b530/packages/math/src/angle/points.ts#L94-L97),
while its test command finds no files. A later 267-file tenancy foundation in
[`PR #759`](https://github.com/memohai/Memoh/pull/759) was correctly closed
instead of merged after review found several default-team boundary errors, but
it remains a negative architecture and validation sample.

### Stewardship and trajectory

- Memoh has 55 public releases in roughly six months. Fifty-four were published
  through Actions, about 43 inspected annotated version tags were signed by the
  subject, and the [release workflow](https://github.com/memohai/Memoh/blob/main/.github/workflows/release.yml)
  covers source bundles, two npm scopes, three desktop platforms, and macOS
  signing and notarization. High-frequency pre-1.0 releases are one correlated
  lifecycle, not 55 independent maintenance contexts.
- Of 679 inspected Memoh PRs, the subject authored 144 and merged 378. Merge and
  release authority is genuinely distributed to other contributors, and
  [CODEOWNERS](https://github.com/memohai/Memoh/blob/main/.github/CODEOWNERS)
  delegates backend, agent-loop, runtime, web, and desktop surfaces to teams.
  This supports recurring governance rather than organization membership alone.
- Review depth is the counterweight. Of 255 inspected subject review events,
  248 were bodyless approvals and only two requested changes; 122 of the
  subject's 126 merged Memoh PRs were self-merged, with few visible human
  approvals. The active rule nominally requests one approval, yet many later
  self-merges have no public approval, consistent with an administrator bypass.
  This proves gate responsibility but not a repeatedly high-quality review
  culture.

Those facts produce S=73 from `4 / 4 / 3 / 3.5`, with a reasonable sensitivity
interval of 69–78. System owner is stable; Maintainer / technical leader remains
an adjacent possibility rather than the displayed band.

T=73 follows a non-linear two-year progression. Earlier attempts include the
closed [`VitePress` API-index PR #3870](https://github.com/vuejs/vitepress/pull/3870),
a `bumpp` change the subject correctly closed after discovering existing
support, and [`xsai` PR #166](https://github.com/moeru-ai/xsai/pull/166), where an
upstream maintainer rejected the proposed interpolation API and escaping model.
The later released `xsai` transcription package supplies the clean external
success; then Memoh expands the scope into agent state, multi-tenancy, databases,
containers, Computer Use, CI, release, and contributor responsibility. The
recent open [`Memoh` PR #828](https://github.com/memohai/Memoh/pull/828) shows
prompt closure on human findings about fail-open tenancy, idempotency, and
bounded cancellation, but it remains open and receives only partial realized-work
credit. The anchors are `4 / 3 / 3.5 / 4`, with a reasonable interval of 66–79.

### Impact, scarcity, and blind spots

- Memoh has real use beyond attention. Independent users filed install,
  provider, production-image, and memory-operation reports; its public release
  assets had about 1,902 downloads at the snapshot. Docker Hub showed about
  26,038 `server`, 19,537 `web`, and 836 `workspace` pulls, but these correlated
  counts include upgrades, CI, and repeated pulls and are not unique users.
- Independent reuse includes [`GenMult`](https://github.com/ZihengXiong/GenMult),
  which says it is built on Memoh, the now-discontinued
  [`Memoh-v2`](https://github.com/Kxiandaoyan/Memoh-v2), and a
  [New API integration guide](https://github.com/QuantumNous/new-api-docs-v1/blob/main/content/docs/zh/apps/memoh.mdx).
  The subject's released [`@xsai/stream-transcription`](https://www.npmjs.com/package/@xsai/stream-transcription)
  package also had about 25,300 downloads in the inspected month and remains in
  independent downstream code. Downloads are distribution evidence, not unique
  people, and ongoing package maintenance is not wholly attributable to the
  original contributor.
- I=69 comes from `3.5 / 3.5 / 3.5 / 4 / 2.5 / 2.5`, with a reasonable interval
  of 62–74. Memoh project impact is attributed to the subject at roughly
  45%–65%, not inherited wholesale. Removing Memoh and its derivatives lowers I
  to roughly 43–47. Project stars, forks, and the account's followers were used
  only for navigation.

R remains formally `unknown`. The diagnostic anchors `3.5 / 3.5 / 4 / 3.5 / 3`
produce 71 for the named multi-agent-platform role, but discovery relied on
repository and metadata search rather than a reproducible sample of qualified
people. A broad full-stack agent-product role lowers the diagnostic to about 49;
a narrow role tailored to Memoh raises it to about 80 and is rejected as circular.

Memoh's public history is only about six months, its hosted cloud remained
forthcoming at the snapshot, some derivatives and ChatTutor are already inactive,
and its npm SDK surface lags the main application. Private production scale,
unique installations, undisclosed AI assistance, the subject's formal
organization role, and incident history outside public issues remain unknown.
These gaps may move confidence or sensitivity but are not scored as failures.

## `bagder`

- Role lens: portable network-protocol library maintainer, security and release
  lead.
- Capability interpretation: Maintainer / technical leader.
- R cohort: top-level maintainers who combine public API compatibility,
  multi-protocol state machines, TLS and resolver integration, portability, and
  release/security responsibility for general-purpose network client libraries.
  The 2026-07-18 discovery frame uses the public maintainer and release records
  for [curl](https://github.com/curl/curl/blob/master/docs/GOVERNANCE.md),
  [OpenSSL](https://openssl-library.org/community/omc/),
  [nghttp2](https://github.com/nghttp2/nghttp2),
  [libssh2](https://github.com/libssh2/libssh2), and
  [GNU Wget](https://git.savannah.gnu.org/cgit/wget.git/tree/AUTHORS). It is not
  a labor-market sample.

### Engineering and attribution

- [`curl/curl#15289`](https://github.com/curl/curl/pull/15289) repairs
  undefined-behavior sanitizer findings by aligning callback types across 42
  files and preserving tests and public behavior.
  [`curl/curl#17253`](https://github.com/curl/curl/pull/17253) moves the shared
  `curlx_` surface through 463 files while reasoning about legacy MSVC builds,
  linkage, symbol collisions, and merge sequencing. The latter was discussed at
  curl-up and received independent manual VS2010 validation.
- [`curl/curl#17134`](https://github.com/curl/curl/pull/17134) introduces a
  resolver wrapper with c-ares-aware debugging and test support, while
  [`curl/curl#16358`](https://github.com/curl/curl/pull/16358) changes IPv6
  `CURLOPT_RESOLVE` replacement semantics with documentation, tests, and
  multi-person design discussion. These are distinct interface, diagnostic,
  and compatibility traces rather than one large refactor counted repeatedly.
- Reviews of [`curl/curl#22302`](https://github.com/curl/curl/pull/22302) and
  [`curl/curl#22247`](https://github.com/curl/curl/pull/22247) show current
  judgment over negative-DNS-cache poisoning, threaded/c-ares/DoH resolver
  differences, and MIME filename header injection. Both were still open at the
  snapshot, so they support review quality and T only, not realized I.

Those artifacts produce E=96 from `4.5 / 5 / 5 / 4.5 / 5`. The implementation
and reliability half-points retain the counterevidence: the 463-file change was
self-merged without a formal approval after several CI failures, and a later
comment on #15289 reported a `CURL_STRICTER` C++ break. The packet does not infer
that every curl regression, protocol implementation, or test is personally
attributable to the subject.

### Stewardship, impact, and trajectory

- Curl's [governance](https://github.com/curl/curl/blob/master/docs/GOVERNANCE.md)
  names Daniel Stenberg as the driving force and current final decision point,
  while also defining maintainers, a core team, a security team, server
  administration, and a succession path. The
  [release procedure](https://github.com/curl/curl/blob/master/docs/RELEASE-PROCEDURE.md)
  defines an eight-week cadence, feature windows, freezes, signing, and release
  checks. The subject published the inspected 8.12.0 through 8.21.0 GitHub
  releases. This yields S=98 from `5 / 5 / 4.5 / 5`.
- The incomplete [commercial-use list](https://curl.se/docs/companies.html),
  independent operating-system distribution, and decades of retained API
  dependence establish ecosystem-shaping adoption. The
  [contributor history](https://github.com/curl/curl/graphs/contributors) also
  shows a real multi-contributor project, so adoption and community are held at
  4.5 rather than transferring curl's full outcome to one person. The durable
  [Everything curl](https://everything.curl.dev/) reference supports knowledge
  diffusion. I=96 follows `4.5 / 5 / 5 / 4.5 / 5 / 5`.
- T=70 from `2.5 / 5 / 4 / 2.5` is intentionally far below the other axes.
  The recent window demonstrates continuing apex-level responsibility and
  external reliance, but limited difficulty or scope expansion relative to the
  subject's own multi-decade baseline. High current activity is not treated as
  growth by itself.

R=90 follows `4.5 / 4 / 5 / 4.5 / 4.5` within the named network-library
cohort. The result is driven by the unusual coupling of protocol semantics,
portable C, ABI compatibility, TLS/resolvers, security response, and a broad
release matrix; it says nothing about compensation or demand. Reasonable
sensitivity intervals are E 93–97, S 94–99, I 92–98, T 62–76, and R 84–92.
Confidence is high for the public boundary, but private incident work and
security reports are unknown.

## `BurntSushi`

- Role lens: Rust text-search, automata, and performance-library maintainer.
- Capability interpretation: Maintainer / technical leader.
- R cohort: maintainers with verified ownership across foundational Rust
  text-scanning crates, automata semantics, command-line search, performance
  engineering, and cross-platform correctness. The comparison frame uses the
  [Rust Library Team's public remit](https://std-dev-guide.rust-lang.org/team/summary.html)
  and public owner, reverse-dependency, release, and contribution records for
  `regex`, `regex-automata`, `aho-corasick`, `memchr`, `bstr`, `jiff`, and
  `ripgrep` as of the snapshot. Overlap between those crates is treated as
  concentration, not seven independent observations.

### Engineering and AI attribution

- [`rust-lang/regex#1364`](https://github.com/rust-lang/regex/pull/1364)
  supplies a minimal reproduction and a semantics-level repair for reverse
  suffix/inner optimization under leftmost-first matching, with regression,
  MSRV, Miri, platform, and `rebar` benchmark validation. The subject explicitly
  says an LLM wrote the PR, then records that he rejected the original complex
  solution, simplified it, checked semantics, and accepted measured performance
  regressions to restore correctness. Implementation authorship is shared;
  diagnosis, trade-off, and verification ownership remain directly evidenced.
- [`BurntSushi/ripgrep#3472`](https://github.com/BurntSushi/ripgrep/pull/3472)
  adds incremental ignore checking and responds to externally raised hidden
  ancestor, symlink, Windows, and case-insensitive-filesystem cases before an
  immediate `ignore` crate release.
  [`BurntSushi/ripgrep#3475`](https://github.com/BurntSushi/ripgrep/pull/3475)
  fixes a worker-panic deadlock, while its review also identifies a remaining
  builder-panic hang scenario; the follow-up risk prevents a ceiling reliability
  anchor.
- [`BurntSushi/jiff#593`](https://github.com/BurntSushi/jiff/pull/593) repairs a
  non-empty-buffer soundness bug and passes no-std, Miri, fuzz, feature, and
  platform matrices. [`astral-sh/ruff#26771`](https://github.com/astral-sh/ruff/pull/26771)
  is an independent organization trace: the subject's ignore-system change
  received upstream review and passed Ruff's broader test, ecosystem, and
  benchmark gates.

E=94 follows `4.5 / 5 / 4.5 / 4.5 / 5`. The half-points preserve the disclosed
AI implementation share, the intentional benchmark regressions in #1364, and
the post-merge edge identified around #3475; the score is not based on crate
download totals.

### Stewardship, impact, and trajectory

- Sustained releases of [`ripgrep`](https://github.com/BurntSushi/ripgrep/releases),
  `regex`, and the newer `jiff` demonstrate long-lived ownership and
  compatibility work. External review succeeds in ripgrep and Ruff, but the
  [contribution histories](https://github.com/BurntSushi/ripgrep/graphs/contributors)
  remain strongly subject-concentrated and do not show a comparably mature
  maintainer-succession institution. S=87 therefore uses `5 / 4.5 / 4 / 3.5`.
- Crates.io shows broad independent reverse dependence for
  [`regex`](https://crates.io/api/v1/crates/regex),
  [`memchr`](https://crates.io/api/v1/crates/memchr),
  [`aho-corasick`](https://crates.io/api/v1/crates/aho-corasick), and
  [`bstr`](https://crates.io/api/v1/crates/bstr), while `ripgrep` and
  [`jiff`](https://crates.io/api/v1/crates/jiff) extend the leverage into end-user
  search and date/time correctness. Registry downloads include CI and repeated
  installs; reverse dependencies, independent upstream acceptance, and
  multi-year maintenance carry the impact claim. I=93 follows
  `5 / 5 / 4.5 / 3.5 / 4.5 / 5`.
- T=88 from `4 / 4.5 / 5 / 4` reflects movement from an already high regex
  baseline into Jiff's temporal constraints, external Ruff integration, and an
  explicit agent-assisted workflow in which generated solutions are benchmarked,
  simplified, and sometimes rejected. Scope expansion remains below the
  cross-domain five anchor, and this is not a raw-commit acceleration score.

R=82 from `4.5 / 4 / 4.5 / 3 / 4.5` is confined to the named Rust
text/search-performance cohort. Reasonable sensitivity intervals are E 89–96,
S 80–91, I 89–95, T 80–92, and R 75–86. Confidence is high because AI credit is
disclosed and the selected work has inspectable tests, reviews, and release
outcomes; undisclosed private performance work remains unknown.

## `FiloSottile`

- Role lens: Go cryptography, security protocols, transparency systems, and
  maintainable specifications.
- Capability interpretation: Maintainer / technical leader.
- R cohort: public maintainers who combine production cryptographic-library
  implementation, protocol specification, test-vector design, security release
  responsibility, and certificate/transparency-log operations. The comparison
  frame uses the [C2SP maintainer model](https://github.com/C2SP/C2SP/), the
  [Go security process](https://go.dev/doc/security/policy), public Go crypto
  commit/review records, and public C2SP, CT, and Sigsum maintainer records at
  the snapshot. It is a technical-supply frame, not a market-value estimate.

### Engineering and attribution

- [`FiloSottile/age#651`](https://github.com/FiloSottile/age/pull/651) adds
  hybrid post-quantum and tagged recipients across 35 files, while preserving
  plugin and older-client compatibility and testing Linux, macOS, Windows,
  FreeBSD, oldstable/current Go, static analysis, and vulnerability scanning.
  External cryptographic reviewers participated before release.
- [`FiloSottile/sunlight#56`](https://github.com/FiloSottile/sunlight/pull/56)
  designs priority eviction and metrics for load shedding in a certificate
  transparency log. One small commit is Copilot-coauthored; the surrounding
  architecture, core implementation, tests, and operational rationale remain
  attributable to the subject. Two `go.mod latest` checks were failing at merge,
  which is retained as reliability counterevidence.
- [`C2SP/C2SP#225`](https://github.com/C2SP/C2SP/pull/225) develops a chunked
  encryption specification and changes commitments and limits in response to
  independent cryptographic review.
  [`C2SP/wycheproof#248`](https://github.com/C2SP/wycheproof/pull/248)
  supplies ML-DSA randomized test vectors and schema changes under external
  approval. These specification and adversarial-test traces are independent of
  the age implementation artifact.
- Recent directly attributable Go work includes P-256 scalar
  [replacement](https://github.com/golang/go/commit/be35de22f18a3c16e24a20490ec1fc316ea12b04)
  and [optimization](https://github.com/golang/go/commit/2c659bb4db1ff06c819f8b4cd6decc71e4d5b36e),
  plus TLS [ML-KEM](https://github.com/golang/go/commit/6b0243ccf6e83afbd79889a7862599cb5992660c)
  and [ML-DSA](https://github.com/golang/go/commit/c74ba7d265519fab5794e5b69e4e9f6c25b45582)
  support. Credit is limited to the linked changes, not the whole Go standard
  library.

E=96 uses `5 / 5 / 4 / 5 / 5`; the debugging anchor distinguishes strong public
design and validation traces from repeated cross-context incident diagnosis.
S=94 from `5 / 5 / 4.5 / 4` reflects release and standards authority with
external review, while retaining the owner concentration in age and Sunlight
and avoiding a governance ceiling before independent calibration.

### Impact, trajectory, and blind spots

- [`age` releases](https://github.com/FiloSottile/age/releases) ship the linked
  post-quantum work and an interoperable format used by the independent
  [`rage`](https://github.com/str4d/rage) implementation,
  [`SOPS`](https://github.com/getsops/sops), hardware plugins, and major package
  repositories. C2SP turns those interfaces into versioned, reviewable public
  specifications. Go crypto changes supply high downstream leverage, but their
  adoption belongs to the Go team and ecosystem as well as the author. I=94
  therefore uses `4.5 / 5 / 5 / 4.5 / 4 / 5` rather than ceiling attribution.
- T=95 from `4.5 / 5 / 5 / 4.5` captures externally reviewed expansion from an
  already deep Go-crypto baseline into post-quantum standard-library support,
  interoperable specifications, adversarial vectors, and operational CT
  infrastructure. Scope is held at 4.5 because these remain related security
  systems. This is relative growth, not a reward for cryptography being rare.
- R=93 follows `4.5 / 4.5 / 5 / 5 / 4` within the named cohort. The score
  would be lower for a broad application-security role and is not portable to
  that role.

Reasonable sensitivity intervals are E 92–98, S 88–97, I 90–96, T 89–98, and
R 86–95. Confidence is high for public work. Private vulnerability handling,
production incident volume, and undisclosed security consultations are unknown
and are not assumed positive or negative.

## `yyx990803`

- Role lens: frontend framework/compiler architecture and ecosystem technical
  leadership.
- Capability interpretation: Maintainer / technical leader.
- R cohort: creator-maintainers who retain public technical authority across a
  widely adopted UI framework plus its compiler and build-tool interfaces. The
  2026-07-18 frame uses the official [Vue core-team roster](https://vuejs.org/about/team),
  [Vite team record](https://github.com/vitejs/vite/blob/main/docs/team.md), and
  public core/release records for React, Angular, Svelte, Solid, and their build
  integrations. This is a role-conditioned project-maintainer sample, not a
  ranking of frontend developers generally.

### Engineering and project attribution

- [`vuejs/core#12359`](https://github.com/vuejs/core/pull/12359) is an
  eight-month, 303-file Vapor-mode integration spanning compiler, runtime,
  interoperability, tests, end-to-end cases, and size reports. Ninety-nine of
  the 100 listed commits are attributable to the subject. It is strong direct
  architecture evidence, but still one correlated Vue artifact rather than 303
  independent observations.
- [`vuejs/core#11944`](https://github.com/vuejs/core/pull/11944) removes
  exponential cost and stack-depth failure in deeply chained computed refs.
  [`vuejs/core#11458`](https://github.com/vuejs/core/pull/11458) adds lazy
  hydration strategies while reasoning about tree shaking, Suspense,
  reactivity, teardown, documentation, and externally raised edge cases.
- Vapor merged without formal human approval and with several incomplete
  feature/documentation items. An accidental squash required revert and manual
  re-merge to restore history. The sampled direct changes were commonly
  self-merged. Those facts keep implementation and reliability at 4.5 and give
  E=93 from `4.5 / 5 / 4.5 / 4.5 / 4.5`.
- [`rolldown/rolldown#8446`](https://github.com/rolldown/rolldown/pull/8446)
  records the subject's approval and process direction for an AI-assisted,
  spec-driven workflow, not Rolldown implementation authorship. Rolldown's
  contribution graph and Vite's distributed team prevent transferring their
  entire code, review, or release output to the subject.

### Stewardship, impact, and trajectory

- Direct Vue ownership plus the public Vue and Vite teams establish durable
  roadmap, release, and contributor institutions beyond a solo project. The
  recent direct PR sample nevertheless contains less visible review of others
  than its governance reach might imply. S=93 follows `5 / 5 / 4 / 4.5`,
  keeping durable team governance below a person-level ceiling.
- Exact-window npm telemetry for
  [`vue`](https://api.npmjs.org/downloads/point/2026-06-18:2026-07-17/vue),
  [`vite`](https://api.npmjs.org/downloads/point/2026-06-18:2026-07-17/vite),
  and [`vitepress`](https://api.npmjs.org/downloads/point/2026-06-18:2026-07-17/vitepress)
  corroborates broad distribution but includes CI, caches, and repeat installs.
  Independent framework integrations, stable public interfaces, and continued
  team maintenance carry the impact claim. I=97 uses
  `5 / 5 / 5 / 4.5 / 4 / 5`, retaining attribution discounts for team-owned
  outcomes and knowledge diffusion that is difficult to isolate personally.
- T=85 from `4 / 4 / 4.5 / 4.5` recognizes Vapor and expansion from Vue into
  build/compiler direction, but does not equate the Rolldown team's execution
  or current ecosystem size with the subject's personal growth. Relative to the
  earlier Vue/Vite baseline, this is meaningful expansion rather than a new
  five-anchor difficulty regime.

R=82 follows `4.5 / 4 / 4.5 / 3 / 4.5` within the named
framework/compiler-leader cohort. Reasonable sensitivity intervals are E
88–95, S 87–96, I 94–99, T 77–90, and R 75–87. Confidence is high for Vue and
team governance; private organizational decisions and uncredited work inside
Rolldown or Vite remain unknown.

## `mitchellh`

- Role lens: cross-platform terminal/runtime performance creator and subsystem
  governor, with older infrastructure-tooling work used only as a baseline.
- Capability interpretation: Maintainer / technical leader.
- R cohort: public creator-maintainers of cross-platform, GPU-accelerated
  terminal emulators who own terminal semantics, rendering/runtime boundaries,
  OS integration, performance, packaging, and contributor governance. The
  snapshot frame uses maintainer, contributor, and release records for
  [Ghostty](https://github.com/ghostty-org/ghostty),
  [WezTerm](https://github.com/wezterm/wezterm),
  [kitty](https://github.com/kovidgoyal/kitty), and
  [Alacritty](https://github.com/alacritty/alacritty). It is not a general
  systems-engineer or employment-market cohort.

### Engineering and AI attribution

- [`ghostty#13264`](https://github.com/ghostty-org/ghostty/pull/13264) builds
  page-based scrollback compression through a 38-file `PageList` refactor, LZ4,
  OS memory reclamation, incremental idle work, a C API, benchmarks, and
  differential tests. The subject explicitly discloses Codex and LLM help,
  including generated optimization and commit messages, while documenting
  extensive review and rewrites. Core implementation attribution is therefore
  shared rather than silently credited 100%.
- [`ghostty#13209`](https://github.com/ghostty-org/ghostty/pull/13209) diagnoses
  a POSIX PTY pipeline bottleneck across kernel queues and supplies A/B
  benchmarks plus independent Linux-user reproduction; the final code is
  described as hand-written and verified after an agent found the path.
  [`ghostty#13367`](https://github.com/ghostty-org/ghostty/pull/13367) implements
  error-safe terminal resize rollback/fallback semantics with broad tests; its
  disclosure limits AI assistance to judging and test help.
- [`coder/websocket#565`](https://github.com/coder/websocket/pull/565) removes
  per-frame allocation closures with benchmarks and upstream maintainer
  approval. Its disclosure says AI helped find and fix the issue while the
  subject understood and manually adapted it, providing an external attribution
  and validation trace independent of Ghostty.

E=94 follows `4.5 / 4.5 / 5 / 4.5 / 5`. The half-points retain shared
implementation, the absence of human approvals on the largest self-merged
Ghostty traces, and the fact that differential corpus/fuzz validation was added
only after the subject identified it as a pre-merge gap.

### Stewardship, impact, and trajectory

- [Ghostty CODEOWNERS](https://github.com/ghostty-org/ghostty/blob/main/CODEOWNERS)
  identifies the subject as current BDFL while delegating font, GTK, macOS,
  renderer, shell, and terminal subsystems to maintainer teams. Its
  [contributor guide](https://github.com/ghostty-org/ghostty/blob/main/CONTRIBUTING.md)
  defines contribution, AI-vouch, triage, and review processes. Tags from
  [v1.0.0 through v1.3.1](https://github.com/ghostty-org/ghostty/tags) show a
  sustained release lifecycle. Concentrated subject commits and frequent
  self-merge keep collaboration at 4 and S=91 from `5 / 4.5 / 4 / 4.5`.
- Ghostty is independently packaged across several operating-system
  repositories documented by its [installation guide](https://ghostty.org/docs/install/binary).
  Older, directly attributable initial commits for
  [Vagrant](https://github.com/hashicorp/vagrant/commit/050bfd9c686b06c292a9614662b0ab1bbf652db3),
  [Packer](https://github.com/hashicorp/packer/commit/9c22026293c937a45b269a938c7775def8544dea),
  and [Terraform](https://github.com/hashicorp/terraform/commit/649cf336e86da10910f6e50ea3cfaad507a2e336)
  support creation and durability baselines only. Current HashiCorp adoption,
  maintenance, and community work are not transferred to a former creator.
  I=92 uses `4.5 / 5 / 5 / 4 / 4 / 5`.
- T=93 from `5 / 4.5 / 4 / 5` captures the externally visible shift from
  Go infrastructure tools into Zig, terminal emulation, native macOS and GTK,
  rendering, PTYs, and subsystem governance. Explicit agent use shows an
  inspectable learning and verification process, but mostly self-reviewed work
  keeps independent validation and learning below their ceiling anchors.

[`ghostty#8442`](https://github.com/ghostty-org/ghostty/pull/8442) adds a
security confirmation before Finder/open executes scripts, but a user reported
that the friction caused them to leave and the discussion was later locked.
This is retained as a real security-versus-product trade-off, not treated as
unambiguous success. R=91 follows `4.5 / 4.5 / 5 / 4.5 / 4` within the named
terminal cohort. Reasonable intervals are E 89–96, S 84–94, I 86–95, T 86–97,
and R 84–94. Confidence is high for public artifacts; private usage, crash
telemetry, and undisclosed agent work remain unknown.

## `simonw`

- Role lens: SQLite data-publishing and Python LLM-tool/plugin ecosystem creator
  and maintainer.
- Capability interpretation: System owner ↔ Maintainer / technical leader
  boundary. The point estimate reaches the latter, while the low end of
  implementation attribution does not clear its E gate.
- R cohort: maintainers who combine SQLite data tooling, a Python plugin
  ecosystem, multi-provider LLM abstractions, release responsibility, and
  durable technical documentation. That intersection is too tailored for a
  reproducible supply sample. R is therefore formally `unknown`; the diagnostic
  frame uses public maintainers of Python database tools, model-provider
  abstraction libraries, and plugin-based developer tools, not only projects
  selected for resemblance to this subject.

### Engineering and AI attribution

- [`simonw/llm#996`](https://github.com/simonw/llm/pull/996) is a directly
  authored 2025 baseline for tool definitions, tool calls/results, chains,
  approvals, logging, async failure repair, types, tests, and documentation.
  [`datasette#2844`](https://github.com/simonw/datasette/pull/2844) independently
  diagnoses Python's SQLite context-manager semantics and proves atomic rollback
  and reader invisibility in threaded and zero-thread modes.
- The largest current changes have explicit agent attribution.
  [`simonw/llm#1411`](https://github.com/simonw/llm/pull/1411) is a third-attempt
  structured-message/parts and streaming-event redesign with many
  Claude-coauthored commits; the subject iterates the public Python API,
  exercises it against live providers, edits compatibility/docs, and decides
  the alpha boundary. [`datasette#2824`](https://github.com/simonw/datasette/pull/2824)
  begins from a public Fable session and contains Claude-authored API consistency
  changes reviewed inline by the subject. These support architecture, decision,
  validation, and S more strongly than direct implementation authorship.
- [`datasette#2689`](https://github.com/simonw/datasette/pull/2689) replaces
  token CSRF protection with Fetch Metadata/Origin checks, compatibility shims,
  bearer-token handling, tests, and upgrade guidance; its first commits are
  Claude-authored and later commits mix coauthorship and direct cleanup.
  [`sqlite-utils#795`](https://github.com/simonw/sqlite-utils/pull/795) is also
  Claude-authored from a linked session. No silent 100% implementation transfer
  is made for either.

E=85 follows `4 / 4.5 / 4.5 / 4 / 4`. The direct tools and transaction traces
establish independent technical depth; mixed implementation, owner-only review,
and correlated agent-generated API work keep the current engineering anchors
below the other five packets.

### Stewardship, impact, trajectory, and blind spots

- The subject publishes repeated [Datasette](https://github.com/simonw/datasette/releases)
  and [`llm`](https://github.com/simonw/llm/releases) releases, maintains
  compatibility and upgrade documentation, and owns long-running roadmaps.
  Review of external work such as
  [`sqlite-utils#634`](https://github.com/simonw/sqlite-utils/pull/634) catches
  optimized-mode `assert` behavior, while
  [`datasette-acl#51`](https://github.com/datasette/datasette-acl/pull/51)
  simplifies a contributor API. The two-year merged external-review sample is
  much smaller than the subject's authored/self-reviewed work, so collaboration
  is 3.5 and S=89 uses `5 / 5 / 3.5 / 4`.
- The official [Datasette plugin directory](https://datasette.io/plugins)
  listed 154 plugins at the snapshot, including independent owners and recent
  releases. At the snapshot, PyPIStats `last_month` telemetry reported about
  156,000 downloads for
  [`datasette`](https://pypistats.org/packages/datasette),
  409,000 for [`llm`](https://pypistats.org/packages/llm), and
  1.13 million for
  [`sqlite-utils`](https://pypistats.org/packages/sqlite-utils).
  Those counts corroborate continuing distribution but include CI and repeat
  installs.
  Plugin interfaces, independent extensions, releases, and durable
  documentation carry I=89 from `4.5 / 4.5 / 4.5 / 4 / 4.5 / 4.5`; the whole
  plugin ecosystem is not assigned to one author.
- T=87 from `4 / 3.5 / 5 / 5` reflects expansion from the established SQLite and
  publishing baseline into multi-provider model APIs, tools, resumable
  human-in-the-loop chains in [`llm#1482`](https://github.com/simonw/llm/pull/1482),
  and a transparent agent-driven engineering practice. High learning and scope
  do not erase lower direct-code attribution; the limited independent human
  review keeps external validation at 3.5.

The diagnostic R anchors `3.5 / 3 / 4 / 3 / 3.5` mechanically produce 68, but
R remains `unknown` because the role intersection and qualified-person sample
are not reproducible enough. Reasonable intervals are E 74–89, S 82–93, I
83–93, and T 78–91. E's lower bound crosses the Maintainer gate, so the packet
must disclose System owner as an adjacent band. Overall confidence is medium:
AI attribution is unusually transparent, but private production use,
independent incident outcomes, and undisclosed agent assistance remain unknown.

## Review and activation protocol

Before promoting a packet from candidate to active anchor:

1. Freeze the linked artifacts or record commit identifiers for every material
   score.
2. Have a second reviewer independently score a redacted evidence packet.
3. Record exact-anchor agreement, agreement within 0.5, and mean absolute
   anchor difference.
4. Resolve any one-point disagreement using evidence, then rerun band and
   sensitivity checks.
5. Version the activated packet against the rubric and retain this provisional
   snapshot for drift analysis.
6. Record assessment depth, source-inspection status, and source review packet
   identifiers for every source-dependent E score.
