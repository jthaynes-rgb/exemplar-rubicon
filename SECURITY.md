# Security — goals until proven

Nothing in this file is a claim that the private suite is already secure. Every line is a **goal** until it has a sealed PASS with proof.

## Standing goals

| ID | Goal |
|----|------|
| G-KEY | Device keys are designed to be non-extractable (hardware-backed or non-exportable CryptoKey), never raw in durable plaintext stores |
| G-AUTH | Confirm / clear paths are designed to reject identity aliases as proof |
| G-PHRASE | Exactly one confirm-phrase checker in a codebase |
| G-EGRESS | Apps are designed for measurable zero unexpected egress under test |
| G-CSP | Web shells are designed with strict CSP (nonce scripts; no unsafe-inline) |
| G-AT-REST | Sensitive held lines are designed encrypted at rest |
| G-THREAT | A public threat model ships before any "we are secure" marketing copy |

## Public voice hygiene

- Never write LLC until that filing is real.
- Never put personal identifiers in suite or OS UI.
- Never treat feed bans as a reason to dump private trees public.

## Reporting

If you find a vulnerability in **public** material in this repository, open a private GitHub security advisory on this repo. Do not file issues that paste secrets.
