# Formal Relational Constraint Substrate

## Projection-Relative Distinguishability, Constraint-Typed Transformations, Recoverability, and Composable Interaction

---

# Status

This document is a formal companion to the conceptual document:

```text
Relational Constraint Substrate
```

The purpose of this document is narrower.

It attempts to turn the conceptual vocabulary into a minimal formal scaffold.

It is not yet a complete mathematical theory.

It is a typed formalization intended to make explicit:

```text
what the primitives are
how distinctions are defined
how constraints act
how transformations compose
how recoverability is measured
when interaction exists
when organization becomes possible
```

The central revision is:

> Distinction is not treated as absolute. Distinction is defined as distinguishability under a projection, measurement, decoder, or use-context.

In compressed form:

> A substrate supports interaction when projection-distinguishable states are coupled by constraint-typed transformations that preserve recoverable structure across composition.

---

# Abstract

The conceptual framework proposed that reality supports interaction when distinguishable states are embedded in relation structures that constrain how transformations propagate, compose, and remain recoverable.

This formal companion replaces the primitive notion of `distinction` with:

```text
distinguishability under projection Π at resolution ε
```

and replaces informal recoverability with:

```text
recoverability by decoder Δ over horizon H at cost C with error ≤ ε and probability ≥ p
```

The framework is built around a typed substrate:

```text
S = (X, Π, R, K, T, Δ, μ)
```

where:

```text
X  = state space
Π  = projection or measurement family
R  = relation structure over projected states
K  = constraint regime
T  = admissible transformation family
Δ  = decoder or recovery family
μ  = cost, probability, or distortion measure
```

The core question is not:

```text
What objects exist?
```

but:

```text
Which distinctions are recoverable under which projections, transformations, constraints, horizons, costs, and decoders?
```

In compressed form:

> Objects, memory, cause, computation, affordance, and organization are derived from recoverable distinction under constrained transformation.

---

# 0. Orientation

Let:

```text
W
```

represent a world, physical system, environment, substrate, model universe, or bounded domain.

Let:

```text
X
```

represent the state space of `W`.

Let:

```text
x, y, z ∈ X
```

represent states.

Let:

```text
Π = {π_i}
```

represent a family of projections, sensors, measurements, interpretations, feature maps, decoders, or model views:

```text
π_i : X → Y_i
```

Let:

```text
ρ_i : Y_i × Y_i → ℝ_{0}
```

represent a distance, divergence, distinguishability, or decision metric in projected space.

Let:

```text
ε_i > 0
```

represent the resolution threshold for projection `π_i`.

Let:

```text
K
```

represent a constraint regime.

Let:

```text
T_K ⊆ X × X
```

represent the transition relation admissible under `K`.

Let:

```text
A_K(x)
```

represent the reachable set from state `x` under `K`.

Let:

```text
Δ
```

represent a decoder, recovery procedure, inverse estimator, reconstruction rule, or use-context procedure.

Let:

```text
H
```

represent a finite horizon.

Let:

```text
c
```

represent cost.

Let:

```text
p
```

represent probability of successful recovery.

The central formal question is:

```text
Given S = (X, Π, R, K, T, Δ, μ),
which distinctions are preserved, recoverable, composable, and operationally relevant?
```

In compressed form:

> Formal analysis begins with projection-relative distinguishability and asks which transformations preserve it well enough for future use.

---

# 1. Projection-Relative Distinguishability

## 1.1 Definition

Two states `x, y ∈ X` are distinguishable under projection `π_i` at resolution `ε_i` when:

```text
Dist_{π_i, ε_i}(x, y) ⇔ ρ_i(π_i(x), π_i(y)) > ε_i
```

If:

```text
ρ_i(π_i(x), π_i(y)) ≤ ε_i
```

then `x` and `y` are indistinguishable under projection `π_i` at that resolution.

Thus distinction is not absolute.

It is indexed by:

```text
projection
resolution
metric
noise model
use-context
```

In compressed form:

> A distinction exists operationally only relative to a projection that can separate states above threshold.

---

