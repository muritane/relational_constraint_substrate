# Recoverability Support Field Integration

## What the Recoverability Support Fields Extension Introduces, Improves, and Adjusts

---

# Status

This document is a companion extension to:

```text
Relational Constraint Substrate
Formal Relational Constraint Substrate
Recoverability Support Fields
```

Its purpose is integrative.

The earlier substrate introduced distinction, projection, constraint, transformation, coupling, composability, and recoverability.

The recoverability support fields extension adds a missing layer:

```text
locality of recovery
support distribution
carrier density
regeneration domain
resistance gradient
transport of support
boundary as recoverability threshold
```

This document states what is improved, what is newly introduced, and what should be adjusted in the prior documents.

In compressed form:

> Recoverability is not merely a predicate on a distinction. It is a distributed field over regions, substrates, decoders, costs, horizons, and regeneration mechanisms.

---

# Abstract

The original relational constraint substrate asked:

```text
Which distinctions can constrain transformations while remaining recoverable enough to support interaction, memory, computation, objecthood, and organization?
```

The formal substrate made this more precise by indexing recoverability by:

```text
projection
resolution
decoder
horizon
cost
error
probability
use-context
```

The recoverability support fields extension improves this by adding:

```text
where recoverability is supported
which substrates carry it
how densely it is represented
which mechanisms regenerate it
how resistance varies across regions
how support can be transported or lost
```

The resulting question becomes:

```text
Where, through what support structure, by which decoder, under which constraint regime, and at what cost does distinction D remain recoverable or regenerable?
```

In compressed form:

> Existence-for-use is local, substrate-indexed, cost-bounded recoverability under projection and constraint.

---

# 0. Orientation

The earlier substrate treated recoverability mainly as a relation between:

```text
source distinction
encoded trace
decoder
horizon
cost
error
probability
use-context
```

This was sufficient for defining memory, persistence, organization, and composable transformation.

But it left underdeveloped the fact that recoverability is unevenly distributed.

A distinction can be:

```text
highly recoverable here
weakly recoverable there
unrecoverable elsewhere
recoverable only through communication
recoverable only if carriers are transported
recoverable only if a regeneration regime remains active
```

Examples:

```text
dollar distinction
corporation distinction
language distinction
private memory distinction
electron distinction
clock distinction
roof-leak precursor distinction
```

These do not differ merely by being physical or nonphysical.

They differ by their support geometry.

In compressed form:

> Different kinds of things differ by the shape, density, durability, and regeneration of their recoverability fields.

---

# 1. The Main Improvement

## 1.1 From Recoverability Predicate to Recoverability Field

Earlier formulation:

```text
Rec(D; π, Δ, H, C, ε, p, U)
```

means distinction `D` is recoverable under projection `π`, decoder `Δ`, horizon `H`, cost bound `C`, error bound `ε`, probability threshold `p`, and use-context `U`.

The support-field extension changes this to:

```text
LocalRec(D; L, B, π, Δ, H, C, ε, p, U)
```

where:

```text
L = region, locus, domain, neighborhood, jurisdiction, access zone, or organizational locality
B = substrate, carrier family, medium, infrastructure, or support base
```

Then recoverability becomes a field:

```text
Φ_D(L, B, U)
```

rather than a global yes/no property.

In compressed form:

> Recoverability becomes spatially, institutionally, materially, and procedurally distributed.

---

## 1.2 Why This Matters

Without locality, the framework can say:

```text
The dollar distinction is recoverable.
```

With locality, the framework can say:

```text
The dollar distinction is highly recoverable in banks, ledgers, payment networks, contracts, central bank systems, and ordinary commercial practice.

It is weakly recoverable in remote regions without communication.

It is locally unrecoverable in arbitrary matter unless a supporting representation, decoder, or channel is present.
```

Without locality, the framework can say:

```text
A corporation is a recoverable organization.
```

With locality, it can say:

