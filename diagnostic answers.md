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
Answer steps:
1. multiply left by 2/2 and right by 3/3 (LCM)
2. multiply both sides by 6
3. solve for x
4. x = -14
**1b. (Schema)** You have the equation `kx + 6 = 3x + k` where k is a constant. Find x in terms of k. For what value of k does the equation have no solution? What happens algebraically at that value?
Answer:
- move all x's to left side
- extract x with distribution
- divide both sides by -3
- x = (-6 + k)/(k-3)
- k cannot be equal to 3 because x would be 0 making the answer undefined

time: low effort: low

---

### Node 02 — Absolute value

**2a. (Fluency)** Solve: `|3x + 2| = 11`
- removing || can yield -11 and 11
- solve for both x
- x = 3, x = -13/3

**2b. (Fluency)** Solve: `|2x - 5| ≤ 9`
- break into -9 and 9
- x <= 7, x >=-2

**2c. (Schema)** Write an absolute value inequality whose solution set is exactly `(-3, 7)`. Show how you constructed it — not just the answer.
- gap between -3 and 7 is 10
- absolute value has to encapsulate that many values, so output must be < 5
- |x| < 5 covers (-5,5)
- offset by 2 brings us to |x-2| < 5

---

### Node 05 — Quadratic factoring

**5a. (Fluency)** Factor completely: `3x² - 10x - 8`
- gd = c
- 3d + g = b
- d = (-10-g)/3
- 0 = g^2 +10g -24
- (g+12)(g-2)
- g = 2 guess
- 2(d) = -8
- d = -4
- 3(-4) + 2 = -10
- (3x+2)(x-4)

**5b. (Fluency)** Solve by factoring: `x² - 2x - 15 = 0`
- gd = -15
- g+d = -2
- (x-5)(x+3)

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
- 0 = u^2 - 13u +36
- use quadratic formula
- u = (13 +- sqrt(169 - 144))/2
- u = 9, 4

**7b.** Solve: `x² - 5x + 4 + \frac{4}{x² - 5x} = 8`. (Hint: let `u = x² - 5x`.)
- u + 4 + 4/u =8
- u + 4/u = 4
- u^2 - 4u + 4 = 0
- (u-2)^2 = 0
- (x^2-5x-2)^2 = 0
- 

---

## Results template (fill in after solving)

| Node                    | Problem | Outcome                    | Notes                       |
| ----------------------- | ------- | -------------------------- | --------------------------- |
| 01-linear-one-var       | 1a      | easy / struggled / no idea | easy                        |
| 01-linear-one-var       | 1b      | easy / struggled / no idea | easy                        |
| 02-absolute-value       | 2a      | easy / struggled / no idea | easy                        |
| 02-absolute-value       | 2b      | easy / struggled / no idea | easy                        |
| 02-absolute-value       | 2c      | easy / struggled / no idea | slightly struggled          |
| 05-quadratic-factoring  | 5a      | easy / struggled / no idea | easy                        |
| 05-quadratic-factoring  | 5b      | easy / struggled / no idea | easy                        |
| 06-quadratic-formula    | 6a      | easy / struggled / no idea | somewhat struggled          |
| 06-quadratic-formula    | 6b      | easy / struggled / no idea | easy                        |
| 07-quadratic-variations | 7a      | easy / struggled / no idea | fairly easy                 |
| 07-quadratic-variations | 7b      | easy / struggled / no idea | factored and did not finish |
