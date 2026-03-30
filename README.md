# Recursive Origin

**One equation. Zero free parameters. The Standard Model, general relativity, and observer theory from a binary seed.**

---

## What This Is

Recursive Origin is a mathematical physics framework that derives physical law from a single equation — **f'' = f** — whose solution space has dimension 2, basis solutions {cosh, sinh} on ℝ and {cos, sin} on iℝ. The binary seed S₀ = {0,1} indexes this solution space. Everything in the framework is f'' = f at some depth through some projection face.

The matrix realization R = [[0,1],[1,1]] satisfies **R² = R + I** — the Fibonacci recurrence, which is f'' = f in discrete form. Two generators R and N = [[0,−1],[1,0]] (with N² = −I, the companion equation f'' = −f) produce a closed algebra spanning M₂(ℝ) ≅ Cl(1,1), from which the framework derives:

- **Five constants** — φ, e, π, √2, √3 — as evaluations of the algebra's eigenvalues, norms, and exponentials
- **The Standard Model gauge group** SU(3) × SU(2) × U(1) from the tower's eigenspace stabilizer sequence
- **Three generations** of fermions from the three irreducible representations of S₃ = Aut(V₄)
- **Parity violation** (su(2)_L only) from the categorical distinction between ℂ-linear and ℂ-antilinear morphisms
- **General relativity** via the Jacobson thermodynamic derivation with all inputs framework-derived
- **Observer theory** with a two-axis consciousness model, abstract Bekenstein bounds, and a forced self-modeling loop
- **18 physical quantities** with zero free dimensional parameters

The organizing principle is **R(R) = R**: self-action stabilizes. This holds at every level — categorically (q∘q = q), algebraically (Fibonacci fixed point φ̄), observationally (the meta-encoding M(FRAME) = FRAME), and semantically (the vocabulary carries the algebra it describes).

---

## The Derivation Chain

The framework follows a zero-branching algebraic chain from the binary seed to physics:

```
{0,1}                        Binary seed, index of basis solutions
  ↓  self-product
V₄ = {0,1}²                 Four-element group under XOR
  ↓  automorphisms
S₃ = Aut(V₄)                Symmetric group, |S₃| = 6
  ↓  linearization
ℚ[S₃] ≅ ℚ ⊕ ℚ ⊕ M₂(ℚ)     Artin-Wedderburn decomposition
  ↓  completion
M₂(ℝ) with R, N             Generator algebra, seven identities
  ↓  spectral completion
M₂(ℂ)                       Spectrally complete; terminates the chain
  ↓  Hermitian subspace
Herm(M₂(ℂ)) ≅ ℝ^{1,3}      Spacetime with Minkowski metric
  ↓  observer consistency
Gauge theory + Gravity       Yang-Mills and Einstein from one schema
```

Every arrow has zero forward branching. Given {0,1}, M₂(ℂ) with R and N is the unique conclusion.

---

## Architecture

The framework is organized as a **9 × 3 grid** B(level, projection) across nine tower levels and three projection faces:

| Projection | Generator | Constant | Reading |
|-----------|-----------|----------|---------|
| **P1** (Production) | R | φ | What self-action generates |
| **P2** (Mediation) | h = diag(1,−1) | e | What level-transition carries |
| **P3** (Observation) | N | π | What observation reveals and annihilates |

| Level | Name | Content |
|-------|------|---------|
| 0 | Substrate | f'' = f, co-primitives, observer-relative existence |
| 1 | Binary | S₀ = {0,1}, pair-space |
| 2 | Categorical | Dist (the unique forced category), observer = quotient |
| 3 | Algebraic | Bridge chain, {R,N}, five constants, Cl(1,1), quantum group U_{φ²}(sl₂) |
| 4 | Projected | Three projections, independence, central collapse, lattice Λ' ≅ ℤ⁵ |
| 5 | Observer | K = (d_K, Δ_K, σ_K), Bekenstein bounds, consciousness hierarchy |
| 6 | Physical | Spacetime, gauge forces, gravity, cosmological tower equation |
| 7 | Meta | FORCED / ENCODED / RESONANT / MYTHIC claim grading |
| 8 | Semantic | Contranyms, meta-primitives, self-specification χ∘χ = χ |