```text
A corporation has support hubs, legal carriers, employee carriers, database carriers, authority paths, communication channels, jurisdictional boundaries, and regeneration mechanisms.
```

In compressed form:

> The extension turns abstract persistence into recoverability geography.

---

# 2. What Is Newly Introduced

## 2.1 Support Region

A support region is the domain in which a distinction remains recoverable above an operational threshold.

```text
Supp_θ(D) = { (L, B) | Φ_D(L, B, U) ≥ θ_U }
```

where:

```text
θ_U = recoverability threshold for use-context U
```

This threshold may depend on:

```text
agent capability
cost budget
time horizon
risk tolerance
projection family
decoder availability
required fidelity
```

In compressed form:

> A support region is where a distinction remains operationally available.

---

## 2.2 Recovery Density

Recovery density measures how concentrated the distinction-supporting carriers are in a region.

```text
σ_D(L, B)
```

High recovery density means:

```text
many carriers
many independent traces
many redundant encodings
many access paths
many compatible decoders
low reconstruction cost
```

Low recovery density means:

```text
few traces
fragile carriers
poor redundancy
missing decoder
high access cost
long reconstruction path
```

Examples:

```text
Federal Reserve systems are high-density support hubs for dollar-relevant distinctions.

A single unspoken memory in one brain has low-density private support.

A living language community has higher active recovery density than an unread archive.
```

In compressed form:

> Recovery density is the local concentration of structures from which a distinction can be reconstructed.

---

## 2.3 Support Hub

A support hub is a region or substrate where many recovery paths converge.

```text
Hub_D(L) ⇔ σ_D(L) is high and access paths from L to other support regions are numerous
```

Examples:

```text
banking databases for monetary distinctions
courts and registries for legal distinctions
laboratories and textbooks for scientific distinctions
speaking communities for language distinctions
source repositories and runtime environments for software distinctions
neural populations for private memory distinctions
```

A hub is not necessarily the object itself.

It is a region where the object's identity-relevant distinctions are densely recoverable.

In compressed form:

> A hub is not the thing; it is where the thing becomes easy to recover.

---

## 2.4 Regeneration Domain

A regeneration domain is a region or substrate regime that actively recreates a distinction over time.

```text
Γ_D(L, B) > 0
```

means that region `L` and substrate `B` contain processes that regenerate distinction `D`.

Examples:

```text
legal practice regenerates corporation distinctions
markets regenerate price distinctions
schools regenerate language distinctions
laboratories regenerate scientific distinctions
oscillators regenerate clock distinctions
physical constraint regimes regenerate electron-relevant distinctions
```

This is different from storage.

Storage preserves a trace.

Regeneration recreates a distinction across carrier turnover.

In compressed form:

> Storage lets a distinction wait; regeneration lets it live.

---

## 2.5 Resistance Gradient

A resistance gradient measures how recovery cost changes across regions and substrates.

```text
Res_D(L, B, Δ, U) = Cost_D(L, B, Δ, U)
```

or, more generally:

```text
∇Res_D
```

tracks how rapidly recovery becomes harder when moving away from support hubs or regeneration domains.

Low resistance:

```text
many carriers
many decoders
high redundancy
short access path
active regeneration
low institutional or physical friction
```

High resistance:

```text
few carriers
weak traces
hostile substrate
missing decoder
long causal path
high energy cost
no local regeneration
```

In compressed form:

> Resistance is the cost of making a distinction recoverable where the substrate does not already support it.

---

## 2.6 Transported Support

A distinction can enter a region by transporting carriers, decoders, or regeneration machinery.

```text
Transport(D, L_a → L_b)
```

may occur by moving:

```text
records
devices
trained agents
software
measurement instruments
legal documents
communication channels
protocols
rituals
models
memory carriers
```

A spacecraft can carry Earth-origin clocks, maps, money records, software protocols, and measurement conventions into space.

