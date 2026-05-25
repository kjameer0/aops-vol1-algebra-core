# 01 — Linear Equations: One Variable

## Prereqs
- Variables and expressions (external)
- Distributive property (external)
- Arithmetic with fractions and negatives (external)

## Enables
- 02-absolute-value
- 03-systems-two-var

## What this node is

A linear equation in one variable has degree one — no variable raised to a power other than 1, no products of variables. The AoPS treatment goes beyond mechanics: it introduces solving for a variable in terms of other constants (e.g. solve `ax + b = c` for x), and uses non-obvious manipulation to linearize equations that don't look linear at first (e.g. `1/y + 1 = 3y`). Fluency-heavy node — the goal is that single-variable manipulation becomes automatic so it doesn't consume working memory in harder problems.

## Clarification — balancing both sides vs. cancelling a denominator

Two operations look similar but do different things. Confusing them is how `x/x` on one side and `1/x` on the other can sneak into the same step and break an equation.

**Balancing both sides (legal everywhere).** Multiply both sides of an equation by the *same* nonzero quantity. The equality is preserved because you applied the same operation to two equal things. Use this when you want to clear a denominator from one or both sides.

> Example. `(x + 1)/2 = (x - 3)/4`. Multiply *both* sides by 4 (the same quantity on each side): `2(x + 1) = (x - 3)`. The denominators are cleared because the multiplier was chosen to cancel them — not because we "moved" them.

**Cancelling within a single fraction (a simplification, not a balance move).** `(kx)/x = k` (with `x ≠ 0`). Cancellation is just `a·b / a = b`. It happens *inside one expression*. It is not an operation applied to "the equation."

**The failure mode.** Multiplying the left side by `x/x` while multiplying the right side by `1/x` is two *different* multipliers — not a balance move at all. The result is not equivalent to the original equation.

**Rule of thumb.** Before manipulating a fraction in an equation, ask: am I (a) multiplying *both* sides by the same thing to clear denominators, or (b) simplifying a single expression by cancelling a common factor? If neither, the move is probably illegal.

## Sources
- AoPS Vol. 1, Ch 3, §3.1–3.2 (pp. 17–18)
- AoPS Exercises 3-1 and 3-2 (p. 18)

## Fluency exercises

1. Solve for y: `3y + 2 = y - 3 + 4y`
2. Solve for y: `y/3 - 3 = y`
3. Solve for x: `2(x - 4) = 3x + 1`
4. Solve for x: `(x + 1)/2 = (x - 3)/4`
5. Solve for x in terms of a, b, c: `ax + b = c` (constants a, b, c; a ≠ 0)

## Schema-building exercises

1. **Linearizing a non-linear equation.** Solve for y: `1/y + y = 2`. What algebraic move makes this tractable? Why does multiplying through by y work here but not always?
2. **Coefficient as variable.** You have `kx + 3 = 2x + k` where k is a constant. Find x in terms of k. For what value of k does the equation have no solution? Infinitely many? Explain why each case arises.
3. **Backwards construction.** Write a linear equation in one variable whose solution is x = -3/2 and that requires at least two steps to solve. Now write one that *looks* linear but has no solution. Explain the structural reason it fails.

## Schema-building answers
1. factoring a perfect square trinomial gets us (y-1)^2 = 0. this works because the original expression can be turned into a perfect sqaure to begin with. I need to look more closely for impossible answers in problems. 0 is not on the table as a solution here because y is in the denominator with no other terms to add to it. this helped me learn that there are multiple things being encoded in an equation, equality AND domain restrictions which I should check first to prevent adding wrong numbers to the solution set.
2. There are 0 solutions if there k = 2 because the denominator would be 0. this means that the two lines generated from the two sides of the equation would be parallel. there are no v1alues for which there are infinitely many solutions, because for there to be infinitely many the lines have to be the same. the slope of one side is always 2, and the the other side's m changes as k changes, so the 2 lines can never meet since they are still different lines when k = 2.
3. 2x + 3 = 0. you have to subtract 3 from both sides and then divide by 2 to isolate x. for the second equation: 3x + 1 = 3x + 2 looks linear but has no solutions because these two lines are never parallel.

## Metacog checks

Run these before advancing. Minimum bar: pass explanation and at least one of transfer or connection.

- **Explanation**: Why does "move the variable to one side and constants to the other" always work for linear equations? What property of equality justifies each step?
- **Transfer**: A classmate claims `2x + 3 = 2x - 5` has solution x = 0. Without solving, how do you know immediately that there's no solution?
- **Connection**: How does solving `ax + b = c` for x connect to what you'll do in node 03 (systems)? What is the same operation, just applied twice?

## Metacog check answers
1. Explanation: the addition property of equality justifies moving variables to one side of an equation and constants to another. Knowing the value of a variable(or acceptable values) is made easier by expressing that variable in terms of other constants. The addition property of equality(as well multiplication property of equality) allows us to shift linear equations as we see fit according to those rules to reword and equation into a more interpretable form
2. Transfer: whoever this person is is wrong because there are isolated constants that are unequal to each other, so if x is 0 then it won't change the fact that these values won't be affected by x and will be unequal.
3. Connection: systems of linear equations require expressing two separate equations in terms of the same variable to set them equal.