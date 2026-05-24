# 07 — Quadratic Variations: Rearrangements and Substitution

## Prereqs
- 05-quadratic-factoring
- 06-quadratic-formula

## Enables
- (schema-building peak — no further nodes in this module)

## What this node is

The schema-building peak of this module. AoPS §6.4 shows that many equations which are not obviously quadratic can be reduced to standard quadratic form by algebraic rearrangement or substitution. The central technique: if an equation has the form `f(x)² + p·f(x) + q = 0` for some expression `f(x)`, substitute `u = f(x)`, solve the quadratic in u, then back-substitute. This requires recognizing quadratic structure in disguise — the hardest cognitive step in the module. Schema-heavy throughout.

## Sources
- AoPS Vol. 1, Ch 6, §6.4 (pp. 59–62)
  - §6.4.1 Rearrangements (p. 59)
  - §6.4.2 Substitutions (p. 60)

## Fluency-light node — schema only. See exercises below.

## Schema-building exercises

1. **Rearrangement.** Solve: `x⁴ - 5x² + 4 = 0`. Identify the substitution, solve for u, back-substitute, find all values of x. What is the structural feature that tells you this problem is "quadratic in disguise"?

2. **Substitution with a rational expression.** Solve: `x² + 1/x² - 3(x + 1/x) + 2 = 0`. Hint: let `u = x + 1/x`. Before solving, verify that `x² + 1/x² = u² - 2`. Why is this identity true? Solve for u, then solve for x. How many total solutions are there?

3. **Construction and transfer.** Create your own equation that is quadratic in some substituted expression `u = f(x)`. Write it in disguised form, solve it yourself, then describe the structural signal that reveals the substitution. What features should a solver look for when deciding whether substitution applies?

4. **Substitution unwinding — asymmetric u → x.** Solve completely: `x² - 5x + (4 / (x² - 5x)) = 3`. Use `u = x² - 5x`. Once you have values for `u`, you must back-substitute and solve the resulting equations *fully* for `x` — do not stop at `u`. For each `u` value, the equation `x² - 5x = u` is itself a quadratic in `x`; finish it. State the total number of `x` solutions, including any that come out irrational. **Self-check:** if your final answer for `x` still contains `u`, or if you wrote something like `(x² - 5x - c)² = 0` as a final answer, you stopped one step early — go back and finish.

5. **Substitution unwinding — verify before unwinding.** Solve: `(x² + 3x)² - 14(x² + 3x) + 40 = 0`. Identify the substitution. After finding the values of `u`, write out the *two separate quadratics in x* you need to solve. Solve each one fully via the quadratic formula. Then verify one of your final `x` values by plugging it back into the original equation — not into the u-equation. Why is plugging back into the original (rather than the u-equation) the stronger check?

## Metacog checks

- **Explanation**: Why does the substitution `u = f(x)` preserve the solution set (i.e. why are the solutions to the u-equation related to the solutions to the original x-equation)? What step could introduce extraneous solutions, and when must you check?
- **Transfer**: Solve `(x² - x)² - 8(x² - x) + 12 = 0`. Identify the substitution without being told what it is.
- **Connection**: How does this node connect to node 03 (systems)? In §3.3, AoPS solves `2√x + 4√y = 10` by treating `√x` and `√y` as the unknowns — what is that, if not substitution? Name the structural principle that unifies both techniques.

## Notes

This is the payoff node. If working memory is still occupied by mechanics (factoring slowly, forgetting how to apply the quadratic formula), the substitution step will be invisible. That is the signal to return to nodes 05–06 for more fluency work before attempting 07.
