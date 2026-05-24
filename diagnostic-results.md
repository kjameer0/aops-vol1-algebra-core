# Diagnostic Results — aops-vol1-algebra-core — 2026-05-24

Source: learner-completed `diagnostic answers.md` (renamed/copied to this file for `refine` consumption).

## Results table

| Node                    | Problem | Outcome        | Notes                                            |
| ----------------------- | ------- | -------------- | ------------------------------------------------ |
| 01-linear-one-var       | 1a      | easy           | x = -14, correct                                 |
| 01-linear-one-var       | 1b      | easy           | x = (k-6)/(k-3), correct. Reasoning slip: said "x=0 makes it undefined" — actual issue is denominator = 0 / division by zero when k=3. Mathematical precision-of-language gap. |
| 02-absolute-value       | 2a      | easy           | x = 3, -13/3, correct                            |
| 02-absolute-value       | 2b      | easy           | -2 ≤ x ≤ 7, correct                              |
| 02-absolute-value       | 2c      | struggled      | Got \|x-2\| < 5, correct, but slightly struggled constructing it |
| 05-quadratic-factoring  | 5a      | easy           | (3x+2)(x-4), correct                             |
| 05-quadratic-factoring  | 5b      | easy           | (x-5)(x+3), correct                              |
| 06-quadratic-formula    | 6a      | struggled      | Reached the formula but derivation steps were sloppy / not AoPS-rigorous (skipped intermediate algebra, dropped factoring step) |
| 06-quadratic-formula    | 6b      | **WRONG (rated easy)** | Wrote m = √16 (one), m < √16 (none), m > √16 (two). Missed the negative case entirely — should be m = ±4 (one), \|m\| > 4 (two), \|m\| < 4 (none). **Real conceptual gap on discriminant sign analysis.** |
| 07-quadratic-variations | 7a      | easy           | u = 9, 4 correct, but didn't unwind to x = ±2, ±3 |
| 07-quadratic-variations | 7b      | did not finish | Got (u-2)² = 0, u = 2, then wrote (x²-5x-2)² = 0 — incorrect unwinding. Should be x²-5x = 2 → x²-5x-2 = 0 → x = (5±√33)/2. **Substitution-unwinding gap.** |

## Summary

**Overall calibration:** module is too easy at the `algebra-1` level recorded in `plan.yaml`. The `learner_state` premise (CK12-level) is outdated — most fluency-tier problems on nodes 01, 02, 05 were trivial.

**Genuine weak spots discovered (despite the "easy" ratings on the surface):**

1. **Discriminant sign reasoning (Node 06).** Treats m as if it were nonneg; misses symmetric/negative root cases.
2. **Substitution unwinding (Node 07).** Can identify u-substitution and solve in u, but fails to substitute back and finish solving for x cleanly.
3. **Derivation rigor (Node 06).** Reaches correct results but steps are sketchy — not at AoPS rigor standard.
4. **Mathematical precision of language (Node 01b).** Confuses "x = 0" with "denominator = 0 / division by zero."

## Recommendations for refine

- **Calibration:** raise difficulty across nodes 01, 02, 05 from `algebra-1` to `aops-vol1` (or compress these nodes into brief review rather than full study sessions).
- **Content additions:**
  - Node 06: add targeted schema exercises on **discriminant sign cases** (parametric quadratics where the parameter can be negative).
  - Node 07: add targeted schema exercises on **substitution unwinding** (solve in u, then return to x to completion, including non-symmetric u → x relationships).
  - Node 06: demand step-level rigor on derivation exercises; possibly add a rubric for what counts as "complete" derivation steps.
- **Entry-point review:** consider whether nodes 01, 02 should be entry points at all, or whether the module should start at 05/06.
- **Update `learner_state` in `plan.yaml`** to reflect actual level (no longer CK12-baseline).