Those distinctions are not recovered from vacuum alone.

They are recovered from imported support.

In compressed form:

> Expansion of a distinction's domain requires either local regeneration or imported support.

---

## 2.7 Boundary as Threshold Crossing

A boundary is not always a surface.

For distinction `D`, a boundary can be defined as the region where recoverability falls below an operational threshold.

```text
Boundary_θ(D) = { L | Φ_D(L) crosses θ }
```

This applies to:

```text
physical objects
institutions
languages
jurisdictions
software systems
organisms
scientific concepts
private memories
```

A rock may have a boundary that roughly aligns with physical geometry.

A corporation has boundaries formed by:

```text
contracts
jurisdiction
employment relations
recognized control paths
assets
records
authority chains
communication systems
```

A language has boundaries formed by:

```text
speakers
texts
teaching practices
mutual intelligibility
correction norms
transmission pathways
```

In compressed form:

> A boundary is where identity-relevant distinctions stop being cheaply recoverable.

---

# 3. What Is Improved

## 3.1 Improved Treatment of Existence

The earlier framework already displaced the question:

```text
What objects exist?
```

with:

```text
Which distinctions are recoverable under which projections and constraints?
```

The support-field extension improves this further:

```text
Where are those distinctions recoverable, by what support, and at what cost?
```

This reduces confusion around entities whose reality is distributed, institutional, informational, or projection-relative.

Examples:

```text
dollar
corporation
citizenship
software account
legal title
scientific concept
memory
species
word meaning
```

These are not unreal because they require interpretation.

They are real where their distinction-supporting carriers, decoders, and regeneration regimes remain active.

In compressed form:

> Existence claims become support-distribution claims.

---

## 3.2 Improved Treatment of Physical and Institutional Entities

The extension avoids a crude split between:

```text
physical things
nonphysical things
```

All distinctions require physical instantiation.

But not all distinctions have the same support geometry.

Electron-relevant distinctions are broadly recoverable because the physical constraint regimes that regenerate them are broadly active.

Dollar-relevant distinctions are locally and institutionally recoverable because their support depends on:

```text
records
payment systems
recognition
law
human practice
central bank procedure
communication channels
```

This does not make dollars nonphysical.

It means their recovery field depends on different substrate classes and regeneration regimes.

In compressed form:

> The difference is not physical versus nonphysical; it is broad physical regeneration versus specialized organizational regeneration.

---

## 3.3 Improved Treatment of Memory

The original substrate defined memory as delayed recoverability of distinction.

The support-field extension improves this by asking:

```text
Where is the memory recoverable?
How redundant is it?
Which substrate carries it?
Is it merely stored or actively regenerated?
What happens if a decoder is lost?
```

A memory can therefore be classified as:

```text
private neural support
shared conversational support
written support
digital support
institutional support
ritual support
scientific support
```

Each has different:

```text
durability
copyability
error profile
access path
regeneration rate
decay rate
recovery cost
```

In compressed form:

> Memory is not only delayed recoverability; it is delayed recoverability distributed across support media.

---

## 3.4 Improved Treatment of Organization

The formal substrate defined organization as sustained admissible transformation under recoverable identity conditions.

The support-field extension adds that an organization has:

```text
identity support regions
support hubs
carrier density
regeneration domains
access paths
boundary thresholds
resistance gradients
failure zones
```

An organization persists not because its material parts remain identical, but because identity-relevant distinctions remain recoverable and regenerated across turnover.

Examples:

```text
employees change
servers change
buildings change
procedures change
contracts update
records migrate
```

but the organization persists if its identity-relevant distinction cluster remains recoverable above threshold.

In compressed form:

> An organization is a distributed recoverability regime with active regeneration.

---

## 3.5 Improved Treatment of Discovery

The earlier framework treated discovery as projection refinement.

The support-field extension adds:

```text
discovery creates new local recoverability
new distinctions require new support
new support can expand through instruments, records, training, and institutions
```

