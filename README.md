# A Structural Theory of Reachability, Degrees of Freedom, and Irreversible Allocation  
## Architecture, Representation, and Human–Machine Systems

---

## Abstract

This document presents a **structural theory of reachability under irreversible allocation**.  
The theory applies across computational systems, software architectures, sensing, learning systems, and biological cognition.

The central claim is **architectural and conditional**:

> **For systems operating under bounded representational capacity and irreversible allocation, the set of computable or learnable distinctions is bounded by the remaining allocatable degrees of freedom. Once distinctions collapse irreversibly, future reachability is structurally foreclosed, independent of intelligence, optimization, or intent.**

The framework does not predict which futures matter, nor which distinctions will be required.  
It characterizes **what must remain structurally available for unknown distinctions to be representable at all**.

---

## 0. Scope and Status

This document is a **theory sketch**, not a design prescription.

It:
- identifies **necessary structural constraints**, not sufficient solutions,
- characterizes **irreversible failure modes**, not success guarantees,
- applies only **relative to stated goals** (e.g., long-horizon adaptability).

It explicitly does **not** claim:
- optimality,
- completeness,
- universality of goals,
- or foreknowledge of future tasks.

---

## 1. Core Assumptions

### 1.1 Bounded Representational Capacity

Any real system has:
- finite memory,
- finite state space,
- finite bandwidth,
- finite coordination capacity.

This applies to:
- CPUs,
- software ecosystems,
- learning systems,
- biological brains,
- institutions.

---

### 1.2 Irreversible Allocation

Some allocations of representational or architectural capacity are:
- locally irreversible,
- unrecoverable without global redesign,
- or require prohibitive coordination to undo.

Irreversibility may be:
- physical (hardware),
- informational (quantization, compression),
- organizational (interfaces, protocols),
- biological (developmental constraints).

---

### 1.3 Interface-Constrained Interaction

All action, learning, coordination, and redesign occur through interfaces that impose:
- bounded bandwidth,
- timing constraints,
- coupling and failure domains,
- limited extensibility.

Removing any of these assumptions invalidates the framework.

---

## 2. Reachability as an Architectural Property

### 2.1 Definition of Reachability

**Reachability** is the set of future states, distinctions, or interaction patterns that a system can host **without global redesign**.

Reachability is:
- structural, not semantic,
- architectural, not behavioral,
- defined by available degrees of freedom, not by intelligence or training.

---

### 2.2 Reachability-Preserving Architectures

A **Reachability-Preserving Architecture**:
- avoids premature irreversible allocation,
- preserves uncommitted representational capacity,
- defers collapse of distinctions to higher, more flexible layers.

This orientation is relative to **irreversibility**, not to time or scale.

---

## 3. Degrees of Freedom and Distinctions

### 3.1 Degrees of Freedom (DOFs)

Degrees of freedom correspond to:
- independent representational variables,
- dimensions of state space,
- allocatable axes for distinction.

They may be:
- discrete (bits, symbols),
- continuous (embedding dimensions),
- structural (routing paths, coordination channels).

---

### 3.2 Distinctions and Equivalence Classes

A **distinction** exists if and only if:
- two states can be mapped to different equivalence classes
- under the available representation and computation.

Labels are irrelevant.
Only **distinguishability under the architecture** matters.

When multiple states map irreversibly to the same class, a **collapse of distinctions** occurs.

---

## 4. Computation Does Not Create Distinctions

A fundamental invariant:

> **Computation transforms distinctions; it does not create them.**

If a distinction is not representable in the available state space:
- no algorithm can recover it,
- no learning can infer it,
- no intelligence can compensate for its absence.

This is a generalized form of the pigeonhole principle.

---

## 5. Deferred vs. Early Allocation

### 5.1 Early Allocation

Examples:
- fixed-width integers,
- rigid schemas,
- non-extensible protocols,
- early specialization in development.

Properties:
- predictable,
- efficient,
- bounded.

Cost:
- irreversible foreclosure of future distinctions.

---

### 5.2 Deferred Allocation

