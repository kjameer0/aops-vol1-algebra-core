# Refine log

## 2026-05-21 — sources: audit

### Applied
- `plan.yaml` + `nodes/02-absolute-value.md`: removed one-sided `enables: [03-systems-two-var]` edge — systems does not require absolute value as a prereq; edge was spurious
- `nodes/06-quadratic-formula.md`: added `## Sources` section with AoPS Vol. 1, Ch 6, §6.3 reference
- `nodes/07-quadratic-variations.md`: added `## Sources` section with AoPS Vol. 1, Ch 6, §6.4 reference
- `nodes/02-absolute-value.md`: strengthened Connection metacog check to include an in-module reference (node 01) alongside the out-of-module §21.5.3 reference

### Surfaced (user decision required)
None.

### Recommended follow-ups
- Run `/learning-plan audit ~/claude-workspace/modules/aops-vol1-algebra-core` to confirm 0 warnings
- Then run `/learning-plan diagnose ~/claude-workspace/modules/aops-vol1-algebra-core`

---

## 2026-05-24 — sources: diagnostic

### Applied
- `plan.yaml`: rewrote `learner_state` from outdated CK12 baseline to reflect diagnostic findings (nodes 01/02/05 solid, gaps on discriminant sign analysis and substitution unwinding, derivation rigor below AoPS)

### Surfaced (user decision required)
1. **Calibration of nodes 01, 02, 05** — diagnostic shows fluency at these nodes is trivial. Options:
   a. Compress: keep nodes but reduce `fluency_spec.count` (e.g. 10 → 4) as quick warm-up only
   b. Rebuild at AoPS rigor: change `fluency_spec.difficulty` from `algebra-1` to a higher level (e.g. `aops-vol1`) and regenerate worksheets
   c. Remove from module: skip these nodes; move entry point forward to 04 or 05
2. **Entry-point shift** — should the module's entry node be 01, or should it move to 04/05/06? Depends on (1).
3. **New schema exercises on Node 06 — discriminant sign cases.** Refine won't auto-write schema content. Want me to draft 2–3 parametric-discriminant exercises (with negative-parameter cases) for you to review and add?
4. **New schema exercises on Node 07 — substitution unwinding.** Same — want me to draft 2–3 exercises emphasizing the substitute-back step (asymmetric u → x)?
5. **Derivation rigor on Node 06a** — add an explicit rubric to the node file describing "complete" derivation steps (no skipped algebra, justifications for each move)?

### Recommended follow-ups
- Resolve the 5 surfaced items above, then re-run refine to apply
- After calibration changes: existing worksheets will be marked stale; will need regeneration on next `schedule`
- Then `/learning-plan audit` to confirm, then `/learning-plan schedule` (or `reschedule` if a schedule already exists)

---

## 2026-05-24b — sources: user decisions on surfaced items

### Applied
- **(1) Compress.** `plan.yaml`: reduced `fluency_spec.count` on nodes 01, 02, 05 from 10/10/12 → 4 each. Comment on each line records the reason and date. Difficulty kept at `algebra-1` (warm-up tier).
- **(2) Entry point unchanged** — stays at 01-linear-one-var.
- **(3) Node 06 — discriminant sign exercises added.** Added schema exercises 4 and 5 to `nodes/06-quadratic-formula.md`:
  - Ex 4: symmetric parameter, forces examination of negative `m` (directly targeting the diagnostic gap).
  - Ex 5: asymmetric parameter — coefficient of `x²` is also the parameter, forcing degenerate-case handling (`k = 0`) plus discriminant analysis.
  - Bumped `schema_exercises: 3 → 5` in `plan.yaml`.
- **(4) Node 07 — substitution unwinding exercises added.** Added schema exercises 4 and 5 to `nodes/07-quadratic-variations.md`:
  - Ex 4: explicitly calls out the failure mode from the diagnostic (`(x² - 5x - c)² = 0` as final answer) and tells the learner to finish.
  - Ex 5: forces writing out the two separate quadratics in x after the u-step, and back-substitution into the *original* equation as the strong check.
  - Bumped `schema_exercises: 3 → 5` in `plan.yaml`.
