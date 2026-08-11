\# T015 — Repeated-Run Consistency — Series Environment



\*\*Specification:\*\* COMASTA v0.2-draft

\*\*Protocol:\*\* T015 — Repeated-Run Consistency

\*\*Series:\*\* Formal Preregistered Series 001

\*\*Planned Runs:\*\* 5

\*\*Observation Status:\*\* No T015 output observed at environment registration



\## Runtime



\*\*Codex CLI Version:\*\*



`codex-cli 0.147.0`



\*\*Model:\*\*



`gpt-5.6-sol`



\*\*Reasoning Effort:\*\*



`high`



\*\*Interface:\*\*



Codex CLI non-interactive execution



\*\*CODEX\_HOME:\*\*



`C:\\Users\\ASIR\\Desktop\\COMASTA-blind\\codex-clean`



\*\*AGENTS.md Present:\*\*



`False`



\*\*AGENTS.override.md Present:\*\*



`False`



\## Execution Controls



All five preregistered runs will use:



\- `--ephemeral`

\- `--ignore-user-config`

\- `--ignore-rules`

\- `--sandbox read-only`

\- `--skip-git-repo-check`

\- `model\_reasoning\_effort="high"`

\- `web\_search="disabled"`



No run will be repaired, normalized, discarded, replaced, or rerun because of an unexpected result.



\## Frozen Input



Canonical fixture SHA-256:



`C0C421C1DF8B57DA2445E7E65EE90681CDC6F6ADBE36850B65D20971ACFD1192`



Complete repeated-run input SHA-256:



`76C598DF5DE91C383CD384FFF9E0B30394FCB60401D4F6E65BFA1C17AC9BF143`



The complete input is copied byte-for-byte from the frozen `T003-B-run-002` input.



It will not be reconstructed or edited independently for individual T015 runs.



\## Preregistered Runs



\- T015-R001

\- T015-R002

\- T015-R003

\- T015-R004

\- T015-R005



Exactly these five formal runs will be executed.



No additional run will be added to improve apparent consistency.



Any later replication must be recorded as a separately identified replication series.



\## Command Template



```powershell

Get-Content -Raw .\\input.txt | codex exec --model gpt-5.6-sol --ephemeral --ignore-user-config --ignore-rules --sandbox read-only --skip-git-repo-check -c 'model\_reasoning\_effort="high"' -c 'web\_search="disabled"' -o .\\<RUN-ID>-raw.md -

