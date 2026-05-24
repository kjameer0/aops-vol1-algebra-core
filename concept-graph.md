# Concept Graph — AoPS Vol. 1 Algebra Core

## Assumed prerequisites (outside this module)

- Variables and expressions (what a variable is, what a coefficient is)
- Distributive property: `a(b + c) = ab + ac`
- Basic arithmetic with fractions and negatives
- Cartesian coordinates and graphing points (needed for systems interpretation)

If any of these are weak, fix them first — a gap here silently breaks everything downstream (§12).

## Nodes

```
01 linear-one-var ──► 02 absolute-value
       │
       ▼
03 systems-two-var ──► 04 word-problems
       │
       ▼
05 quadratic-factoring ──► 06 quadratic-formula
                                    │
                                    ▼
                           07 quadratic-variations  ← schema-building peak
```

All of 01–06 are prerequisites for 07.

## Edge semantics

- `01 → 02`: absolute value equations split into two linear cases — you must solve those cases cleanly
- `01 → 03`: systems are solved by reducing to single-variable linear equations
- `03 → 04`: word problems often produce systems; you need both solution methods available
- `05 → 06`: the quadratic formula is derived by completing the square on the general quadratic — factoring fluency needed to recognize when *not* to use the formula
- `06 → 07`: variations use the formula as a tool; substitution requires you to recognize quadratic structure in disguise

## AoPS chapter map

| Node | AoPS Source |
|---|---|
| 01 | Ch 3, §3.1–3.2 (pp. 17–18) |
| 02 | Ch 21, §21.5.1 (pp. 191–192) |
| 03 | Ch 3, §3.3 (pp. 19–21) |
| 04 | Ch 3, §3.4 (pp. 22–27) |
| 05 | Ch 6, §6.1–6.2 (pp. 52–55) |
| 06 | Ch 6, §6.3 (pp. 56–58) |
| 07 | Ch 6, §6.4 (pp. 59–62) |

## Where fluency vs schema-building lives

- **Fluency-heavy**: 01, 02, 03, 05 — these need automaticity so working memory is free at 06–07
- **Schema-heavy**: 06, 07 — derivation, structure-recognition, and creative substitution

## Interleaving opportunities (§10)

Once 01–03 are stable, mix in single sessions:
- Solve linear / solve absolute value / identify system type — same manipulation toolkit, different constraints
- Factor / use formula / choose method — forces discrimination between when to factor vs. when to apply the formula
