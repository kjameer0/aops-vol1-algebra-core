# Audit — aops-vol1-algebra-core — 2026-05-21

## Summary
- 0 errors, 3 warnings, 1 info

## Errors
None.

## Warnings

- [plan.yaml: node 02-absolute-value] `enables: [03-systems-two-var]` but `03-systems-two-var.prereqs` does not include `02-absolute-value`. Edge is one-sided. Either remove `02` from `enables`, or add `02` to `03`'s prereqs list. Current structure implies 02 unlocks 03 but 03 doesn't require 02 — likely the latter is correct (systems doesn't require absolute value). Recommend removing `03-systems-two-var` from `02`'s `enables` in `plan.yaml`, and removing the same from the node file.

- [nodes/06-quadratic-formula.md] No formal `## Sources` section. AoPS chapter reference appears in the "What this node is" body text but is not under a Sources heading. Violates node template. Add `## Sources` with the AoPS Vol. 1, Ch 6, §6.3 reference.

- [nodes/07-quadratic-variations.md] Same issue — AoPS chapter reference is in the body, not under a `## Sources` section heading. Add `## Sources`.

## Info / suggestions

- [nodes/02-absolute-value.md: Connection metacog] References §21.5.3 from AoPS (piecewise functions) — valid connection, but that section is outside the module's scope. The connection check would be stronger if it also named a node *within* the module (e.g. node 01 or 05). Consider adding a second connection prompt.