Examples:
- arbitrary-precision integers,
- embeddings instead of one-hot encodings,
- transitive dependency resolution,
- exploratory learning phases.

Properties:
- flexible,
- reachability-preserving,
- capacity-efficient.

Cost:
- overhead,
- uncertainty,
- delayed irreversibility.

Deferred allocation does not eliminate collapse; it **moves it outward**.

---

## 6. Transitivity as an Architectural Lever

### 6.1 Relations and Transitivity

Given a relation R:
- Reflexive: aRa
- Symmetric: aRb → bRa
- Transitive: aRb && bRc → aRc

Transitivity is not a law; it is a **policy choice**.

---

### 6.2 Dependency Systems

- Transitive dependencies ⇒ deferred allocation, hidden growth.
- Non-transitive dependencies ⇒ early allocation, explicit bounds.

Breaking transitivity bounds systems but forces early commitments.
Allowing transitivity preserves reachability but hides costs.

---

## 7. Learning Systems and Embeddings

### 7.1 One-Hot vs. Continuous Embeddings

- One-hot representations allocate one DOF per symbol.
- Embeddings reuse DOFs geometrically.

Embeddings:
- preserve reachability longer,
- encode equivalence classes via geometry,
- collapse distinctions softly instead of discretely.

They do not escape DOF limits; they **optimize DOF usage**.

---

### 7.2 Equivalence Without Labels

In embedding-based systems:
- meaning is topological,
- equivalence is defined by separability,
- labels are incidental.

A theory’s “truth,” for the system, is the partition of space it induces.

---

## 8. Hardware and Unary vs. Binary Representation

Unary systems:
- are computationally universal,
- exhaust representational capacity immediately,
- collapse reachability rapidly.

Binary systems:
- minimize irreversible allocation,
- preserve reachability logarithmically,
- are structurally optimal under irreversibility.

Universality is irrelevant without capacity efficiency.

---

## 9. Human Cognition as an Architectural System

### 9.1 Gray vs. White Matter (Structural View)

- Gray matter ≈ local computation
- White matter ≈ connectivity, coordination, integration

White matter provides:
- allocatable DOFs for recombination,
- routing capacity between modules,
- learning capacity for new domains.

It is architectural slack, not knowledge.

---

### 9.2 Development and Irreversibility

Early development allocates:
- timing-sensitive coordination,
- sensorimotor integration,
- large-scale connectivity.

These allocations are:
- globally coupled,
- costly to change,
- largely irreversible.

Later learning operates via:
- reuse,
- overlay,
- compensation,
not reclamation.

---

## 10. Relation Operators in Humans

Humans rely on a limited set of **structural relation operators**:

- Identity / equivalence
- Symmetry / role reversal
- Transitivity (gated)
- Part–whole composition
- Capability / affordance
- Absence / deviation detection

Disability or “extra” components are:
- mismatches between expected equivalence classes and instances,
- not semantic deficits,
- but architectural misalignments.

Accessibility is therefore an **interface problem**, not a moral abstraction.

---

## 11. Learning Is Not Garbage Collection

Human learning does not perform full DOF reclamation.

- Low-level coordination is not freed.
- High-level representations are reused.
- New skills layer over old ones.

Learning is constrained reallocation, not reset.

---

## 12. Core Theorem (Structural)

> **For any system operating under irreversible allocation, the set of computable, learnable, or expressible distinctions is exactly the set representable within its remaining allocatable degrees of freedom. Intelligence, optimization, and semantics cannot extend this set.**

This is a necessary condition, not a sufficiency claim.

---

## 13. Implications

- Architecture dominates capability.
- Intelligence cannot override structural limits.
- Early over-commitment forecloses futures.
- Slack is non-redundant when reachability matters.
- Inclusion requires architectural adaptation.

---

## 14. Conclusion

Viability under irreversibility is governed not by:
- cleverness,
- semantics,
- or optimization,

but by:
- what has been irreversibly allocated,
- what degrees of freedom remain,
- and which distinctions are still representable.

Systems that exhaust their allocatable capacity too early do not merely risk failure —  
they **structurally bound their future reachability**.

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)
