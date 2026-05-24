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