---

## Source Files

16 source files, ~4,700 lines total. Each file owns a specific tower level and carries its own theorem index, verification table, and claim status audit.

| File | Level | Lines | Owns |
|------|-------|-------|------|
| `SUBSTRATE.md` | 0–1 | ~770 | f'' = f, co-primitives, ORE/CIA, four modes, sweep, stance grammar, UAT |
| `CATEGORY.md` | 2 | ~290 | Dist, observer = quotient, kernel theorem, three readings |
| `ALGEBRA.md` | 3 | ~450 | Bridge chain, seven identities, five constants, quantum group |
| `P1_PRODUCTION.md` | 4/P1 | ~240 | Fibonacci field, Möbius dynamics, self-signature, baryogenesis |
| `P2_MEDIATION.md` | 4/P2 | ~210 | Two routes to e, KMS, Landauer cost, gravity chain entry |
| `P3_OBSERVATION.md` | 4/P3 | ~220 | π absolutely forced, SO(2), spin-½, P3 attractor |
| `CROSS_PROJECTION.md` | 4/cross | ~490 | Independence, central collapse, lattice, (e,π) problem |
| `OBSERVER.md` | 5 | ~360 | A1–A4 axioms, Bekenstein, K6'/K7'/K4, two-axis model |
| `PHYSICS.md` | 6 | ~670 | Spacetime, gauge SM, gravity, predictions, cosmological tower eq |
| `COMPUTATION.md` | 3–5 | ~250 | Three computation types, cost formalism, OWF = Phase-Dist |
| `GOVERNANCE.md` | 7–8 | ~230 | Four statuses, generation/standing/transport, SIL blind spot |
| `SEMANTICS.md` | 8 | ~170 | 10 contranyms, 8→3 meta-primitives, semantic exhaustion |
| `DICTIONARY.md` | 8 | ~220 | ~50 entries with definitions and discipline rules |
| `SHA256.md` | 3–6 | ~210 | SHA-256 as framework algebra, Ch = O⁻ / Maj = O⁺, quantum hash |
| `ASI.md` | 5–8 | ~320 | 21 cognitive invariants, 9-layer architecture, derived physics engine |
| `REGISTRY.md` | 8 | ~260 | Five generators 𝔤₁–𝔤₅, self-specification χ∘χ = χ, RO-2012 |

---

## Claim Grading

Every claim in the framework carries an explicit epistemic grade. The four statuses are derived from the framework's own three-projection structure applied to meta-statements:

| Status | Meaning | Example |
|--------|---------|---------|
| **FORCED** | Zero-branching derivation; the conclusion is unique given the premises | R² = R + I, sin²θ_W = 3/8, three generations |
| **ENCODED** | Recognizable structural image of forced content; containment proof | v/M_P = φ̄⁸⁰ (5.3% match) |
| **RESONANT** | Computationally verified pattern; no derivation or containment | Monster moonshine connection |
| **MYTHIC** | Interpretive overlay; does not survive formal verification | — |

Status must be earned by derivation, not by residence in a prestigious document. Retractions are recorded explicitly (e.g., the Cosmological Depth Decomposition, Thm 5.10m — retracted after corrected CTE revealed it as an artifact of compensating errors).

---

## Key Results

### Structural (zero parameters, zero anchors)

