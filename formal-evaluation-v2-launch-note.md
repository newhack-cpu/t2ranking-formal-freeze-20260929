# Formal evaluation v2 launch note

The first launch (`formal-evaluation-v1-20260929`) exited before label access
because its shell environment omitted the `formal-prep-v3` project root from
`PYTHONPATH`. It produced no result file and no qrels-derived metric. Its
stdout/stderr, lock, start, and exit receipts remain in the v1 directory on
the instance and are not overwritten.

The corrected, unique v2 release binds the same frozen inputs and code to a
new output path and adds the missing project-root import path:

- Manifest SHA-256: `90fac09021be2c21b48dc8387637e20341a98886275370d29c3b6821f4d9e59e4`
- Release directory: `formal-evaluation-v2-20260929`
- Output: `formal-evaluation-v2-20260929/output/evaluation.json`
- v1 pre-input failure is recorded in the v2 manifest and remains immutable.

The evaluation remains CPU-only and one-time for the v2 output path.