A newly discovered distinction may initially be recoverable only in:

```text
a lab
a detector system
a trained expert's practice
a dataset
a mathematical formalism
a small research community
```

It becomes more persistent when support expands.

In compressed form:

> Discovery is not complete when a distinction is first detected; it matures as its support field expands.

---

## 3.6 Improved Treatment of Failure

The prior framework identified failures such as:

```text
distinction failure
relation failure
transformation failure
composition failure
recoverability failure
projection rigidity
```

The support-field extension adds field-level failures:

```text
support thinning
hub collapse
access-path loss
carrier decay
decoder loss
regeneration failure
boundary retreat
resistance increase
transport failure
```

Examples:

```text
a file remains stored but no reader exists
an archive survives but no one can interpret it
a currency has records but no active market
an institution has legal traces but no enforcement path
a scientific distinction has papers but no reproducible instrumentation
```

In compressed form:

> A distinction can fail not only by being erased, but by losing the field conditions that make it recoverable.

---

# 4. What Should Be Adjusted in the Earlier Documents

## 4.1 Adjustment to the Conceptual Substrate

Original emphasis:

```text
Interaction is constrained state-change across a recoverable distinction.
```

Adjusted emphasis:

```text
Interaction is constrained state-change across a distinction recoverable within a local support field.
```

This means every discussion of:

```text
memory
objecthood
cause
computation
organization
role
affordance
```

should allow the question:

```text
Where is the relevant distinction recoverable, and what support makes it so?
```

In compressed form:

> Recoverability should be treated as locally supported, not globally presumed.

---

## 4.2 Adjustment to the Formal Substrate

Original formal substrate:

```text
S = (X, Π, R, K, T, Δ, μ)
```

Recommended extended substrate:

```text
S_R = (X, Π, R, K, T, Δ, μ, L, B, A, Φ, σ, Γ)
```

where:

```text
L = locality domain
B = substrate or carrier family
A = access-path structure
Φ = recoverability field
σ = recovery density
Γ = regeneration operator or regeneration field
```

The measure component `μ` should include or interface with:

```text
cost
probability
error
distortion
decay
redundancy
access cost
regeneration rate
```

In compressed form:

> The formal substrate should make locality, carrier class, access path, field strength, density, and regeneration explicit.

---

## 4.3 Adjustment to Recoverability

Original recoverability:

```text
Rec(x, y; π, Δ, H, C, ε, p, U)
```

Adjusted recoverability:

```text
Rec(x, y; L, B, A, π, Δ, H, C, ε, p, U)
```

or:

```text
LocalRec(D; L, B, A, π, Δ, H, C, ε, p, U)
```

This makes explicit that recovery depends on:

```text
where the recovering system is
which carriers are available
which access paths are open
which decoders exist
which regeneration mechanisms remain active
```

In compressed form:

> Recovery is indexed by locality and support, not only by decoder and horizon.

---

## 4.4 Adjustment to Objecthood

Original objecthood:

```text
An object is a recoverable relation cluster under projection and use-context.
```

Adjusted objecthood:

```text
An object is a cluster of distinctions whose recovery fields cohere across regions, substrates, projections, and horizons.
```

This handles different object types more cleanly:

```text
chair
storm
cell
corporation
electron
language
software system
legal title
private memory
```

Each has a different recovery-field geometry.

In compressed form:

> Objecthood is coherence in a cluster of recoverability fields.

---

## 4.5 Adjustment to Organization

Original organization:

```text
Organization is sustained composability of interaction under preserved distinction.
```

Adjusted organization:

```text
Organization is sustained composability of interaction under regenerated identity-relevant recoverability fields.
```

This adjustment distinguishes:

```text
stored organization
active organization
dormant organization
defunct organization
simulated organization
remembered organization
legally alive organization
operationally alive organization
```

In compressed form:

> Organization persists when its identity distinctions are not merely stored but regenerated above threshold.