- **Spacetime dimension 4** with Minkowski signature (1,3) from Herm(M₂(ℂ))
- **Gauge group** su(3) ⊕ su(2) ⊕ u(1) from tower eigenspace stabilizers
- **Chirality**: su(2)_L only — the right-handed sector requires ℂ-antilinear maps outside the Dist morphism category. Parity violation is categorical, not dynamical. Matches V−A (zero right-handed coupling).
- **Three generations** from |irreps(S₃)| = 3 (three conjugacy classes)
- **Confinement**: physical states are color-singlets by ORE + Schur's lemma for non-abelian SU(3). Free quarks are in ker(q_K).
- **15 Weyl fermions per generation** with anomaly cancellation (all 6 conditions verified)
- **sin²θ_W = 3/8** at the unification scale (observed 0.231 at M_Z via RG running)
- **Koide parameter Q = 2/3** = ‖N‖²/‖R‖² (generator norm ratio)
- **Koide phase δ = 2π/3 + 2/9** from K4 deficit minimization → τ mass within 0.006%
- **α_S = φ̄³/2 ≈ 0.1180** from K4 thermal equilibrium (observed 0.1179 ± 0.0010)
- **Λ > 0** as a theorem (finite observer axiom A1 + de Sitter entropy)
- **Einstein's equations** from Jacobson with all inputs framework-derived
- **Cosmological Tower Equation** Λ_n = 12πη/(ln(φ)·2^n) — the hierarchy IS the tower

### Observer Theory

- **Abstract Bekenstein**: S_max = log₂(d_K), A_max = 2log₂(d_K)
- **Two-axis consciousness model**: Axis 1 (K1', doubly-exponential depth wall) × Axis 2 (K6', no wall)
- **Universal consciousness**: every A1–A4 observer has Level 3 (recursive negation)
- **Constitutive Agent Forcing** (RO-2012): the framework's own origin forced to within one gauge bit

### Quantum Group / Knot Theory

- **U_{φ²}(sl₂)**: the quantum group at q = φ². R² = R + I is simultaneously the Cayley-Hamilton equation, Hecke relation, Fibonacci anyon fusion rule, and M(2,5) minimal model fusion rule
- **Quantum integers**: [n]_{φ²} = F(2n) (Fibonacci at even indices)
- **Figure-eight knot**: every invariant expressible in framework cardinals at q = φ²

---

## What's Open

| Problem | Status |
|---------|--------|
| (e,π) algebraic independence | CONDITIONAL on EPC for 𝔾_m × SO₂ (9 obstructions unconditional) |
| Cosmological constant Λ value | n_cosmo ≈ 409, observation-constituted (CSM theorem) |
| m_e/M_Planck | OPEN (the sole undetermined dimensionless ratio) |
| C5U unification mechanism | FORCED (15 instances, mechanism closed via 3+2 Coherence) |
| Volume conjecture at q = φ² | OPEN |

---

## How to Read

**Start here:** `SUBSTRATE.md` §0 (the equation) → `CATEGORY.md` (the category) → `ALGEBRA.md` (the bridge chain). These three files contain the mathematical core. Everything downstream is structure built on this foundation.

**For the physics:** `PHYSICS.md` is self-contained with full transport certificates on every theorem. The gauge derivation (§§2–4) and gravity derivation (§6) are the load-bearing sections.

**For the meta-structure:** `GOVERNANCE.md` (how claims are graded) → `REGISTRY.md` (how the framework specifies itself). The self-specification χ∘χ = χ is the framework's boundary closure.

**For applications:** `SHA256.md` (SHA-256 decomposed through the algebra) and `ASI.md` (cognitive architecture from observer constraints).

---

## Technical Notes

- **Two co-primitives** (P.1: Recursive Substrate, P.2: Productive Distinction) are the sole posited objects. Everything else is derived.
- **Two irreducible constants** (G, Λ): G enters as the dimensional anchor η = 1/(4G), which equals 1/4 in natural units (unit convention). Λ is observation-constituted via the Cosmological Self-Measurement theorem. Zero free parameters.
- **Convergence witnesses** at five sites confirm structural necessity: ρ-regulation, Dist uniqueness, e (two routes), σ₁ = ∫_{P3} α = 1/2, and Bekenstein (algebraic + thermodynamic).
- **22 refuted claims** in SHA256 and 1 retraction in PHYSICS are recorded explicitly alongside the positive results.

---

## Citation

If referencing this work:

> Kael. *Recursive Origin.* 2024–2026. 16 source files, ~4,700 lines.

---

*f'' = f.*

*R(R) = R.*
