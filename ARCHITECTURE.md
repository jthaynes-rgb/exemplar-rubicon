# Architecture

## Root contract

Before labour starts, state one clear contract:

- **Intent** — what the operator wants.
- **Done-when** — what counts as finished.
- **Not-allowed** — what must not happen.

If the intent cannot be stated in one sentence, stop. Do not start on a guess.

## Root · reducer · worker

```
Operator (I CONFIRM)
        │
        ▼
   Root / Seat Seven   ← holds intent; never invents confirmation
        │
        ▼
   Local bus           ← gated kinds only (vault, delete, net, dispatch, subprocess…)
        │
   ┌────┴────┐
   ▼         ▼
Reducers   Shell UI
(domain)   (windows)
   │
   ▼
Workers (small, pure, ≤ bounded token / context)
```

- **Root** owns the contract.
- **Reducers** split work by domain into pure tasks (same input → same result; no side effects outside the task).
- **Workers** receive only the inputs they need. The method travels; the owner's private files stay with the owner.

## Sovereign gate

Seats speak. Only the operator's own typed **I CONFIRM** acts.

Hold at the gate anything that:

- touches owned files or stores,
- starts a new process, or
- reaches outward (post, send, publish, upload, merge, deploy, spend).

No seat may say the phrase for the operator, infer it, or carry it from another task. One confirmation covers exactly what it names, once.

## Anti-dilution

- No placeholders marked done.
- No swallowed errors — name them where they happen.
- Nothing abstracted away that cannot be checked.
- Proven claims stay fact; unproven capabilities are **goals** ("is designed to…").
- Newest sealed canon wins on conflict.

## Local-first desk (design goal)

The desk is designed so that:

- work can run without a remote "brain" in the room,
- the bus is the only path for gated kinds,
- suite apps (notes, wire, command, coil bridges) plug in as windows over the bus — not as autonomous cloud actors.

Unproven hardware or egress claims stay goals until sealed with proof. See `SECURITY.md`.

## What peers can build from this

1. A root that refuses outbound work without an exact confirm phrase.
2. A drift check that halts at 2.0 (see `docs/DRIFT.md`).
3. A seal step that fingerprints finished artifacts (see `docs/SEAL.md`).
4. Reducers and workers that stay pure and inspectable.

Private product implementations are out of scope for this repository.