---

## 4.6 Adjustment to Boundary

Original boundary treatment:

```text
A boundary is where a distinction or relation cluster stops being operationally available under projection.
```

Adjusted boundary treatment:

```text
A boundary is where the support field for identity-relevant distinctions falls below the threshold required by a use-context.
```

This makes boundaries:

```text
projection-relative
cost-relative
agent-relative
support-relative
regeneration-relative
```

In compressed form:

> Boundaries are threshold surfaces in recoverability space.

---

# 5. Formal Refinement

## 5.1 Vector-Valued Recovery Field

A scalar field:

```text
Φ_D(L) ∈ ℝ_{0}
```

is useful as a first approximation.

But recoverability strength combines several different dimensions.

A more precise form is vector-valued:

```text
Φ_D(L, B, U) = (p, C, ε, H, r, σ, a, g, q)
```

where:

```text
p = probability of successful recovery
C = recovery cost
ε = expected or bounded error
H = supported horizon
r = redundancy
σ = carrier density
a = access-path availability
g = regeneration strength
q = decoder or projection quality
```

The use-context `U` determines how these dimensions are weighted.

```text
Score_U(Φ_D) ≥ θ_U
```

then defines operational support.

In compressed form:

> A distinction is supported when its recoverability vector satisfies the threshold of a use-context.

---

## 5.2 Support Condition

A distinction `D` is supported in `(L, B)` for use-context `U` when:

```text
Support(D; L, B, U) ⇔ Score_U(Φ_D(L, B, U)) ≥ θ_U
```

This allows different agents or systems to have different support maps.

A distinction may be recoverable for:

```text
expert but not novice
instrumented system but not naked observer
connected terminal but not isolated terminal
court system but not private individual
trained model but not untrained model
```

In compressed form:

> Support is relative to the recovery capabilities and thresholds of a use-context.

---

## 5.3 Regeneration Condition

A distinction `D` is regenerated in `(L, B)` when there exists a process `G` such that, across horizon `H`, identity-relevant distinction remains recoverable despite carrier turnover.

```text
Regen(D; L, B, G, H, U)
```

holds when:

```text
∀ t ∈ H, Support(D_t; L, B, U)
```

and there is nontrivial replacement or refresh of carriers:

```text
B_t ≠ B_{t+1}
```

while:

```text
D_t ≈_U D_{t+1}
```

In compressed form:

> Regeneration is preservation of recoverable distinction through support turnover.

---

## 5.4 Support Transport Condition

Support is transported from region `L_a` to region `L_b` when carriers, decoders, or regeneration mechanisms are moved or copied such that:

```text
¬Support(D; L_b, B_b, U)
```

before transport, but:

```text
Support(D; L_b, B_b', U)
```

after transport.

Formally:

```text
Transport_D(L_a → L_b) ⇒ Φ_D(L_b, B_b', U) > Φ_D(L_b, B_b, U)
```

In compressed form:

> Transport extends a recovery field by moving or rebuilding its support path.

---

# 6. Integration With Constraint Regimes

## 6.1 Support as Constraint-Dependent

Support is not passive.

A distinction's support depends on active constraints.

For example:

```text
legal distinction requires legal constraints
currency distinction requires institutional and economic constraints
software distinction requires computational constraints
memory distinction requires biological or storage constraints
clock distinction requires physical and engineering constraints
```

Thus:

```text
Φ_D = Φ_D(L, B, K, Π, Δ, U)
```

where `K` determines which transformations preserve or regenerate the distinction.

In compressed form:

> A support field is shaped by the constraint regime that preserves, refreshes, or destroys its carriers.

---

## 6.2 Constraint Failure as Field Collapse

If the constraint regime that regenerates a distinction fails, the support field may decay even if some carriers remain.

Examples:

```text
a currency after institutional collapse
a software protocol after runtime disappearance
a law after enforcement failure
a language after speaker extinction
a scientific model after instrumentation loss
```