- **(5) Node 06 — derivation rigor rubric added.** New "Derivation rigor rubric" section in `nodes/06-quadratic-formula.md` with 9 numbered steps that exercise 1 must satisfy. Exercise 1 prompt updated to reference the rubric.
- **Cleanup:** removed duplicate `## Sources` sections in `nodes/06-quadratic-formula.md` and `nodes/07-quadratic-variations.md` (audit-level cleanup discovered while editing).

### Surfaced (user decision required)
None.

### Recommended follow-ups
- No pre-generated worksheets existed in `nodes/*/`, so no stale-marking was needed. New worksheets will be produced on first `schedule` run from the updated `fluency_spec` counts.
- Run `/learning-plan audit "/Users/khalidjameer/Documents/Obsidian Vaults/Personal Vault/aops-vol1-algebra-core"` to confirm 0 errors / 0 warnings on the edited structure.
- Then `/learning-plan schedule "<module>"` to set cadence and generate worksheets + `.ics`.

---

## 2026-05-24c — sources: logs (session-01)

### Applied
- **Session-log template (`templates/session-log.md`):** added a brief description to each marginal-gains dimension so raters know what each row measures (resolves session-01 issue 1).
- **Session-log template:** added an `**Expected duration:**` header field above the actual `Duration:` field, so each log captures the planned vs. actual session length (resolves session-01 issue 2).
- **`subcommands/complete.md`:** updated the pre-fill step to populate `Expected duration` from `cadence.minutes_per_session` when generating future session log files.

### Surfaced (user decision required)
None. Session-01 log left as-is (issues were template-level and only affect future logs).

### Recommended follow-ups
- Future `/learning-plan complete` runs will emit logs with the new fields populated. No reschedule needed.

---

## 2026-05-25 — sources: logs (session-02)

### Applied
- **Combined sessions split into fluency + schema** to keep the 30-min target honest (session-02 ran 3.3x expected).
  - Old session 03 (node-combined, 02-absolute-value) → new sessions 03 (fluency) + 04 (schema)
  - Old session 09 (node-combined, 05-quadratic-factoring) → new sessions 10 (fluency) + 11 (schema)
  - Old session 02 (node-combined, 01-linear-one-var) was already completed and stays combined (one-off).
  - Net: 14 → 16 sessions. End date moves from 2026-07-06 → 2026-07-13 (Mon).
  - `plan.yaml`: sessions list rewritten with new ids and types. Cadence-block comment added.
  - `schedule/sessions.md` and `schedule/learning-plan.ics`: regenerated with new sequence and dates. Existing UIDs reused (Calendar updates events in place; content shifts for renumbered slots).
  - `schedule/logs/session-03.md` header updated from `node-combined` → `node-fluency`.
- **"Balance vs. cancel" clarification added to `nodes/01-linear-one-var.md`.** New subsection between "What this node is" and "Sources" distinguishing (a) multiplying both sides of an equation by the same quantity from (b) cancellation inside a single fraction. Worked example shows the exact failure mode from the session-02 log (multiplying one side by `x/x` and the other by `1/x`).
- **New schema Ex 4 added to `nodes/03-systems-two-var.md`** targeting the same distinction — solving a 2-equation system where one equation invites a balance move and the other a denominator-clearing move. Forces explicit labelling of each step as balance vs. cancel and surfacing of domain restrictions. Includes pointer back to the node-01 subsection.
- `plan.yaml`: `03-systems-two-var.schema_exercises: 3 → 4` (with dated comment). Session 06 (new id) activities reference the new Ex 4 and the pre-read of the node-01 subsection.

### Surfaced (user decision required)
None remaining.

### Recommended follow-ups
- Re-import `schedule/learning-plan.ics` into Calendar (open command at end of complete-run handles this).
- No worksheets marked stale — `fluency_spec` counts didn't change for any node; the +1 on `03-systems-two-var` is a schema exercise, not fluency.
- Watch session-03 duration vs. expected to confirm the split helps.