## 1.2 Distinction Class

The distinction class induced by projection `π_i` is the equivalence relation:

```text
x ~_{π_i, ε_i} y ⇔ ρ_i(π_i(x), π_i(y)) ≤ ε_i
```

The quotient:

```text
X / ~_{π_i, ε_i}
```

is the set of distinguishable state classes under `π_i`.

A projection therefore does not expose reality directly.

It partitions reality into operationally distinguishable classes.

In compressed form:

> A projection creates an operational ontology by partitioning state space.

---

## 1.3 Distinction Refinement

Projection `π_a` is finer than projection `π_b` when:

```text
x ~_{π_a} y ⇒ x ~_{π_b} y
```

but not necessarily the reverse.

Then `π_a` preserves every distinction preserved by `π_b`, plus possibly additional distinctions.

Equivalently:

```text
Π_a refines Π_b
```

when the partition induced by `π_a` is finer than the partition induced by `π_b`.

Example:

```text
LiDAR occupancy projection
```

may distinguish:

```text
free space vs occupied space
```

while object recognition projection may further distinguish:

```text
fridge vs cabinet vs wall
```

In compressed form:

> Learning a new projection can refine the reachable ontology of a system.

---

# 2. Constraint Regimes

A constraint regime defines which transformations are admissible.

## 2.1 Transition Relation

Let:

```text
T_K ⊆ X × X
```

where:

```text
(x, y) ∈ T_K
```

means:

```text
y is an admissible next state from x under constraint regime K
```

The reachable set is:

```text
A_K(x) = { y ∈ X | (x, y) ∈ T_K }
```

For multi-step reachability:

```text
A_K^n(x) = { y ∈ X | there exists a path x = x_0 → x_1 → ... → x_n = y, with each (x_j, x_{j+1}) ∈ T_K }
```

For horizon `H`:

```text
A_K^H(x)
```

represents states reachable within the declared horizon.

In compressed form:

> A constraint regime is a rule that turns state space into reachable and unreachable futures.

---

## 2.2 Constraint Types

Constraints should not be treated as undifferentiated.

A constraint regime may include multiple typed components:

```text
K = K_phys × K_info × K_log × K_comp × K_inst × K_econ × K_norm
```

where:

```text
K_phys = physical constraints
K_info = information-channel constraints
K_log  = logical or formal constraints
K_comp = computational constraints
K_inst = institutional or procedural constraints
K_econ = economic or resource constraints
K_norm = normative admissibility constraints
```

Each type constrains transitions differently.

Examples:

```text
K_phys: a robot arm cannot pass through a wall
K_info: a sensor cannot recover invisible state above its channel capacity
K_log: a proof step must follow inference rules
K_comp: exhaustive search may exceed compute budget
K_inst: a permit cannot be issued without a valid procedure
K_econ: a project cannot execute without budget or resource flow
K_norm: an action may be physically possible but prohibited
```

In compressed form:

> Constraints share the function of restricting admissible transitions, but differ in source, enforcement, reversibility, and failure semantics.

---

## 2.3 Constraint Composition

Multiple constraints combine by intersection over admissible transitions:

```text
T_K = T_{K_1} ∩ T_{K_2} ∩ ... ∩ T_{K_m}
```

A transition is admissible only if it satisfies every active constraint layer.

```text
(x, y) ∈ T_K ⇔ (x, y) ∈ T_{K_j} for all j
```

If one binding constraint rejects the transition, the transition is not admissible.

In compressed form:

> Constraint composition shrinks the reachable set.

---

# 3. Coupling and Interaction

## 3.1 Operational Coupling

Let a system be decomposed into loci:

```text
X = X_a × X_b × X_e
```

where:

```text
X_a = state variables of locus a
X_b = state variables of locus b
X_e = remaining environment
```

Locus `a` is coupled to locus `b` under `K` when changing `x_a` changes the reachable set of `x_b`:

```text
A_K(x_b | x_a) ≠ A_K(x_b)
```

More explicitly, there exist states `x_a, x'_a` such that:

```text
A_K(x_b | x_a) ≠ A_K(x_b | x'_a)
```

In compressed form:

> Interaction begins when one locus changes the reachable future set of another.

---

## 3.2 Interaction Event

An interaction event occurs when:

```text
x_t → x_{t+1}
```

and at least one projection-recoverable distinction in one locus changes the admissible future set of another locus.

Formally:

```text
Interaction_K(a, b, t)
```

holds when:

```text
∃ π_i, ε_i:
Dist_{π_i, ε_i}(x_a(t), x'_a(t))
```

and:

```text
A_K(x_b(t+1) | x_a(t)) ≠ A_K(x_b(t+1) | x'_a(t))
```

In compressed form:

> Interaction is constraint-relevant distinguishability across loci.

---

# 4. Transformations

## 4.1 Transformation Function

A deterministic transformation is:

```text
T : X → X
```

A nondeterministic transformation is:

```text
T : X → P(X)
```

A stochastic transformation is:

```text
P_T(y | x)
```

where:

```text
P_T(y | x)
```

is the probability of transitioning from `x` to `y`.

A transformation is admissible under `K` when:

```text
T(x) ∈ A_K(x)
```

or, for stochastic transformations:

```text
support(P_T(. | x)) ⊆ A_K(x)
```

In compressed form:

> A transformation is constraint-typed when its outputs remain inside the admissible reachable set.

---

## 4.2 Transformation of Distinctions

A transformation `T` preserves a distinction under projection `π_i` when:

```text
Dist_{π_i, ε_i}(x, y) ⇒ Dist_{π_i, ε_i}(T(x), T(y))
```

It collapses a distinction when:

```text
Dist_{π_i, ε_i}(x, y)
```

but:

```text
¬Dist_{π_i, ε_i}(T(x), T(y))
```

It creates a distinction under `π_i` when:

```text
¬Dist_{π_i, ε_i}(x, y)
```

but:

```text
Dist_{π_i, ε_i}(T(x), T(y))
```

In compressed form:

> Transformations can preserve, collapse, or create operational distinctions.

---

## 4.3 Distortion

For projection `π_i`, define transformation distortion:

```text
δ_i^T(x, y) = | ρ_i(π_i(x), π_i(y)) - ρ_i(π_i(T(x)), π_i(T(y))) |
```

A transformation is approximately distinction-preserving over domain `D ⊆ X` if:

```text
δ_i^T(x, y) ≤ η
```

for all relevant `x, y ∈ D`.

In compressed form:

> Distinction preservation can be measured as bounded distortion under projection.

---

# 5. Recoverability

## 5.1 Decoder-Indexed Recoverability

Let:

```text
E : X → Z
```

be an encoder or projection into representation space.

Let:

```text
Δ : Z → X'
```

be a decoder or reconstruction procedure.

A structure is recoverable for use-context `U` when:

```text
Δ(E(x)) ≈_U x
```

where:

```text
≈_U
```

means equivalence with respect to distinctions relevant to use-context `U`.

In compressed form:

> Recoverability is not recovery of everything; it is recovery of use-relevant distinctions.

---

## 5.2 Quantified Recoverability

A distinction between `x` and `y` is recoverable under tuple:

```text
(π_i, Δ, H, C, ε, p, U)
```

when, after horizon `H`, decoder `Δ` can recover the distinction at cost no greater than `C`, with error no greater than `ε`, with probability at least `p`, for use-context `U`.

Formally:

```text
Rec(x, y; π_i, Δ, H, C, ε, p, U)
```

holds when:

```text
P[ ρ_U(Δ(z_H(x)), Δ(z_H(y))) > ε ] ≥ p
```

and:

```text
cost(Δ, z_H) ≤ C
```

where:

```text
z_H(x)
```

is the representation available after horizon `H` from source state `x`.

In compressed form:

> Recoverability is indexed by decoder, horizon, cost, error, probability, and use-context.

---

## 5.3 Memory Condition

A system has memory of a distinction `D(x, y)` over horizon `H` when:

```text
Dist_{π_i, ε_i}(x, y)
```