The distinction may remain archived.

But it no longer functions as active organization.

In compressed form:

> Archival survival is not the same as operational regeneration.

---

# 7. Integration With Projection

## 7.1 Projection Availability

A region may contain carriers but lack the projection needed to recover a distinction.

```text
Carrier(D, L) ∧ ¬ProjectionAvailable(π_D, L)
```

then local recovery may fail.

Examples:

```text
ancient inscription without script knowledge
sensor trace without calibration model
legal document without recognized authority
raw dataset without feature schema
biological signal without assay technique
```

In compressed form:

> A carrier does not support a distinction unless a projection can expose it.

---

## 7.2 Projection Discovery Expands Support

When a new projection is discovered:

```text
Π_old → Π_old ∪ {π_new}
```

then support for a previously unrecoverable distinction may appear:

```text
Φ_D^{Π_old}(L) < θ
```

but:

```text
Φ_D^{Π_old ∪ {π_new}}(L) ≥ θ
```

Examples:

```text
microscopy exposing cellular distinctions
spectroscopy exposing chemical distinctions
formal accounting exposing financial distinctions
logging exposing software failure distinctions
medical imaging exposing pre-symptomatic disease distinctions
```

In compressed form:

> A new projection can turn latent structure into recoverable support.

---

# 8. Integration With Cause and Influence

## 8.1 Cause as Field Perturbation

A cause can be treated as a change in the reachable future set of a locus.

The support-field extension adds that causes can also perturb recovery fields.

```text
Cause(a, b) ⇔ A_K(b | a) ≠ A_K(b)
```

Field version:

```text
Cause(a, Φ_D) ⇔ Φ_D changes under the presence, absence, or state of a
```

Examples:

```text
burning an archive lowers support for recorded distinctions
teaching a language increases support for linguistic distinctions
building a bank branch increases local support for monetary distinctions
installing a sensor increases support for environmental distinctions
cutting a network link reduces local support for remote account distinctions
```

In compressed form:

> Influence includes changing what distinctions are recoverable where.

---

## 8.2 Support Engineering

An agent can act on a distinction not only by changing the object directly, but by changing the support field around it.

Examples:

```text
backup records
train decoders
distribute copies
build institutions
install sensors
create standards
publish documentation
open communication channels
refresh carriers
create redundancy
```

In compressed form:

> Support engineering is action aimed at making distinctions more recoverable.

---

# 9. New Failure Modes

## 9.1 Support Thinning

Support thinning occurs when recovery density falls while the distinction has not fully disappeared.

```text
σ_D(L, B) decreases
```

Examples:

```text
fewer speakers of a language
fewer maintainers of a protocol
fewer copies of a dataset
fewer experts able to interpret a method
```

In compressed form:

> Support thinning is gradual loss of recoverability before collapse.

---

## 9.2 Hub Collapse

Hub collapse occurs when a high-density support region fails.

```text
Hub_D(L) fails ⇒ Φ_D decreases over dependent regions
```

Examples:

```text
banking system outage
archive destruction
server failure
court system breakdown
central repository deletion
```

In compressed form:

> A hub collapse can reduce recoverability far beyond the hub itself.

---

## 9.3 Access-Path Loss

A region may retain remote recoverability only through a communication or access path.

If that path is lost:

```text
A_path(L, Hub_D) = 0
```

then local support may fall below threshold.

Examples:

```text
payment terminal without network
remote lab without database access
software service without authentication path
legal actor outside jurisdictional recognition
```

In compressed form:

> A distinction may be locally recoverable only because it is connected to elsewhere.

---

## 9.4 Decoder Loss

A carrier may persist while the decoder disappears.

```text
Carrier(D, L) remains
Δ_D unavailable
Rec(D) fails
```

Examples:

```text
unknown script
obsolete file format
forgotten ritual
uncalibrated instrument output
unmaintained machine-learning model checkpoint
```

