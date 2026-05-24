# 06 — The Quadratic Formula

## Prereqs
- 05-quadratic-factoring

## Enables
- 07-quadratic-variations

## What this node is

The quadratic formula solves `ax² + bx + c = 0` for any a, b, c. The AoPS treatment derives it by completing the square on the general form — the formula is not given, it is *proved*. This is a schema-heavy node: the derivation requires manipulating an equation with symbolic coefficients (a, b, c instead of numbers), which forces relational encoding rather than surface encoding. The discriminant `b² - 4ac` is introduced as the structural indicator of whether the equation has 0, 1, or 2 real solutions.

## Sources
- AoPS Vol. 1, Ch 6, §6.3 (pp. 56–58)

## Fluency-light node — schema only. See exercises below.

## Derivation rigor rubric

Exercise 1 (derivation) is graded against this rubric. A "complete" derivation must include **every** step, in order, with each algebraic move explicitly written:

1. Start: `ax² + bx + c = 0`. State a ≠ 0.
2. Divide both sides by `a`: `x² + (b/a)x + c/a = 0`. (Justify: dividing by a nonzero quantity preserves equality.)
3. Move constant: `x² + (b/a)x = -c/a`.
4. Identify the term needed to complete the square: half of `b/a` is `b/(2a)`; its square is `b²/(4a²)`. State this explicitly.
5. Add `b²/(4a²)` to both sides: `x² + (b/a)x + b²/(4a²) = b²/(4a²) - c/a`.
6. Factor the left as a perfect square: `(x + b/(2a))² = b²/(4a²) - c/a`.
7. Common-denominator the right: `= (b² - 4ac)/(4a²)`. Show the algebra.
8. Take square root of both sides: `x + b/(2a) = ±√(b² - 4ac) / (2a)`. (Note: `√(4a²) = 2|a|`; the ± absorbs the sign — justify briefly.)
9. Isolate x: `x = -b/(2a) ± √(b² - 4ac) / (2a) = (-b ± √(b² - 4ac)) / (2a)`.

**No step may be skipped or hand-waved.** If a move is non-obvious (e.g. step 7's common denominator, step 8's sign handling), it must be written out, not implied.

## Schema-building exercises

1. **Derive the formula.** Starting from `ax² + bx + c = 0`, derive the quadratic formula by completing the square. Do this without looking at the book or notes. Grade your derivation against the rubric above — every numbered step must appear explicitly. If you get stuck, identify exactly *which step* you're stuck on, then look up only that step. Repeat until you can write the derivation from scratch passing the rubric.
2. **The discriminant as a structure indicator.** Explain why `b² - 4ac > 0` gives two distinct real roots, `= 0` gives one repeated root, and `< 0` gives no real roots. Where in the derivation does `b² - 4ac` appear, and why does its sign determine the nature of the solutions?
3. **Completing the square on a specific equation.** Solve `2x² - 4x - 6 = 0` by completing the square (not by using the formula directly). Then verify with the quadratic formula. The two paths should produce the same answer — why is it useful to know both?
4. **Discriminant sign analysis — symmetric parameter.** For what values of `m` (positive, negative, or zero) does `x² + mx + 9 = 0` have exactly one real solution? Two? None? Express each as a condition on `m`. **Important:** check the case where `m` is negative. Plot the boundary values of `m` on a number line and label each region with the number of real solutions. Then verify by picking one `m` value from each region (including a negative one) and solving the resulting concrete quadratic.
5. **Discriminant sign analysis — asymmetric parameter.** For what values of `k` does `kx² + (k+2)x + 1 = 0` have exactly one real solution? Be careful: this is not a single-parameter problem at the surface — the coefficient of `x²` is also `k`. Two cases to handle: (a) `k = 0` (the equation degenerates — what does it become?), and (b) `k ≠ 0` (genuine quadratic; analyze the discriminant). Combine both cases for the full answer. State whether negative `k` values are valid solutions and verify with a concrete value.

## Metacog checks

- **Explanation**: Explain what "completing the square" means geometrically. Why is the term "completing" appropriate? What square is being completed?
- **Transfer**: For what values of k does `x² + kx + 9 = 0` have exactly one solution? Two solutions? No real solutions? Express your answer as conditions on k.
- **Connection**: How does the quadratic formula connect back to factoring (node 05)? Specifically: if `b² - 4ac` is a perfect square, what does that imply about the factorability of the quadratic over the integers?
