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

Its purpose is to make explicit a constraint that already exists—implicitly—across multiple domains and has been encountered repeatedly in practice:

> **Once representational capacity is irreversibly allocated, the set of distinctions a system can host is structurally constrained by the remaining addressable degrees of freedom.**

The contribution is **clarification and alignment**, not discovery.

---

## How to Read This Document

This document does not argue for the existence of the constraint described here.  
It points to it.

The constraint has been encountered often enough that it is no longer informative to test it repeatedly through optimization, scaling, or refinement within a fixed representation.

If a reader wishes to verify its existence empirically, they are free to do so.

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
- communication protocols,
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
- migration or replacement,
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
- neurons or parameters,
- embedding dimensions,
- routing paths,
- message fields,
- control channels,
- organizational roles.

Only **addressable DOFs** matter.  
Latent or inaccessible variation that cannot be acted upon through interfaces is structurally equivalent to nonexistence.

DOFs are the allocatable resource that determines which distinctions can be represented.

---

## Already Formalized Degrees of Freedom (By Domain)

Degrees of freedom are not abstract or informal in most domains.  
They are already explicitly counted, bounded, and engineered around.

This framework does not introduce new DOFs.  
It aligns existing ones.

---

### Machine Learning

Formalized DOFs include:
- number of neurons,
- number of layers,
- embedding dimension,
- parameter count,
- activation precision,
- attention head count,
- context window length.

**Known wall:**  
A single linear neuron cannot represent XOR.  
No amount of learning, data, or optimization alters this.  
The only remedy is representational expansion.

---

### Information Theory and Digital Systems

Formalized DOFs include:
- number of bits,
- register width,
- address space size,
- channel capacity,
- entropy bounds.

**Known wall:**  
An *n*-bit register cannot represent more than 2ⁿ states.  
Once bits are overwritten or truncated, the original distinction is unrecoverable.

---

### Programming Languages and Runtimes

Formalized DOFs include:
- fixed-width integer ranges,
- stack size limits,
- heap size limits,
- pointer width,
- message size limits.

Deferred allocation (e.g., dynamically sized integers) preserves distinctions by routing representation through additional interfaces (heap, RAM), but introduces latency, coordination overhead, and unpredictability.

The cost is displaced, not eliminated.

---

### Networking and Communication Protocols

Formalized DOFs include:
- packet size limits (MTU),
- header field widths,
- sequence number ranges,
- window sizes,
- bandwidth constraints.

**Known wall:**  
A packet cannot carry more information than its payload allows.  
Lost or truncated packets do not reconstruct themselves.

Fragmentation and retransmission preserve reachability at the cost of coordination.

---

### Storage Systems

Formalized DOFs include:
- block sizes,
- page sizes,
- schema field widths,
- write-cycle limits (e.g., flash endurance).

**Known wall:**  
Once information is discarded or storage media wear out, recovery requires migration or replacement.

This is a physical constraint, not a design preference.

---

### Hardware Systems

Formalized DOFs include:
- RAM size,
- disk capacity,
- bus width,
- cache size,
- power budget.

A device cannot allocate more internal capacity than it physically contains.  
Expansion requires external intervention.

---

### Physical Space (Trivial but Instructive)

A refrigerator has fixed volume.

Shelves can be rearranged.  
Internal volume cannot be increased without replacing the appliance.

Reallocation is possible.  
Expansion requires redesign.

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

Approximation or inference may occur, but this does not restore the original distinction.

---

## A Structural Constraint

> **Given finite representational capacity and irreversible allocation, no sequence of internal operations can recover distinctions that were eliminated by earlier many-to-one allocation.**

If the information required to separate two states was not preserved:
- no algorithm can recover it,
- no learning process can infer it,
- no increase in optimization power compensates.

This is not a performance limitation.  
It is a representational boundary.

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

---

## Known Walls (Canonical Examples)

These failures are not hypothetical.

- A single linear neuron cannot represent XOR.
- A fixed-width integer cannot represent values outside its range.
- A lossy compression cannot be inverted without side information.
- A system that did not log a distinction cannot reconstruct it later.
- Centralized coordination cannot express decentralized autonomy without restructuring.

In each case, the only remedy is representational change.

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

Learning succeeds only when the relevant distinctions were implicitly preserved.

---

## Scaling and Extension

Adding capacity later is itself an allocation decision.

Such changes:
- introduce new interfaces,
- consume coordination resources,
- incur migration costs,
- create new irreversibilities at higher levels.

Scaling expands reachability prospectively.  
It does not retroactively restore eliminated distinctions.

---

## Relation to Existing Theory

This constraint appears across domains:

- information theory (irreversibility, channel limits),
- learning theory (hypothesis class constraints),
- control theory (observability and controllability),
- computer architecture (fixed representations),
- biology (developmental specialization),
- organizational theory (path dependence).

Each addresses a projection of the same structural phenomenon.

This document aligns them without domain-specific semantics.

---

## Summary

- Systems allocate finite representational DOFs.
- Some allocations are costly or infeasible to reverse.
- These allocations determine which distinctions remain reachable.
- Learning and optimization operate within these bounds.
- Expansion requires redesign, not effort.

---

## Status

This is a working structural note.

It points to constraints that already exist.  
It does not prescribe goals.

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)
