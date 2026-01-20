# LIMENWARD

**LIMENWARD v0.0.0** is a boundary primitive.

It does not decide.
It does not verify.
It does not witness.
It does not execute.

It enforces **transition discipline**.

LIMENWARD exists only at the threshold between states.

---

## Philosophy

Most failures occur *between* steps, not within them.

LIMENWARD exists to make transitions explicit, deliberate, and auditable.
It does not evaluate content.
It evaluates **whether passage is permitted**.

If a boundary matters, it must be guarded.

---

## What LIMENWARD Guards

LIMENWARD is invoked when something attempts to cross a boundary, including but not limited to:

* draft → final
* private → public
* uncommitted → committed
* unverifiable → verifiable
* observation → action

It answers one question only:

> **Is this allowed to cross, right now?**

---

## What It Enforces

LIMENWARD enforces *preconditions*, not outcomes.

Specifically:

* No ambiguity exists at the moment of transition
* Explicit intent or finality is present
* Forbidden states are blocked at the boundary

LIMENWARD does not judge correctness.
It judges **right to proceed**.

---

## What It Is Not

* Not a judge
* Not a verifier
* Not a witness
* Not an executor
* Not a safety mechanism

Anything that changes state is out of scope.

---

## Behavior

* Consumes context via `stdin`
* Refuses silent invocation
* Evaluates boundary conditions deterministically
* Emits exactly one verdict
* Appends allowed transitions to a ledger
* Exits immediately after evaluation

No retries.
No flags.
No configuration.

---

## Verdicts

LIMENWARD emits exactly one of the following:

* `ALLOWED` — the transition may proceed
* `DENIED` — the transition is blocked

The verdict concerns **permission**, not quality.

---

## Usage

LIMENWARD is never run alone.
It must guard a transition.

```sh
<transition-context> | ./limenward.sh
```

### Example

```sh
echo "ready for release" | ./limenward.sh
```

If all boundary conditions are satisfied:

```text
ALLOWED
```

If a boundary condition is violated:

```text
DENIED
```

---

## Contract

Once a verdict is emitted:

* The decision stands
* Responsibility transfers to the caller
* Circumvention is explicit, not accidental

LIMENWARD guarantees **clarity at the boundary**.

---

## Relationship to Other Artifacts

* **GUILLOTINE** — destroys state
* **IRREVOCULL** — judges output
* **ATTESTORIUM** — witnesses reality
* **VALIDEXOR** — verifies claims
* **LIMENWARD** — guards transitions

Each artifact is orthogonal.
None can replace another.

---

## Warning

Boundaries create accountability.

If you do not want to be responsible for crossing one,
do not invoke LIMENWARD.

---

## About

LIMENWARD is a minimal, deterministic boundary guard for irreversible systems.

If transitions do not matter, do not use it.
If they do, nothing else is sufficient.

---

## Responsibility Boundary

This software is provided under the MIT License.

The MIT License permits use, copying, modification, and redistribution of the code, but it does not provide assurance, certification, audit defense, operational guarantees, or liability coverage.

Use of this software in environments where failure, compliance, legal exposure, or irreversible decisions matter requires an accountable party.

The original maintainer is available for assurance, adaptation, and responsibility when such accountability is required.

Contact: contact@speedkit.eu

Authoritative signed records are issued separately and are not produced by the software.