In compressed form:

> A trace without a decoder is not operational memory.

---

## 9.5 Regeneration Failure

A distinction may remain stored but cease to be actively recreated.

```text
Γ_D(L, B) → 0
```

Examples:

```text
defunct corporation
inactive currency
abandoned protocol
dead language
obsolete measurement standard
```

In compressed form:

> Regeneration failure converts living distinction into archive.

---

# 10. Examples

## 10.1 Dollar

The dollar distinction is supported by:

```text
central bank infrastructure
commercial banks
ledgers
cash
payment networks
legal tender rules
contracts
merchant practice
accounting conventions
expectations
exchange systems
```

Its support field is dense in financial institutions and ordinary commercial environments.

It is weak or absent in regions with no carriers, no communication, no recognition, and no enforcement path.

Its regeneration domain includes:

```text
banking operations
legal recognition
market exchange
taxation
accounting
monetary policy
payment settlement
```

In compressed form:

> A dollar persists where monetary distinctions are recorded, recognized, exchanged, and regenerated.

---

## 10.2 Corporation

A corporation is supported by:

```text
charters
registries
contracts
employees
bank accounts
servers
property records
communications
recognized obligations
legal procedures
```

Its boundary is not a wall.

Its boundary is where corporate identity-relevant distinctions stop being recoverable or enforceable.

Its regeneration domain includes:

```text
governance
payroll
contract execution
legal compliance
customer interaction
internal communication
record maintenance
```

In compressed form:

> A corporation is a distributed identity field regenerated by legal, financial, procedural, and communicative constraints.

---

## 10.3 Electron

Electron-relevant distinctions are broadly recoverable because the relevant physical constraint regimes are broadly active.

Support does not require human institutions to already exist locally.

It may require instruments and projections for a given agent, but the interaction regimes that make electron distinctions recoverable are physically widespread.

In compressed form:

> An electron has a broad physical recovery field because its distinguishing constraints are widely regenerated by physical law.

---

## 10.4 Private Memory

A private memory may be supported by only one neural substrate.

Its recovery field is narrow.

If the memory is spoken, written, acted upon, or encoded externally, its support field expands.

If not, it may disappear with the carrier.

In compressed form:

> A private distinction survives by becoming public, recorded, enacted, or redundantly encoded.

---

## 10.5 Scientific Concept

A scientific concept may be supported by:

```text
papers
textbooks
measurements
instruments
trained experts
laboratory practices
mathematics
software
replication procedures
```

If the concept maps onto stable physical constraints, reality can regenerate evidence for it.

If it survives only by repetition or authority, its support may weaken when institutional support decays.

In compressed form:

> A scientific concept persists through both archival support and repeated contact with regenerating constraint regimes.

---

# 11. Candidate Propositions

## Proposition 1 — Locality of Existence-for-Use

If a distinction `D` is recoverable in region `L_a` but not recoverable in region `L_b` under the relevant threshold, then `D` exists-for-use in `L_a` but not in `L_b` for that use-context.

Formally:

```text
Support(D; L_a, B_a, U) ∧ ¬Support(D; L_b, B_b, U)
```

implies:

```text
D is operationally available in L_a but not in L_b
```

In compressed form:

> Global support does not imply local availability.

---

## Proposition 2 — Regeneration Outlives Storage

If two distinctions have equal storage density but one has stronger regeneration, the regenerated distinction is more likely to persist across carrier turnover.

```text
σ_D ≈ σ_E
```

but:

```text
Γ_D > Γ_E
```

then, all else equal:

```text
Persistence_H(D) > Persistence_H(E)
```

In compressed form:

> Regenerated distinctions survive turnover better than merely stored distinctions.

---

## Proposition 3 — Support Expansion Changes Objecthood

If new carriers, decoders, or regeneration mechanisms expand the support field of a distinction cluster, the operational object associated with that cluster may gain persistence, boundary, and agency relevance.

