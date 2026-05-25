# 03 — Systems of Two Linear Equations

## Prereqs
- 01-linear-one-var

## Enables
- 04-word-problems

## What this node is

Two linear equations in two unknowns. The core insight is that each equation describes a line; a solution is an intersection point. AoPS teaches both substitution and elimination, but more importantly introduces the two degenerate cases — parallel lines (0 solutions) and identical lines (infinitely many) — and asks you to prove the general elimination algorithm holds symbolically. Fluency-heavy for the mechanics; the degenerate cases introduce the first real structural reasoning.

## Sources
- AoPS Vol. 1, Ch 3, §3.3 (pp. 19–21)
- AoPS Exercises 3-3 i–iv (p. 21)
- AoPS Example 3-9 (p. 21): solving non-linear system as linear by treating `√x` and `√y` as the variables

## Fluency exercises

1. Solve by elimination: `2x + 3y = -1` and `3x - 4y = 7`
2. Solve by substitution: `x + y = 3` and `x - y = 1`
3. Solve: `3x = 5 + 2y` and `2x - 2y = 7`
4. Solve: `0.1x + y = 3` and `0.5x - 3y = 7`
5. Attempt to solve: `2x - 4y = 7` and `x - 2y = 2`. What happens? What does it mean geometrically?

## Schema-building exercises

1. **General proof.** AoPS (p. 20) asks: given `a₁x + a₂y = a₃` and `b₁x + b₂y = b₃`, multiply the first by `-b₁` and the second by `a₁`, then add. What happens to x? Write the general solution for y and then for x. Under what conditions on the a's and b's does this fail? What geometric fact does that condition correspond to?
2. **Non-linear as linear.** Solve: `2√x + 4√y = 10` and `2√x - 3√y = 3`. (Treat `√x` and `√y` as the unknowns, solve, then square.) Explain why you can treat `√x` as a single variable here and what constraint that places on your final answers.
3. **Building from a solution.** Construct a 2×2 linear system whose unique solution is `(x, y) = (-1, 4)`. Now modify one equation so the system has infinitely many solutions. What algebraic relationship must the two equations satisfy for that to happen?
4. **Balance vs. cancel — applied to a system.** Solve: `(x + y)/2 = 3` and `1/x + 1/y = 5/6`. The first equation invites a "balance both sides by 2" move; the second invites clearing denominators by multiplying through by `xy` (a balance move, *not* a cancellation). Show every multiplier explicitly and label each step as either (a) balancing both sides by the same quantity or (b) simplifying a single expression by cancelling. State any domain restrictions introduced by the second equation. See the "balance vs. cancel" subsection of [01-linear-one-var.md](../nodes/01-linear-one-var.md) if the distinction is fuzzy.

## Metacog checks

- **Explanation**: Why does elimination work? Justify from first principles why adding a multiple of one equation to another doesn't change the solution set.
- **Transfer**: Three equations, two unknowns: `x + y = 5`, `2x - y = 4`, `x - 2y = 1`. Can all three be satisfied simultaneously? How would you check without solving all three pairs?
- **Connection**: How does the degenerate case (0 = 3 from elimination) connect to what you saw in node 01 — equations with no solution? What is structurally the same?
