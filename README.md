# Reachability Under Irreversible Allocation  
## A Structural Account of Representational Degrees of Freedom

---

## What This Document Is

This document presents a **structural description** of how representational degrees of freedom (DOFs) behave in systems with finite capacity and irreversible allocation.

It does not propose:
- optimal design strategies,
- preferred system goals,
- normative criteria such as adaptability or efficiency,
- or new physical or computational laws.

Its purpose is to make explicit a constraint that already exists—implicitly—across multiple domains:

> **Once representational capacity is irreversibly allocated, the set of distinctions a system can host is structurally constrained by the remaining addressable degrees of freedom.**

The contribution is **clarification and unification**, not discovery.

---

## What This Document Is Not

This document does **not** claim:
- that flexibility is superior to early commitment,
- that deferred allocation is generally desirable,
- that learning failures are inevitable,
- or that specific architectures are flawed.

Any preference for adaptability, efficiency, robustness, or coordination is **external to this framework** and must be supplied by downstream task requirements.

---

## Scope of Applicability

This framework applies to any system that satisfies all of the following:

- finite representational capacity,
- allocation of that capacity across independent DOFs,
- the existence of allocations that are costly or infeasible to reverse,
- operation and modification mediated by constrained interfaces.

Examples may include:
- computational systems,
- learning systems,
- hardware architectures,
- biological or cognitive systems,
- organizations or institutions,

but only insofar as these assumptions hold.

If any assumption fails, the framework does not apply.

---

## Core Assumptions

### 1. Finite Representational Capacity

Any realizable system has finite capacity to represent distinctions.

This includes limits on:
- memory,
- parameters,
- precision,
- bandwidth,
- coordination channels,
- addressable state.

Capacity may be large relative to a specific task, but it is never infinite relative to all possible distinctions.

---

### 2. Irreversible Allocation Exists

Some allocations of representational capacity cannot be freely undone.

“Irreversible” does not mean logically impossible to change.  
It means that reversal requires one or more of the following:

- global redesign,
- coordination across many components,
- loss of information elsewhere,
- external intervention beyond the system’s normal interfaces.

Irreversibility is defined **relative to the system’s own feasible resources**.

---

### 3. Interaction Is Interface-Constrained

All learning, optimization, adaptation, and redesign occur through interfaces.

Interfaces impose:
- bandwidth limits,
- latency,
- partial observability,
- coupling constraints,
- failure domains.

Self-modification and meta-learning are themselves mediated processes and consume representational capacity.

---

## Degrees of Freedom

A **degree of freedom (DOF)** is an independent axis along which a system can represent variation.

Examples include:
- bits or registers,
- embedding dimensions,
- parameters,
- routing paths,
- control channels,
- organizational roles.

Only **addressable DOFs** matter.  
Latent or inaccessible variation that cannot be acted upon through interfaces is structurally equivalent to nonexistence.

DOFs are the allocatable resource that determines which distinctions can be represented.

---

## Distinctions

A **distinction** exists if and only if:

- two states map to different equivalence classes
- under the system’s available representation and computation.

Semantics, labels, intentions, and interpretations are irrelevant.  
Only **architectural distinguishability** matters.

---

## Collapse of Distinctions

When multiple states are forced into the same equivalence class and this mapping cannot be reversed without irreversible cost, a **collapse of distinctions** occurs.

Once collapsed:
- the distinction is no longer representable,
- the distinction is no longer addressable,
- no internal process can exactly recover it.

Approximation, inference, or probabilistic substitution may occur, but this does not restore the original distinction.

---

## A Structural Constraint (Invariant)

> **Computation can transform and reallocate distinctions only to the extent that the underlying representation preserves sufficient independent degrees of freedom.**

If an irreversible many-to-one allocation has eliminated the information required to separate two states:
- no algorithm can recover that separation,
- no learning process can infer it,
- no increase in optimization power can compensate.

This constraint excludes the claim that optimization or learning can recover distinctions eliminated by earlier irreversible allocation, except where sufficient DOFs were preserved.

---

## Reachability

### Definition

**Reachability** is the set of distinctions a system can represent and act upon **without exceeding a given redesign cost threshold**.

Redesign cost may include:
- coordination bandwidth,
- migration effort,
- downtime,
- information loss,
- external intervention.

Reachability is therefore **graded**, not binary.

Optimization and learning operate **within** the currently reachable set.  
They may shift allocations among existing DOFs but cannot exceed structural limits imposed by irreversible commitments without incurring redesign cost.

---

## Allocation and Task Requirements

Allocation of DOFs is neither good nor bad in itself.  
It is a structural choice whose adequacy is determined by downstream task requirements.

### Example: Rigid Body Representation

Consider a task requiring precise representation of a rigid cube’s position and orientation.

- Fewer than **6 DOFs** are insufficient to uniquely represent pose.
- Exactly **6 DOFs** are sufficient and minimal for efficient pose tracking.
- More than **6 DOFs** may be required if the task also demands:
  - visualization attributes (color, mesh),
  - identifiers or namespaces,
  - uncertainty annotations,
  - interaction affordances.

In visualization systems (e.g., robotics tooling), additional DOFs are often allocated not for physical pose, but for auxiliary representational needs.

The framework does not privilege any choice.  
It only states that **once DOFs are allocated or foreclosed, the corresponding distinctions become reachable or unreachable accordingly**.

---

## Learning and Reallocation

Learning reallocates representational capacity among existing DOFs.

It may:
- refine partitions,
- compress representations,
- reuse structure,
- trade precision for coverage.

It does not:
- recreate eliminated DOFs,
- restore collapsed distinctions,
- bypass irreversible allocation.

Learning outcomes are therefore bounded by the structure it operates within.

---

## Scaling and Extension

Adding capacity later—through scaling or retrofitting—is itself an allocation decision.

Such changes:
- introduce new interfaces,
- consume coordination resources,
- incur migration costs,
- create new irreversibilities at a higher level.

Scaling can expand reachability **prospectively**, but it does not retroactively recover distinctions that were never preserved.

---

## Relation to Existing Theory

This constraint appears in different forms across domains:

- information theory (irreversibility, channel limits),
- learning theory (hypothesis class constraints),
- control theory (observability and controllability),
- computer architecture (fixed representations),
- biology (developmental specialization),
- organizations (path dependence).

Each addresses a projection of the same structural phenomenon.

This document makes the shared constraint explicit without domain-specific semantics.

---

## Non-Claims and Underspecification

This framework does not currently provide:
- a universal unit for remaining DOFs,
- a scalar measure of reachability,
- a complete design calculus.

Any operationalization will be domain-specific and approximate.

The framework is therefore **descriptive first**, not prescriptive.

---

## Summary

- Systems allocate finite representational degrees of freedom.
- Some allocations are costly or infeasible to reverse.
- These allocations determine which distinctions remain reachable.
- Computation and learning operate within, not beyond, these structural limits.
- Adequacy is determined by downstream task requirements, not by the framework itself.

---

## Status

This is a working structural note.

Its purpose is to clarify constraints, not to dictate goals.  
Any normative interpretation must be supplied externally.

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)
