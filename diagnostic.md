# Diagnostic — aops-vol1-algebra-core — 2026-05-21

## Purpose

Sample problems across the critical nodes of this module. Solve what you can without help. Skip what you can't. Your results show where the module's entry point and difficulty calibration need adjustment.

## Instructions

1. Time yourself loosely — note "easy / struggled / no idea" for each problem.
2. Do not look up answers or use any tools while solving.
3. Show your work — partial work on a problem you couldn't finish is useful data.
4. When done, fill in the Results table at the bottom and save the file as `diagnostic-results.md` in the module folder, then run `/learning-plan refine ~/claude-workspace/modules/aops-vol1-algebra-core`.

---

## Problems

### Node 01 — Linear equations: one variable

**1a. (Fluency)** Solve for x:
$$\frac{2x + 1}{3} = \frac{x - 4}{2}$$

**1b. (Schema)** You have the equation `kx + 6 = 3x + k` where k is a constant. Find x in terms of k. For what value of k does the equation have no solution? What happens algebraically at that value?


time: low effort: low

---

### Node 02 — Absolute value

**2a. (Fluency)** Solve: `|3x + 2| = 11`


**2b. (Fluency)** Solve: `|2x - 5| ≤ 9`


**2c. (Schema)** Write an absolute value inequality whose solution set is exactly `(-3, 7)`. Show how you constructed it — not just the answer.


---

### Node 05 — Quadratic factoring

**5a. (Fluency)** Factor completely: `3x² - 10x - 8`


**5b. (Fluency)** Solve by factoring: `x² - 2x - 15 = 0`


---

### Node 06 — Quadratic formula

**6a. (Schema — derivation)** Derive the quadratic formula by completing the square on `ax² + bx + c = 0`. Start from scratch — do not use the formula itself. Show every step.
- 0 = ax^2 +bx +c 
- 0 = ax^2 + bx + b^2/4a - b^2/4a + c
- extract a from all terms
- divide by a on both sides, eliminating a
- factorize x^2+bx/a b^2/4a^2 
- (x+b/2a)^2 = b^2/4a^2 - c
- solve for x
- x = (-b +- sqrt(b^2 - 4ac))/2a

**6b. (Schema — discriminant)** For what values of m does `x² + mx + 4 = 0` have exactly one real solution? Two real solutions? No real solutions? Express each as a condition on m.
- sqrt(m^2-16) is the discriminant
- if m = √16 there is 1 solution
- if m < √16 there are no solutions
- if m > √16 there are 2 solutions
---

### Node 07 — Quadratic variations (schema peak)

**7a.** Solve: `x⁴ - 13x² + 36 = 0`. Identify the substitution, show the quadratic in u, solve for u, then find all values of x.

**7b.** Solve: `x² - 5x + 4 + \frac{4}{x² - 5x} = 8`. (Hint: let `u = x² - 5x`.)

---

## Results template (fill in after solving)

| Node                    | Problem | Outcome                    | Notes |
| ----------------------- | ------- | -------------------------- | ----- |
| 01-linear-one-var       | 1a      | easy / struggled / no idea |       |
| 01-linear-one-var       | 1b      | easy / struggled / no idea |       |
| 02-absolute-value       | 2a      | easy / struggled / no idea |       |
| 02-absolute-value       | 2b      | easy / struggled / no idea |       |
| 02-absolute-value       | 2c      | easy / struggled / no idea |       |
| 05-quadratic-factoring  | 5a      | easy / struggled / no idea |       |
| 05-quadratic-factoring  | 5b      | easy / struggled / no idea |       |
| 06-quadratic-formula    | 6a      | easy / struggled / no idea |       |
| 06-quadratic-formula    | 6b      | easy / struggled / no idea |       |
| 07-quadratic-variations | 7a      | easy / struggled / no idea |       |
| 07-quadratic-variations | 7b      | easy / struggled / no idea |       |