```text
Φ_{cluster}(L) increases across regions
```

implies possible change in:

```text
object boundary
role
affordance
institutional reach
memory horizon
```

In compressed form:

> Changing support changes what kind of object a system can treat something as.

---

## Proposition 4 — Hub Dependence Creates Fragility

If a distinction's support field depends heavily on one hub, then hub failure can produce nonlocal recoverability collapse.

```text
Φ_D(L_i) depends on Hub_D(L_h)
```

and:

```text
Hub_D(L_h) fails
```

then:

```text
Φ_D(L_i) may fall below θ
```

for many dependent regions.

In compressed form:

> Centralized recoverability produces centralized fragility.

---

## Proposition 5 — Projection Discovery Converts Latent Support Into Active Support

If carriers exist but no projection exposes the relevant distinction, then support is latent.

When a projection is introduced, latent support may become active.

```text
Carrier(D, L) ∧ ¬Available(π_D)
```

then:

```text
Φ_D(L) < θ
```

but after:

```text
Π → Π ∪ {π_D}
```

it may become:

```text
Φ_D(L) ≥ θ
```

In compressed form:

> Discovery can activate support that was physically present but operationally inaccessible.

---

# 12. Minimal Revised Primitive Set

The original minimal primitive set was:

```text
S = (X, Π, R, K, T, Δ, μ)
```

A support-aware primitive set is:

```text
S_R = (X, Π, R, K, T, Δ, μ, L, B, A, Φ, σ, Γ)
```

where:

```text
X  = state space
Π  = projection family
R  = relation structure
K  = constraint regime
T  = admissible transformations
Δ  = decoder family
μ  = measure family
L  = locality domain
B  = substrate or carrier family
A  = access-path structure
Φ  = recoverability field
σ  = recovery density
Γ  = regeneration field or operator
```

This is not necessarily the final minimal set.

It is the minimal set needed once recoverability is treated as distributed rather than global.

In compressed form:

> Locality, carrier class, access path, field strength, density, and regeneration become necessary once recoverability is spatialized.

---

# 13. Summary of Introductions, Improvements, and Adjustments

## 13.1 Introduced

```text
local recoverability
support regions
recovery fields
recovery density
support hubs
regeneration domains
resistance gradients
transported support
threshold boundaries
field-level failure modes
```

In compressed form:

> The extension introduces the spatial and substrate distribution of recoverability.

---

## 13.2 Improved

The extension improves treatment of:

```text
existence
objecthood
memory
organization
institutional entities
scientific concepts
physical versus social distinctions
discovery
failure
boundary
persistence
```

It does so by replacing binary or global recoverability with local, cost-indexed, substrate-indexed support.

In compressed form:

> The framework becomes better at describing entities whose persistence is distributed, infrastructural, or regenerated.

---

## 13.3 Adjusted

The following should be adjusted in the prior documents:

```text
recoverability should include locality and substrate
memory should include support distribution
objecthood should be treated as recovery-field coherence
organization should require regeneration of identity-relevant distinctions
boundaries should be threshold crossings in recoverability space
cause should include perturbation of support fields
projection discovery should include support activation
failure modes should include support loss and regeneration collapse
```

In compressed form:

> The older framework remains intact, but recoverability should be reinterpreted as field-like rather than merely predicate-like.

---

# 14. Closing Compression

The relational constraint substrate began with:

```text
distinction
relation
constraint
transformation
recoverability
composition
organization
```

The support-field extension adds:

```text
where
through what
how densely
how redundantly
how actively regenerated
with what resistance
across what boundary
by what transported support
```

The central revision is:

```text
A distinction persists where its recovery field remains above threshold, or where a regeneration domain recreates it faster than support decays.
```

In compressed form:

> Reality-for-use is not just what can be distinguished. It is what can be recovered, regenerated, and acted on within a support field.
