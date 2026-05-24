# 02 — Absolute Value Equations and Inequalities

## Prereqs
- 01-linear-one-var

## Enables
- (terminal in this branch — absolute value is a standalone remediation node)

## What this node is

Absolute value is a function that returns the distance from a number to zero. The key solving technique is case-splitting: `|M| = N` becomes `M = N` OR `M = -N`. For inequalities, `|M| < N` becomes `-N < M < N` (interior of the V); `|M| > N` becomes `M < -N` OR `M > N` (exterior). The precision gap identified in diagnosis lives here — the learner understands the V-shape conceptually but drops arithmetic precision during case-solving. This node is the direct remediation. Fluency-heavy.

## Sources
- AoPS Vol. 1, Ch 21, §21.5.1 (pp. 191–192)
- AoPS Exercise 21-20 (p. 192): why `|x - y| < 2` means x and y are less than 2 apart
- AoPS Exercise 21-22 (p. 192): solve `|(x + 2)/(3x - 1)| = 5`

## Fluency exercises

1. Solve: `|2x - 3| < 7` (this was the diagnostic problem — work it completely, showing the chain of inequalities)
2. Solve: `|x + 4| = 9`
3. Solve: `|3x - 1| = |x + 5|`
4. Solve: `|x - 2| > 5`
5. Solve: `|2x + 1| ≤ 0` (think before computing — when can an absolute value be ≤ 0?)

## Schema-building exercises

1. **Geometric interpretation.** `|x - 3| < 5` describes all x within distance 5 of 3 on the number line. Restate `|x - a| < r` in plain English. Now: what does `|x - 3| + |x - 7| < 6` describe? Is it the same structure? Can you solve it? (Hint: think geometrically before algebraically.)
2. **Case analysis gone wrong.** A student solves `|2x - 3| < 7` and gets the answer `(3, 7)`. Reconstruct the error — what algebraic step did they skip or mis-execute? Write out the correct solution with every step justified.
3. **Constructing from constraints.** Write an absolute value inequality whose solution set is exactly `(-1, 5)`. Then write one whose solution set is `x ≤ -2 OR x ≥ 8`. How does the form of the solution set (bounded interval vs. two rays) determine whether you use `<` or `>`?

## Metacog checks

- **Explanation**: Why does `|M| = N` split into two cases? What property of absolute value forces you to consider both `M = N` and `M = -N`?
- **Transfer**: Solve `|x² - 4| = 5`. Does the case-splitting technique still work here? What's different about the cases?
- **Connection**: How does case-splitting in absolute value connect to (a) the piecewise definition of `|x|` (AoPS §21.5.3) and (b) solving for two linear cases in node 01? What is the same algebraic operation in all three, just triggered by different conditions?

## Notes

The diagnostic showed the learner solved `|2x - 3| < 7` as `(3, 7)` rather than `(-2, 5)`. The error is almost certainly failing to solve `-7 < 2x - 3` correctly (adding 3 to get `-4 < 2x`, then dividing by 2 to get `-2 < x`). Do fluency exercise 1 first, write every step, and check against the correct answer before moving on.