and:

```text
Rec(x, y; π_i, Δ, H, C, ε, p, U)
```

for some relevant tuple.

Thus memory is not merely storage.

It is delayed recoverability of a projected distinction.

In compressed form:

> Memory is recoverability of a distinction across delay.

---

# 6. Composability

## 6.1 Transformation Composition

Two transformations are composable when the output domain of one lies inside the input domain of another:

```text
T_1 : X → Y
T_2 : Y → Z
```

then:

```text
T_2 ∘ T_1 : X → Z
```

In state-transition form:

```text
(x, y) ∈ T_{K_1}
```

and:

```text
(y, z) ∈ T_{K_2}
```

compose into:

```text
(x, z) ∈ T_{K_2 ∘ K_1}
```

when the intermediate state `y` satisfies the interface conditions required by `T_{K_2}`.

In compressed form:

> Composition requires not just sequence, but interface compatibility between transformations.

---

## 6.2 Constraint-Compatible Composition

A chain:

```text
x_0 → x_1 → ... → x_n
```

is constraint-compatible under `K` when:

```text
(x_j, x_{j+1}) ∈ T_K
```

for every `j`.

If any edge violates `K`, the path is inadmissible.

In compressed form:

> A path is executable only if every local transition is admissible.

---

## 6.3 Recoverability Across Composition

Let:

```text
T_{1:n} = T_n ∘ ... ∘ T_1
```

A distinction is preserved across composition if:

```text
Dist_{π_i, ε_i}(x, y) ⇒ Rec(T_{1:n}(x), T_{1:n}(y); π_i, Δ, H, C, ε, p, U)
```

This does not require identical state preservation.

It requires recovery of the relevant distinction after the composed transformation chain.

In compressed form:

> Persistence is recoverability of relevant distinction across composed transformation.

---

# 7. Minimal Conditions for Interaction-Capable Substrate

A substrate:

```text
S = (X, Π, R, K, T, Δ, μ)
```

is interaction-capable when the following conditions hold.

## 7.1 Nontrivial State Space

There exist at least two states:

```text
∃ x, y ∈ X : x ≠ y
```

## 7.2 Projection Distinguishability

There exists at least one projection that distinguishes at least one pair:

```text
∃ π_i ∈ Π, ∃ x, y ∈ X : Dist_{π_i, ε_i}(x, y)
```

## 7.3 Non-Collapse Under Some Transformation

There exists at least one admissible transformation that does not collapse all projected distinctions:

```text
∃ T ∈ T_K, ∃ π_i, ∃ x, y :
Dist_{π_i, ε_i}(x, y) ∧ Dist_{π_i, ε_i}(T(x), T(y))
```

## 7.4 Coupling

There exist at least two loci whose reachable sets are not independent:

```text
∃ a, b : A_K(x_b | x_a) ≠ A_K(x_b)
```

## 7.5 Composability

There exist at least two admissible transformations that can be chained:

```text
∃ T_1, T_2 : T_2 ∘ T_1 is defined and admissible over some domain
```

## 7.6 Recoverability

There exists at least one distinction recoverable after transformation:

```text
∃ x, y, T, Δ : Rec(T(x), T(y); π_i, Δ, H, C, ε, p, U)
```

In compressed form:

> Interaction-capability requires distinguishability, non-collapse, coupling, admissible transformation, composability, and recoverability.

---

# 8. Organization

## 8.1 Organization Candidate

An organization candidate is a tuple:

```text
O = (X_O, Π_O, K_O, T_O, I_O, Δ_O, B_O)
```

where:

```text
X_O   = organizational state subspace
Π_O   = projections relevant to identifying O
K_O   = constraints governing O
T_O   = admissible transitions of O
I_O   = identity predicate or invariant family
Δ_O   = recovery procedures for O-relevant distinctions
B_O   = boundary or interface conditions
```

In compressed form:

> An organization is a constrained transformation regime with recoverable identity-relevant distinctions.

---

## 8.2 Identity Predicate

An identity predicate is:

```text
I_O : X_O × X_O → {0,1}
```

where:

```text
I_O(x_t, x_{t+1}) = 1
```

means:

```text
O remains identifiable across the transition x_t → x_{t+1}
```

Identity over a path requires:

```text
I_O(x_0, x_1) ∧ I_O(x_1, x_2) ∧ ... ∧ I_O(x_{n-1}, x_n)
```

In compressed form:

> Identity is pathwise preservation of organizational reference, not material sameness.

---

## 8.3 Organization Condition

An organization exists over horizon `H` when there is a path:

```text
x_0 → x_1 → ... → x_H
```

such that:

```text
(x_t, x_{t+1}) ∈ T_{K_O}
```

and:

```text
I_O(x_t, x_{t+1}) = 1
```

for all relevant `t`, with required distinctions recoverable:

```text
Rec(x_t, x_{t+1}; Π_O, Δ_O, H, C, ε, p, U)
```

for the identity-relevant use-context.

In compressed form:

> Organization is sustained admissible transformation under recoverable identity conditions.

---

## 8.4 Emergence Condition

An organization emerges relative to projection family `Π_O` when a previously untracked relation cluster becomes recoverable as a stable transformation regime.

Formally, there exists a projection `π_o` and identity predicate `I_O` such that:

```text
O is not distinguishable under Π_old
```

but:

```text
O is distinguishable under Π_old ∪ {π_o}
```

and its transitions satisfy organization condition over horizon `H`.

In compressed form:

> Emergence is projection-enabled recoverability of a stable transformation regime.

---

# 9. Role and Affordance

## 9.1 Role

A role is not an intrinsic property of a state.

A role is a relation:

```text
Role(x; a, π_i, K, C_a, U)
```

where:

```text
x   = state or entity region
a   = agent or system
π_i = projection exposing relevant distinctions
K   = constraint regime
C_a = capabilities of agent/system a
U   = use-context or task context
```

A state `x` has role `r` for agent `a` when the projection of `x` changes the agent's admissible transformation set in a role-specific way:

```text
A_K(a | π_i(x), C_a, U) ≠ A_K(a | C_a, U)
```

In compressed form:

> Role is the effect of a projected structure on an agent's reachable transformations.

---

## 9.2 Affordance

An affordance is an admissible transformation exposed by the relation between:

```text
structure
projection
capability
constraint
context
```

Formally, action `α` is afforded by `x` to agent `a` when:

```text
α ∈ A_K(a | π_i(x), C_a, U)
```

and:

```text
α ∉ A_K(a | C_a, U)
```

or when the presence of `x` significantly changes the cost, probability, or path of `α`.

Example:

```text
fridge under occupancy projection → avoid
fridge under object-recognition projection + manipulation capability → open
fridge under task projection + inventory model → retrieve drink
```

In compressed form:

> An affordance is a transformation made reachable by a projected relation.

---

# 10. Projection Reconciliation

Two projections may expose different distinctions over the same source state.

## 10.1 Common Refinement

Given projections:

```text
π_a : X → Y_a
π_b : X → Y_b
```

A common refinement is:

```text
π_{a,b}(x) = (π_a(x), π_b(x))
```

This projection preserves distinctions exposed by either projection.

However, it may exceed resource limits.

In compressed form:

> Reconciliation can be achieved by refinement, but refinement has cost.

---

## 10.2 Compatibility

Two projections are compatible over domain `D ⊆ X` when their induced partitions have a nonempty joint interpretation and do not create contradictory action constraints under `K`.

A practical condition is:

```text
∀ x ∈ D, ∃ y ∈ X such that π_a(y) = π_a(x) and π_b(y) = π_b(x)
```

and the joint action set is not empty:

```text
A_K(x | π_a, π_b) ≠ ∅
```

In compressed form:

> Projection conflict becomes operational when combined distinctions leave no admissible transition.

---

# 11. Failure Modes as Formal Conditions

## 11.1 Distinction Failure

A distinction exists in source space but not under projection:

```text
x ≠ y
```

but:

```text
¬Dist_{π_i, ε_i}(x, y)
```

Example:

```text
transparent obstacle not detected by sensor
```

## 11.2 Relation Failure

A distinction is detected, but does not modify any reachable transformation set:

```text
Dist_{π_i, ε_i}(x, y)
```

but:

```text
A_K(a | π_i(x)) = A_K(a)
```

Example:

```text
object label exists but planner exposes no action relation
```

## 11.3 Transformation Failure

A role suggests a transformation, but the transition is not admissible:

```text
α proposed
```

but:

```text
α ∉ A_K(a | π_i(x), C_a, U)
```

Example:

```text
fridge is known but handle is unreachable
```

## 11.4 Composition Failure

Local transformations exist but cannot chain:

```text
T_1 defined
T_2 defined
```

but:

```text
T_2 ∘ T_1 undefined or inadmissible
```

Example:

```text
can approach fridge
can open fridge in isolation
cannot coordinate base and arm under real constraints
```

## 11.5 Recoverability Failure

A distinction was once detectable but later unavailable:

```text
Dist_{π_i, ε_i}(x_t, y_t)
```

but:

```text
¬Rec(x_t, y_t; π_i, Δ, H, C, ε, p, U)
```

Example:

```text
detected object was not stored, indexed, or retrievable
```

## 11.6 Projection Rigidity

A system treats one projection as exhaustive:

```text
π_i(x) treated as x
```

and suppresses other admissible projections:

```text
Π_available → {π_i}
```

Example:

```text
fridge treated only as obstacle, never as container, goal, landmark, or resource node
```

In compressed form:

> Failure occurs when projected distinction cannot be made relationally, transformationally, compositionally, or recoverably usable.

---

# 12. Minimality Claim

The proposed formal primitive set is:

```text
S = (X, Π, R, K, T, Δ, μ)
```

where:

```text
X  = possible states
Π  = projection family producing operational distinctions
R  = relation structure among projected distinctions
K  = constraints on admissible transformation
T  = transformation family
Δ  = recovery or decoding family
μ  = measure of cost, error, probability, distortion, or resource use
```

## 12.1 Why `X`?

Without state space, no variation can be represented.

No distinction, transformation, or reachability can be defined.

## 12.2 Why `Π`?

Without projection, distinction becomes absolute and underspecified.

Projection specifies:

```text
for whom
by what measurement
at what resolution
under what decoder
```

## 12.3 Why `R`?

Without relations, distinguished states are isolated.

There is no coupling, locality, topology, dependency, or role.

## 12.4 Why `K`?

Without constraints, every transition is possible or arbitrary.

There is no admissibility, impossibility, boundary, or structural prediction.

## 12.5 Why `T`?

Without transformations, there is no change, interaction, computation, memory update, execution, or process.

## 12.6 Why `Δ`?

Without decoder or recovery, persistence of structure cannot be tested.

A trace is not operational memory unless relevant distinctions can be recovered.

## 12.7 Why `μ`?

Without measure, recoverability, distortion, cost, probability, and error cannot be compared.

The framework remains conceptual rather than formal.

In compressed form:

> The primitive set is minimal only if distinction is projection-relative, transformation is constraint-typed, and recovery is measurable.

---

# 13. Candidate Propositions

These propositions are intended as testable or derivable claims within the scaffold.

## Proposition 1 — Projection Dependence of Objecthood

If two projections induce different partitions of `X`, then an entity may exist under one projection and not under another.

Formally, for relation cluster `O ⊆ X`:

```text
O distinguishable under π_a
```

but:

```text
O not distinguishable under π_b
```

Therefore objecthood is projection-relative.

Operational consequence:

```text
Changing sensors or models can create new operational objects without changing the underlying physical substrate.
```

---

## Proposition 2 — Compression-Induced Ambiguity

If encoder `E` is many-to-one, then upstream state is not uniquely recoverable from representation alone.

If:

```text
E(x) = E(y)
```

and:

```text
x ≠ y
```

then no decoder `Δ` using only `E(x)` can determine whether the source was `x` or `y` without additional constraints.

