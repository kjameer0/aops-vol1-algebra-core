# 05 — Quadratic Equations: Factoring

## Prereqs
- 01-linear-one-var
- 04-word-problems (for applied context)

## Enables
- 06-quadratic-formula

## What this node is

A quadratic is a degree-2 polynomial equation. AoPS §6.1 starts by asking *what makes an equation quadratic*, not just how to solve it. Factoring works by writing `x² + bx + c = (x + p)(x + q)` and using the zero-product property: if a product equals zero, at least one factor is zero. The AoPS treatment includes AC-method for `ax² + bx + c` and recognizing special forms. Fluency-heavy — factoring must be automatic before completing the square or the quadratic formula will overwhelm working memory.

## Sources
- AoPS Vol. 1, Ch 6, §6.1–6.2 (pp. 52–55)

## Fluency exercises

1. Factor: `x² + 5x + 6`
2. Factor: `x² - 7x + 12`
3. Factor: `2x² + 7x + 3`
4. Factor: `x² - 9` (recognize the special form)
5. Solve by factoring: `x² - 3x - 10 = 0`

## Schema-building exercises

1. **Zero-product property from first principles.** The zero-product property says: if `ab = 0`, then `a = 0` or `b = 0`. Prove this using only the definition of multiplication and the property that 0 times anything is 0. Why does this property *not* hold for a product equal to some nonzero constant (i.e. why can't you split `ab = 6` into `a = 6` or `b = 6`)?
2. **Reverse engineering.** A quadratic has roots `x = 3` and `x = -5` and leading coefficient 2. Write the quadratic. Now generalize: given roots `r₁` and `r₂` and leading coefficient `a`, write the general form. What is the relationship between the roots and the coefficients `b` and `c` in `ax² + bx + c`?
3. **When factoring fails.** Try to factor `x² + x + 1` over the integers. Why can't you? What does this tell you about the roots? Connect this to when the quadratic formula will be needed (node 06).

## Metacog checks

- **Explanation**: Why does the factoring method for `x² + bx + c` require finding two numbers that multiply to `c` and add to `b`? Derive this from expanding `(x + p)(x + q)`.
- **Transfer**: Solve: `(x + 1)² = 4`. You can expand and factor, or you can take square roots directly. Show both approaches and explain when each is preferable.
- **Connection**: How does factoring connect to the roots of the equation graphically? What do the factors tell you about where the parabola `y = x² + bx + c` crosses the x-axis?
