# Seal design (schema-level)

## Purpose

Fingerprint each finished piece and record it on one unbroken timeline. Temporary work stays off the main timeline.

## Minimal seal record (design)

```text
seal_id:        opaque id
artifact_path:  relative path in the release tree
sha256:         hex digest of artifact bytes
prev_seal:      sha256 of previous seal record (or genesis)
contract_ref:   short name of the I CONFIRM / contract this closes
sealed_at:      ISO-8601 timestamp (operator locale labeled)
```

## Rules

1. One seal marks one finished piece — a series of locks, not one permanent life seal.
2. The last seal is the zero point drift rolls back to.
3. Public Releases ship a `SHA256SUMS` file covering every artifact in that cut.
4. Private ledger contents (operator history, personal notes, vault material) never belong in a public seal pack.

## Omni-Ledger (goal)

A hash-chained ledger of seals is designed so a stranger can verify continuity without reading private payloads. This repository publishes the **design**; a full production ledger is a separate product surface and is not dumped here.