Operational consequence:

```text
Self-validation of compressed models is insufficient for full correspondence recovery.
```

---

## Proposition 3 — Recoverability Requires External Constraint After Loss

If a distinction is collapsed by transformation `T`, then recovering that distinction requires information not present in `T(x)` alone.

If:

```text
Dist_{π_i}(x, y)
```

but:

```text
¬Dist_{π_i}(T(x), T(y))
```

then recovery requires:

```text
additional source constraint
prior
side channel
memory
or decoder assumption
```

Operational consequence:

```text
Lost distinctions cannot be regenerated from the collapsed representation alone.
```

---

## Proposition 4 — Organization Requires Nonzero Recoverability Across Composition

If every composed transformation collapses all identity-relevant distinctions below recovery threshold, then organization cannot persist over that horizon.

If for identity predicate `I_O`:

```text
∀ paths x_0 → ... → x_H,
¬Rec(I_O(x_0), I_O(x_H); Π_O, Δ_O, H, C, ε, p, U)
```

then:

```text
O does not persist over H
```

Operational consequence:

```text
Persistence is impossible without recoverable identity-relevant distinctions.
```

---

## Proposition 5 — Affordance Expansion by Projection Refinement

If projection `π_a` refines projection `π_b`, and agent capabilities can act on distinctions exposed only by `π_a`, then the agent's reachable action set may expand.

If:

```text
π_a refines π_b
```

and:

```text
∃ α : α ∈ A_K(agent | π_a(x))
```

but:

```text
α ∉ A_K(agent | π_b(x))
```

then recognition expands affordance space.

Operational consequence:

```text
Object recognition can transform an obstacle into a goal, resource, container, landmark, or tool.
```

---

## Proposition 6 — Parallelism Is Partial-Order Width

Given dependency relation `≺` over transformations, maximum parallelism is bounded by the width of the partial order.

Let:

```text
P = (T, ≺)
```

Then transformations may execute in parallel only if they are incomparable under `≺` and do not violate resource constraints.

Operational consequence:

```text
Parallelism is not absence of constraint; it is structure in which many transformations lack direct dependency edges.
```

---

# 14. Diagnostics

The formal scaffold suggests a diagnostic sequence for any system.

## 14.1 Distinction Diagnostic

Ask:

```text
Which distinctions are available under which projections and resolutions?
```

Formal object:

```text
X / ~_{π_i, ε_i}
```

## 14.2 Relation Diagnostic

Ask:

```text
Which projected distinctions are coupled?
```

Formal object:

```text
R over projected classes
```

## 14.3 Constraint Diagnostic

Ask:

```text
Which transitions are admissible under active constraints?
```

Formal object:

```text
T_K ⊆ X × X
```

## 14.4 Transformation Diagnostic

Ask:

```text
Which transformations preserve, collapse, or create relevant distinctions?
```

Formal object:

```text
δ_i^T(x, y)
```

## 14.5 Recoverability Diagnostic

Ask:

```text
Which distinctions remain recoverable, by which decoder, over which horizon, at what cost and error?
```

Formal object:

```text
Rec(x, y; π_i, Δ, H, C, ε, p, U)
```

## 14.6 Composition Diagnostic

Ask:

```text
Can local transformations be chained without violating interface or constraint conditions?
```

Formal object:

```text
T_n ∘ ... ∘ T_1
```

## 14.7 Organization Diagnostic

Ask:

```text
Does the system preserve identity-relevant distinctions across admissible transformation paths?
```

Formal object:

```text
I_O(x_t, x_{t+1})
```

In compressed form:

> Diagnose systems by tracing distinctions through projection, relation, constraint, transformation, recovery, and composition.

---

# 15. Relation to Common Concepts

The conceptual reinterpretations can be stated formally.

## 15.1 Time

```text
time ≈ ordering relation over transformations
```

Formal object:

```text
(T, ≺)
```

where:

```text
T_i ≺ T_j
```

means:

```text
T_j depends on T_i
```

## 15.2 Space

