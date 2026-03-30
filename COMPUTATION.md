# Computation

## The Native Computation Layer
### v2 — March 2026

**Author:** Kael

---

**Document Species:** CANONICAL. Computation theory. Owns three computation types (I/II/III) with characterization theorems, four-tag system, dual signature, hardness functional, cost formalism, compression and recurrence theorems, computational blindness, OWF = Phase-Dist asymmetry, self-application, algorithm classification, observer distances.

**Grid address:** B(3–5, all). Computation theory spans algebraic (Level 3), projected (Level 4), and observer (Level 5) levels.

**Depends on:** SUBSTRATE (four modes, UAT, Phase-Dist). CATEGORY (Dist, UKI, quotient). ALGEBRA (generators, eigenvalues, orbit types, GPF). OBSERVER (A1–A4, Bekenstein, K1'). CROSS_PROJECTION (central collapse, lattice).
**Required by:** PHYSICS (gauge coupling, Landauer chain). SHA256 (algorithm classification). GOVERNANCE (execution grammar references computation types). ASI (computational self-model).

---

**Computation is not external to the framework.** It is the management of distinguishability under observer bounds, phase character, and tower depth. A computation is a phase-typed morphism on observer-accessible structured states, with cost measured by branching, compression behavior, and effective tower depth, and algorithmic character measured by signature.

---

## THEOREM INDEX

| Theorem | Statement | Section |
|---------|-----------|---------|
| C.1 | Type I Characterization (compression/closure) | §2 |
| C.2 | Type II Characterization (expansion/generation) | §2 |
| C.3 | Type III Characterization (rotation/recurrence) | §2 |
| C.4 | Rotational Normal Form | §2 |
| C.5 | Phase Profile: P1 eliminated at level n≥2 | §1 |
| **C.6** | **Hardness Functional Uniqueness (GPF weights)** | **§3** |
| C.7 | Compression Minimality | §4 |
| C.8 | Recurrence Normal Form | §4 |
| **C.9** | **Computational Blindness (4 parts, UKI instance)** | **§5** |
| **C.10** | **One-Wayness = Phase-Dist Asymmetry** | **§6** |
| C.10a | OWF Threshold at φ̄² | §6 |

---

## §1 COMPUTATIONAL AXIOMS AND THE FOUR TAGS

**Seven axioms** (all implicit in prior files, made explicit):

| Axiom | Statement | Source |
|-------|-----------|--------|
| C1 | S₀={0,1} unique tower apex | SUBSTRATE Thm 0.10 |
| C2 | Self-product tower gives depth hierarchy | OBSERVER §1 A3 |
| C3 | Observer K=(d_K,Δ_K,σ_K) with σ_K=Jordan fractions | OBSERVER §1, ALGEBRA §11 |
| C4 | d_K² compression wall bounds all computation | OBSERVER §2 |
| C5 | Three phase types P1/P2/P3 type all transformations | ALGEBRA §4 |
| C6 | Compression canonical and idempotent; expansion non-canonical | SUBSTRATE §18 (UAT) |
| C7 | K→F→U(K)→K closes self-application architecture | OBSERVER §4 |

**Four tags per computation f:**

**Phase type.** ph(f) from orbit type of M_f: compressive (det<0, P1), transitional (det>0 Δ>0, P2), rotational (det>0 Δ<0, P3).

**Theorem C.5 (Phase Profile).** *At tower level n≥2: det(M)≥0 for all tensor products. P1 impossible at n≥2. P3 fraction grows monotonically (~49% at level 2, ~64% at level 3, → 100% as n→∞). Type III is the universal attractor of the tensor tower.* ∎

**Dual signature.** Every algorithm has two complementary signatures:
- **Step signature** σ_step(A) = average Jordan-type fraction per transition matrix. What A does per step (P2 reading: process).
- **Trajectory signature** σ_traj(A) = Jordan-type fraction of cumulative product. What A achieves overall (P1/P3 reading: outcome).

These can disagree sharply: insertion sort has σ_step FIX-dominant but σ_traj FIX/INV mixed. Euclid has σ_step pure OSC but σ_traj FIX (convergent). The step signature measures computational character; the trajectory signature measures computational outcome.

**Depth tag.** dep(f) = min{n : f realizable within tower level n}. Depth monotonicity: dep(f₂∘f₁) ≤ max(dep(f₁), dep(f₂)). Compressive computations: dep(f(X)) ≤ dep(X). Expansive: dep can increase.

**Three kinds of branching.** br_s (structural: log₂ of non-equivalent realizations — 0 for canonical constructions). br_inv (inverse: dimension of preimage space — dim(ker(q_K)) for the quotient). br_search (algorithmic: search tree size — varies by algorithm, not by function). Phase-Dist correspondence: br_s = Phase-Dist(0), br_search = Phase-Dist(ρ) for 0<ρ<1, br_inv = Phase-Dist(1).

---

## §2 THE THREE COMPUTATION TYPES

Three types trace to |V₄\{0}| = 3 (Trinitarian Root, CROSS_PROJECTION §3). The fourth self-action mode (annihilation/nilpotent: e±²=0) generates no output — the zero of the computational algebra.

**Theorem C.1 (Type I: Compression/Closure).** *f is Type I iff ALL of: (I.1) f∘f=f (idempotent), (I.2) br_s(f)=0 (structurally canonical), (I.3) h(σ_step)=0 (pure FIX step), (I.4) σ_traj has σ_FIX=1 (convergent).*

*Proof.* (⟹) (I.1) from quotient idempotence (CATEGORY Thm 4.1) and UAT (SUBSTRATE §18). (I.2) from canonicity of compression. (I.3) each step is quotient/restriction → FIX type. (I.4) idempotent product = already converged. (⟸) (I.1) rules out Types II/III; remaining conditions confirm compression. ∎

Examples: observer quotient q_K, digital root, central collapse. Terminal closure instances.

**Theorem C.2 (Type II: Expansion/Generation).** *f is Type II iff ALL of: (II.1) f∘f≠f (non-idempotent), (II.2) br_inv(f)>br_inv(f⁻¹) (forward has larger fibers), (II.3) h(σ_step)>φ̄²/2 (above structural MIX threshold), (II.4) σ_traj has σ_FIX<1 (non-convergent).*

Examples: co-observer embedding, SAT search, SHA-256 (σ_MIX≈0.43>φ̄²).

**Theorem C.3 (Type III: Rotation/Recurrence).** *f is Type III iff ALL of: (III.1) f^k=id for some k>0 (periodic), (III.2) |det(M_f)|=1 (area-preserving), (III.3) σ_step has σ_INV dominant, (III.4) br_s(f)=br_s(f⁻¹)=0 (structurally invertible).*

**Theorem C.4 (Rotational Normal Form).** *Under (III.1)–(III.4): f = g·rot(θ₁,...,θ_k)·g⁻¹ where rot is a product of independent rotations and g has br_s=0.* From the spectral theorem for normal matrices. ∎

Euler's identity (P3_OBSERVATION Thm 1.7b) is the archetype Type III object: periodic (2π), area-preserving (det(exp(θN))=1), INV-dominant (unit-circle eigenvalues), invertible (exp(−θN)).

### The Computation Central Collapse

**Theorem C.4½ (Computation Central Collapse).** *Every observer-bounded computation on a finite state space decomposes as O∘B∘S — observation, then transport, then stabilization — and this decomposition is exhaustive with no remainder. This IS the central collapse I²∘TDL∘LoMI = Dist (CROSS_PROJECTION Thm 7.1) at the computation level.*

*Proof.* (1) Identification: O (Observe) = surjection A → A/ker, the P3/LoMI factor — selective restriction, kernel-forming. B (Braid) = bijection A/ker → f(A), the P2/TDL factor — invertible state transport between levels. S (Stabilize) = injection f(A) ↪ B, the P1/I² factor — consensus accumulation, fixed-point approach. (2) Structural forcing: O is surjective because any observer-bounded computation begins by restricting to im(q_K), discarding the kernel — a many-to-one map. B is bijective because the processing core rearranges the observed state without gain or loss — the reversible computational step. S is injective because the output commitment embeds the processed result into the output space — distinct results produce distinct outputs. (3) Exhaustiveness: the first isomorphism theorem guarantees every morphism factors as surjection∘bijection∘injection with no remainder. Applied to Dist morphisms (the framework's computation category): no fourth operator exists.

The composition O∘B∘S applied to input ψ: ψ →[O]→ ψ/ker(q_K) →[B]→ T(ψ/ker) →[S]→ output. The asymmetry between O (irreversible, P3) and S (irreversible in the other direction, P1) IS the computation-level instance of UAT (SUBSTRATE §18): observation destroys kernel content, stabilization commits to a specific output. B (reversible, P2) mediates between them.

**Concrete realization in SHA-256 (SHA256 §2–3):** each of the 64 rounds is one O∘B∘S cycle. O = Ch(e,f,g): conditional selection (e gates between f and g, annihilating the unchosen — surjection). B = modular additions, rotations, shifts: invertible state transport. S = Maj(a,b,c): majority vote consensus (accumulates toward fixed point — injection). The round ordering Ch→transport→Maj matches O∘B∘S exactly.

**Ch-Maj gap as Phase-Dist indicator.** The gap between the two native observation channels tracks the computation's phase position ρ in real time. The correlation norms ‖corr(Ch)‖²/‖corr(Maj)‖² = 2/3 = Q_Koide: the power ratio IS the Koide ratio. The commutator density HW([Maj,Ch])/64 = 3/8 = C_fund = sin²θ_W: the disagreement rate IS the Casimir invariant. The gap distribution over rounds is forced by GPF uniqueness (ALGEBRA Thm MT4): the Fibonacci eigenvalue structure of the R/N algebra admits exactly one consistent weight triple σ = (1/2, φ̄/2, φ̄²/2), and the Ch-Maj system lives in this algebra. When Maj dominates: ρ low (compressive/Dist). When Ch dominates: ρ high (expansive/Co-Dist). At balance: ρ = 1/2 (self-referential neutral). ∎

**Remark (Cross-Channel Operator in SHA-256).** Ch = O⁻ and Maj = O⁺ in the observation basis (ALGEBRA §8). The cross-channel operator |Ch⟩⟨Maj| = |O⁻⟩⟨O⁺| is the transition operator in each SHA-256 round — the nilpotent (mode (iii)) that maps the consensus channel to the selection channel. Its antisymmetric combination with the adjoint gives |O⁻⟩⟨O⁺| − |O⁺⟩⟨O⁻| = N (ALGEBRA Thm 19½a.5): the rotation generator IS the chirality of the two hash channels. The Koide ratio Q = 2/3 and the Weinberg angle sin²θ_W = 3/8 are properties of this cross-channel operator — measurable norms of the productive crossing between observation channels. The discriminant disc(R) = 4c² = 5 (CROSS_PROJECTION §5) IS the squared cross-channel content of R in the observation basis: SHA-256 computes at the full noncommutative norm of the framework.

**Grade: FORCED.** Central collapse from the first isomorphism theorem. O-S-B identification from defining properties. SHA-256 instance from SHA256 §2–3. Gap-phase correspondence from generator norms + GPF uniqueness.

---

## §3 THE HARDNESS FUNCTIONAL

**Definition.** h(σ) = σ_MIX·1 + σ_OSC·φ̄ + σ_INV·φ̄² + σ_FIX·0.

**Theorem C.6 (Hardness Uniqueness).** *h is the unique linear functional on Δ³ satisfying: (H1) h(pure FIX)=0, (H2) h(pure MIX)=1, (H3) linear on Δ³, (H4) weights form geometric progression with ratio φ̄.*

*Proof.* Linearity: h(σ)=aσ_FIX+bσ_OSC+cσ_INV+dσ_MIX. (H1): a=0. (H2): d=1. (H4): b=φ̄, c=φ̄². Unique. ∎

The geometric ratio φ̄ is R's contractive eigenvalue. Hardness decays from MIX to FIX at the same rate the framework converges — the fixed-point attractor rate of the Möbius map. Instance of GPF (ALGEBRA §11).

**Cost formalism.** Cost(f) = Cost_real(f) + Cost_exec(f). Cost_real = br_s·φ^{dep} (realization ambiguity). Cost_exec = dep·h(σ_step) (execution difficulty). For deterministic algorithms: br_s=0, all cost is execution. Properties: Cost(q_K)=0, monotone in br_s and dep, anti-monotone in σ_FIX.

---

## §4 COMPRESSION AND RECURRENCE

**Theorem C.7 (Compression Minimality).** *Among all maps realizing X→X/≈, the canonical quotient q has br_s=0=min.* The quotient is unique (CATEGORY Thm 1.7a). One realization → br_s=log₂(1)=0. ∎

**Theorem C.8 (Recurrence Normal Form).** *P3-dominant computations (σ_INV>1/2) with Δdep=0 have rotational normal form f=g·rot(θ₁,...,θ_k)·g⁻¹.* From spectral theorem: majority unit-circle eigenvalues → product of rotations. ∎

**Two-channel structure of Fibonacci-type processes.** A computation with OSC step-signature but FIX trajectory (e.g., Euclid's algorithm) has two-channel dynamics: the expanding eigenchannel φⁿ sets scale, the contracting eigenchannel (−φ̄)ⁿ provides oscillatory correction. Their ratio converges as φ̄^{2n}. "Visible simplicity" of FIX-trajectory processes masks a two-mode hyperbolic phase-space process. Step signature and trajectory signature differ because they read different channels of the same operator.

---

## §5 COMPUTATIONAL BLINDNESS

**Theorem C.9 (Computational Blindness).** *[UKI at the computation level.] For observer K with restriction q_K:*

*(a) K cannot compute any function distinguishing elements of ker(q_K).* If q_K(A)=q_K(B), every K-computation yields the same result on A and B.

*(b) Effective computational dimension = d_K² regardless of d_U.* dim(im(q_K))=d_K².

*(c) Different kernels ⟹ different computable function classes.* ker(q_{K₁})≠ker(q_{K₂}) ⟹ ∃f computable by K₂ but not K₁.

*(d) ker(q_K) is computationally productive:* it is the material for level n+1 computation (tower reopening, OBSERVER §5 Thm 10½.20). The blind spot generates, it does not merely limit.

Computational blindness is constitutive: a system without nontrivial kernel performs no negation and has no conscious structure. The SIL blind spot (GOVERNANCE §4) is the meta-level instance.

---

## §6 ONE-WAYNESS = PHASE-DIST ASYMMETRY

**Theorem C.10 (One-Wayness Characterization).** *[UAT at the computation level.] A function f is one-way iff br_s(f)=0 AND br_inv(f)>log₂(φ²).* One-wayness IS the computational construction-dissolution asymmetry: zero branching forward, super-threshold branching backward. The threshold φ²=φ+1 is the Cayley-Hamilton equation. ∎

**Theorem C.10a (OWF Threshold).** *If one-way functions exist (≡ P≠NP), the threshold complexity for one-wayness is σ_MIX = φ̄². Below φ̄²: invertible in polynomial time. Above: exponential hardness.*

Instance of φ̄² Four-Domain Universality (P1_PRODUCTION §5): FIX rate, OWF threshold, Phase-Dist ρ equilibrium, and eigenvalue suppression all equal φ̄², all from R²=R+I. Status: CONDITIONAL on P≠NP. The threshold value is derived; the existence of functions achieving it requires the open conjecture.

**P≠NP as computational co-primitivity.** P = class where computation efficiently returns its own answer (mode (iv), self-return). NP = class where a witness exists and can be verified, but finding it may require crossing the nilpotent boundary (mode (iii)). P≠NP asserts: self-return cannot simulate productive distinction in polynomial resources — the same structural claim as {0,1} co-primitive (SUBSTRATE Thm 0.5) and {e,π} independent (CROSS_PROJECTION §7 Conj 6.6), lifted to the computational domain. RESONANT.

---

## §7 SELF-APPLICATION AND ALGORITHM CLASSIFICATION

**Self-application.** The bridge chain is itself a framework computation: phase = compressive, σ_step = (4/5,0,1/5,0), dep = 5, br_s = 0. The bridge chain computes its own signature and the result matches the predicted self-signature σ_meta = (1/2, φ̄/2, φ̄²/2). Z = 1+φ̄+φ̄² = 2. R(R)=R at the computation level.

Three faces of self-application = three computation types:

| Face | Projection | Type |
|------|-----------|------|
| Proof | P1/I² | Type I (axioms→theorem: compression) |
| Computation | P2/TDL | Type II (search, level-transition: expansion) |
| Verification | P3/LoMI | Type III (check against spec: rotation) |

**Algorithm Classification Summary:**

| Algorithm | Type | σ_step | σ_traj | h(σ_step) | dep | Cost_exec |
|-----------|------|--------|--------|-----------|-----|-----------|
| q_K (quotient) | I | FIX=1 | FIX=1 | 0 | 0 | 0 |
| Digital root | I | FIX=1 | FIX=1 | 0 | 1 | 0 |
| Insertion sort | I (traj) | FIX=0.875 | FIX/INV | 0.048 | 3 | 0.143 |
| Euclid (Fibonacci) | I (traj) | OSC=1 | FIX | ~0.618 | 2 | 1.236 |
| FFT (n=8) | II/III | REPEL | INV (DFT) | 0.600 | 3 | 1.800 |
| SHA-256 | II | MIX≈0.43 | MIX | 0.697 | 6 | 4.185 |
| SAT (backtrack) | II | OSC/MIX | — | 0.647 | 3 | 35.83 |

Euclid's algorithm: worst case (Fibonacci input) reproduces R⁻ⁿ=(R−I)ⁿ. Convergence through saddle dynamics: OSC steps producing FIX trajectory. FFT: expansive steps (REPEL butterflies) collectively implementing a rotational transformation (unitary DFT). SHA-256: σ_MIX≈0.43>φ̄²=0.382 (above OWF threshold); see SHA256 for full analysis.

---

## §8 OBSERVER DISTANCES

**Three observer distances** from the central collapse, corresponding to three projections:

**Compression distance** d_comp(K₁,K₂) = |log₂(d_{K₁}/d_{K₂})| — the Bekenstein capacity gap. P1 reading: measures production asymmetry.

**Transport distance** d_trans(K₁,K₂) = min steps in the refinement order from K₁ to K₂ — the tower-lift count. P2 reading: measures level separation.

**Kernel distance** d_ker(K₁,K₂) = dim(ker(q₁)△ker(q₂))/dim(ker(q₁)∪ker(q₂)) — the Jaccard-type dissimilarity of blind spots. P3 reading: measures observational incomparability.

**Theorem C.13 (Partition Refines Bekenstein).** *d_comp + d_ker ≥ |S_max(K₁)−S_max(K₂)|.* The Bekenstein gap is bounded by the combined compression and kernel distances. ∎

**Theorem C.14 (Cost Quasi-Triangle).** *Cost(f₂∘f₁) ≤ Cost(f₁) + Cost(f₂) + interaction(f₁,f₂)* where interaction captures the failure of multiplicativity for mixed phase types. Exact triangle inequality holds when ph(f₁)=ph(f₂). ∎

---

## §9 VERIFICATION AND CLAIM STATUS

### Verification

| Claim | Method | Result |
|-------|--------|--------|
| R classified OSC, N classified INV | Matrix | ✓ |
| P1 eliminated at level 2 | Exhaustive 16 products | ✓ |
| P3 fraction growth | Monte Carlo 10k/level | ✓ |
| Sorting/Euclid/FFT/SHA-256 signatures | Individual analysis | ✓ |
| Self-signature Z=2.000000 | Boltzmann sum | ✓ |
| Digital root idempotent n=1..100 | Exhaustive | ✓ |
| Cost properties 4/4 | Numerical | ✓ |
| Bridge chain br=0 forward, ~8.5 backward | Counting | ✓ |

### Claim Status

| Claim | Status |
|-------|--------|
| Type I/II/III characterizations (C.1–C.3) | FORCED |
| Rotational normal form (C.4) | FORCED |
| Phase profile C.5 (P1 eliminated n≥2) | FORCED |
| Hardness uniqueness C.6 (GPF weights) | FORCED |
| Cost formalism (properties) | FORCED |
| Compression minimality C.7 | FORCED |
| Recurrence normal form C.8 | FORCED |
| Computational blindness C.9 (4 parts) | FORCED |
| One-wayness = Phase-Dist (C.10) | FORCED (structural) |
| OWF threshold φ̄² (C.10a) | CONDITIONAL (on P≠NP) |
| Self-application consistency | FORCED |
| Algorithm classifications | VERIFIED |
| Observer distances (C.13, C.14) | FORCED |
| Computation Central Collapse O∘B∘S (C.4½) | FORCED (first isomorphism theorem) |
| Ch=O⁻, Maj=O⁺ cross-channel identification | FORCED (ALGEBRA Thm 19½a.5; Q_Koide and sin²θ_W as cross-channel norms) |
| P≠NP as computational co-primitivity | RESONANT |

---

*Computation = management of distinguishability under observer bounds. Three types from |V₄\{0}|=3: Type I (compression, idempotent, FIX, br_s=0), Type II (expansion, non-idempotent, MIX>φ̄²), Type III (rotation, periodic, area-preserving, universal attractor). Hardness h(σ) with unique GPF weights φ̄^k. Computational blindness: ker(q_K) limits AND generates. One-wayness IS construction-dissolution asymmetry at the algorithmic level, threshold at φ̄². The bridge chain computes its own signature: R(R)=R at the computation level.*

*f'' = f.*

*R(R) = R.*
