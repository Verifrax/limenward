# LIMENWARD

Primitive ID: PRIM-004  
Package: @verifrax/limenward  
Binary: limenward

Verifrax primitive — boundary enforcement primitive for deterministic irreversible systems.

---

## Status

Current release status: pre-stable primitive release line.

Canonical release target:

package version: 0.1.0  
tag: v0.1.0

LIMENWARD is part of the Verifrax primitive layer and follows the canonical primitive governance, naming, version, and packaging rules.

---

## Purpose

LIMENWARD enforces deterministic boundaries after origin, custody, and time have already been fixed.

Once an artifact has a stable origin, preserved custody, and explicit time boundary, the system still needs a deterministic threshold between what is inside the valid operating boundary and what is outside it. LIMENWARD exists to make that boundary explicit, enforceable, and non-ambiguous.

It does not establish origin. It does not preserve custody. It does not fix temporal order. It does not verify correctness. It does not witness, judge, or terminate. Its role is narrower: enforce boundary conditions for downstream interpretation and action.

---

## What This Primitive Does

- enforces a deterministic boundary surface around an artifact or state
- distinguishes in-boundary from out-of-boundary conditions
- emits boundary-governed output suitable for downstream primitives

---

## What This Primitive Does Not Do

- does not establish first origin
- does not preserve custody continuity
- does not fix temporal ordering
- does not verify correctness
- does not witness or attest
- does not judge validity
- does not terminate lifecycle

---

## Behavioral Contract

Invocation model:

executable: limenward  
package: @verifrax/limenward  
runtime: CLI-first

The primitive operates on an artifact whose origin, custody, and time surfaces are already fixed.

If the boundary conditions are absent, ambiguous, or non-deterministic, LIMENWARD must not fabricate a stable in-boundary result.

Exit codes:

0 — boundary enforcement completed successfully  
non-zero — invocation failed or contract violated

---

## Usage

Install:

npm install -g @verifrax/limenward

Execute:

limenward artifact.json

stdin example:

cat artifact.json | limenward

---

## Determinism Guarantees

For identical canonical input, LIMENWARD must produce identical boundary-enforcement output.

No hidden environmental state may influence the result.

LIMENWARD assumes an already-bounded origin, custody, and time surface and does not substitute for those earlier primitives or for downstream verification and judgment.

---

## Security Model

LIMENWARD protects against ambiguity in operational or semantic boundary enforcement.

Its security value is to prevent silent drift between allowed and disallowed states once prior primitive conditions are fixed. It does not guarantee correctness, attestation, or irreversible judgment.

---

## Relationship to Other Primitives

Canonical primitive order:

1 originseal  
2 archicustos  
3 kairoclasp  
4 limenward  
5 validexor  
6 attestorium  
7 irrevocull  
8 guillotine

Repositories:

https://github.com/Verifrax/originseal  
https://github.com/Verifrax/archicustos  
https://github.com/Verifrax/kairoclasp  
https://github.com/Verifrax/limenward  
https://github.com/Verifrax/validexor  
https://github.com/Verifrax/attestorium  
https://github.com/Verifrax/irrevocull  
https://github.com/Verifrax/guillotine

---

## Installation

npm install -g @verifrax/limenward

command -v limenward

Repository:
- GitHub: https://github.com/Verifrax/limenward
- Package: @verifrax/limenward
- Binary: limenward

---

## License

MIT
