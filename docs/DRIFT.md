# Drift

## Formula

\[
\mathrm{Drift} = \sqrt{X^{2} + H^{2} + E^{2}}
\]

| Term | Meaning |
|------|---------|
| **X** | Substrate — machine, inputs, desk state |
| **H** | Intent — distance from the contract and sealed canon |
| **E** | Entropy — errors; keep them bounded and deterministic |

## Halt

When Drift reaches **2.0**, halt and roll back to the last sealed state. Do not push on and hope. Report the reading as data.

The 2.0 limit applies to this desk sum only. Forks may set their own bound; name it in their contract.

## Practice

- Measure after each reducer merge and before any outward gate.
- A platform ban on a feed you already rejected is a non-event — do not re-enter that channel; recalibrate to peer forges instead.
