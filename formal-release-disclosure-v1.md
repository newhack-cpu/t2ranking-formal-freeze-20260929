# Formal T2Ranking evaluation release v1

This release records the single, frozen CPU evaluation planned for the T2Ranking
development query list. It binds the formal manifest to the existing v2.2
protocol, the reviewed evaluator, and the already accepted candidate, CE-score,
allocation, and prediction releases. The result path is unique and the
evaluation must not be retried or overwritten after it starts.

- Manifest SHA-256: `61cc6fa1554f887b581dc1f0456085eeaca9a2bf275565a`
- Protocol SHA-256: `ace766cd01849a03370ab82876067f0bb3c289404b10938af15fb80951d23c75`
- Evaluator SHA-256: `6474ad094609f533a179b08571dfc9572b9df92218cfcac70e8015eb15264e46`
- Independent audit helper SHA-256: `22a05a5044fcebf2bda2ca82ecb52de028839f2ea96cae492e2ed4bf13701a1c`
- Formal output: `formal-evaluation-v1-20260929/output/evaluation.json`
- Runtime: Python 3.10.20, NumPy 2.2.6, SciPy 1.15.3, pytrec_eval 0.5.10;
  exact module/source-tree bindings are in the manifest.
- GPU: not required; this run is CPU-only on the one-core, 16-GiB instance.

## Sequencing disclosure

Before this final release, `qrels.dev.tsv` was read under the user's explicit
authorization for format, coverage, and hash verification. No effectiveness
metric, candidate utility, or formal result was computed from it during that
check. This sequencing deviation is disclosed rather than presented as a
perfectly unopened-label workflow. The final evaluator still performs its own
preflight, binds the qrels SHA, and reads qrels only inside the one-time
evaluation process.

The qrels bytes are bound to SHA-256
`a0356bd3c6d72c532ca17a4d88d7765554857f321346cf0f9cb4ad480738b25a`, matching
the archived T2Ranking data manifest source declaration.
