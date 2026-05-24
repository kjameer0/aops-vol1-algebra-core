# Diagnostic Answer Key — aops-vol1-algebra-core — 2026-05-21

---

## Node 01 — Linear equations

**1a.** `(2x + 1)/3 = (x - 4)/2`

Multiply both sides by 6 (LCM of 3 and 2):
`2(2x + 1) = 3(x - 4)`
`4x + 2 = 3x - 12`
`x = -14`

**1b.** `kx + 6 = 3x + k` → `kx - 3x = k - 6` → `x(k - 3) = k - 6`

So `x = (k - 6)/(k - 3)`, provided `k ≠ 3`.

When `k = 3`: left side becomes `3x + 6 - 3x - 3 = 3`, i.e. `0 = -3`. No solution — the coefficient of x vanishes but the constant equation is false (parallel lines, never equal).

Note: `(k - 6)/(k - 3)` can be rewritten as `1 + (-3)/(k-3)`, which approaches 1 as k → ∞.

---

## Node 02 — Absolute value

**2a.** `|3x + 2| = 11`

Case 1: `3x + 2 = 11` → `x = 3`
Case 2: `3x + 2 = -11` → `3x = -13` → `x = -13/3`

Solutions: `x = 3` or `x = -13/3`

**2b.** `|2x - 5| ≤ 9`

`-9 ≤ 2x - 5 ≤ 9`
`-4 ≤ 2x ≤ 14`
`-2 ≤ x ≤ 7`

Solution: `[-2, 7]`

**2c.** The interval `(-3, 7)` has center `(-3 + 7)/2 = 2` and radius `(7 - (-3))/2 = 5`.

So the inequality is `|x - 2| < 5`.

Verify: `|x - 2| < 5` → `-5 < x - 2 < 5` → `-3 < x < 7`. ✓

Construction method: for any bounded interval `(a, b)`, center = `(a+b)/2`, radius = `(b-a)/2`, inequality is `|x - center| < radius`.

---

## Node 05 — Quadratic factoring

**5a.** `3x² - 10x - 8`

AC method: `a·c = 3·(-8) = -24`. Need two numbers that multiply to `-24` and add to `-10`: those are `-12` and `2`.

`3x² - 12x + 2x - 8 = 3x(x - 4) + 2(x - 4) = (3x + 2)(x - 4)`

**5b.** `x² - 2x - 15 = 0`

Factor: need two numbers multiplying to `-15`, adding to `-2`: those are `-5` and `3`.
`(x - 5)(x + 3) = 0`
`x = 5` or `x = -3`

---

## Node 06 — Quadratic formula

**6a.** Derivation of the quadratic formula:

Start: `ax² + bx + c = 0`

Divide by a: `x² + (b/a)x + c/a = 0`

Move constant: `x² + (b/a)x = -c/a`

Complete the square — add `(b/2a)²` to both sides:
`x² + (b/a)x + (b/2a)² = (b/2a)² - c/a`

Left side is a perfect square:
`(x + b/2a)² = b²/4a² - c/a = b²/4a² - 4ac/4a² = (b² - 4ac)/4a²`

Take square root:
`x + b/2a = ±√(b² - 4ac) / 2a`

Solve:
`x = (-b ± √(b² - 4ac)) / 2a`

**6b.** `x² + mx + 4 = 0`. Discriminant = `m² - 4(1)(4) = m² - 16`.

- Exactly one real solution: `m² - 16 = 0` → `m = ±4`
- Two real solutions: `m² - 16 > 0` → `m² > 16` → `m < -4` or `m > 4`
- No real solutions: `m² - 16 < 0` → `-4 < m < 4`

---

## Node 07 — Quadratic variations

**7a.** `x⁴ - 13x² + 36 = 0`

Let `u = x²`. Then: `u² - 13u + 36 = 0`

Factor: `(u - 4)(u - 9) = 0` → `u = 4` or `u = 9`

Back-substitute:
- `x² = 4` → `x = ±2`
- `x² = 9` → `x = ±3`

Four solutions: `x ∈ {-3, -2, 2, 3}`

**7b.** `x² - 5x + 4 + 4/(x² - 5x) = 8`

Let `u = x² - 5x`. Then: `u + 4 + 4/u = 8`, so `u + 4/u = 4`.

Multiply by u: `u² + 4 = 4u` → `u² - 4u + 4 = 0` → `(u - 2)² = 0` → `u = 2` (double root).

Back-substitute: `x² - 5x = 2` → `x² - 5x - 2 = 0`
→ `x = (5 ± √33)/2`

Two real solutions.

Check `u ≠ 0`: `u = 2 ≠ 0` ✓ (so neither root is 0 or 5; the divide-by-u step was safe).

Note: the perfect-square reduction in u means this u-substitution collapses to a single value rather than fanning out — a nice pedagogical point about when the substitution doesn't double the solution count.