```text
space ≈ locality relation over distinguishable states
```

Formal object:

```text
R_local ⊆ X × X
```

or metric:

```text
d : X × X → ℝ
```

## 15.3 Memory

```text
memory ≈ recoverable distinction across horizon H
```

Formal object:

```text
Rec(x, y; π_i, Δ, H, C, ε, p, U)
```

## 15.4 Object

```text
object ≈ stable relation cluster under projection and identity predicate
```

Formal object:

```text
O = (X_O, Π_O, K_O, T_O, I_O, Δ_O, B_O)
```

## 15.5 Cause

```text
cause ≈ change in reachable set under coupling
```

Formal object:

```text
A_K(x_b | x_a) ≠ A_K(x_b)
```

## 15.6 Computation

```text
computation ≈ implemented transformation of projected distinctions under constraints
```

Formal object:

```text
T_K : X → X
```

with recoverable input-output distinctions.

In compressed form:

> Ordinary categories become typed structures over projection, relation, transformation, and recoverability.

---

# 16. Summary

This document formalizes the relational constraint substrate by replacing absolute primitives with typed, measurable relations.

The main shifts are:

```text
distinction
→ distinguishability under projection
```

```text
constraint
→ admissible transition relation
```

```text
memory
→ delayed recoverability of distinction
```

```text
object
→ stable relation cluster under projection
```

```text
cause
→ change in reachable future set
```

```text
organization
→ sustained admissible transformation preserving identity-relevant recoverability
```

The proposed substrate is:

```text
S = (X, Π, R, K, T, Δ, μ)
```

where:

```text
X  = state space
Π  = projection family
R  = relation structure
K  = constraint regime
T  = admissible transformation family
Δ  = decoder or recovery family
μ  = measure of cost, error, probability, distortion, or resource use
```

The minimal interaction condition is:

```text
projection-distinguishable states
+ coupling
+ constraint-typed transformation
+ composability
+ recoverability
```

The minimal organization condition is:

```text
composed admissible transformations
+ identity predicate
+ recoverable identity-relevant distinctions
+ horizon-bounded support
```

In final compressed form:

```text
Distinction is projection-relative.
Transformation is constraint-typed.
Persistence is recoverability across composition.
Organization is sustained recoverability of identity-relevant structure under admissible transformation.
```

---

# 17. Open Formal Questions

This scaffold leaves several formal questions unresolved.

## 17.1 Minimal Primitive Reduction

Can the primitive set:

```text
S = (X, Π, R, K, T, Δ, μ)
```

be reduced further?

Possibilities:

```text
(X, Π, T, μ)
```

with `R`, `K`, and `Δ` derived.

or:

```text
(X, K, T)
```

with projections treated as constraints.

The current document keeps them separate for diagnostic clarity.

## 17.2 Category-Theoretic Version

Can transformations be treated as morphisms, projections as functors, and recoverability as approximate inverse or adjoint structure?

Possible mapping:

```text
objects      = state spaces or distinction classes
morphisms    = admissible transformations
functors     = projections between categories
invariants   = preserved structures under morphisms
recoveries   = partial inverses or reconstruction maps
```

## 17.3 Quantitative Emergence

Can emergence be measured as increase in recoverable relation structure under a new projection?

Candidate measure:

```text
Emergence(π_new) = I(projected relation cluster; future reachable states) - cost(π_new)
```

## 17.4 Organization Threshold

Can a threshold be defined for when repeated recoverability across transformation becomes organization rather than transient pattern?

Candidate condition:

```text
persistence probability × recovery fidelity × composition depth > threshold
```

## 17.5 Empirical Testing

Potential domains:

```text
robot perception-action systems
LLM tool-use pipelines
memory systems
institutional records
software architecture
biological regulation
supply-chain resilience
```

The testable claim is:

> Systems fail predictably when they detect distinctions without preserving the relation, transformation, recovery, or composition structure required to make those distinctions operational.

In compressed form:

> The next step is to turn the scaffold into measures that predict collapse, affordance expansion, memory failure, and organization persistence.
