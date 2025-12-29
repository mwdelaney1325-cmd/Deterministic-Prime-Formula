# Verification

This document records the scope and method of finite-range verification for the construction defined in `prime_formula.md`.

No claims of completeness, infinitude, or asymptotic behavior are made here.

---

## Verification Scope

The construction was evaluated over a finite initial segment of the primitive input domain.

- **Input domain:** primitive Pythagorean triples \(T(i) = (A,B,C)\) under a fixed deterministic enumeration.
- **Evaluation range:** all \(T(i)\) with \(C \leq C_{\max}\), where \(C_{\max}\) is explicitly bounded in the implementation.
- **Carrier computation:** the same fixed algebraic rule was applied uniformly to all inputs in range.
- **Control conditions:** no parameter tuning, branching logic, or adaptive filtering was used.

---

## Verification Criteria

For each evaluated index \(i\):

1. Compute the carrier value \(K(i) \in \mathbb{Q}\).
2. Compute the integer readout  
   \[
   L(i) := \lfloor K(i) \rfloor .
   \]
3. Compute multiplicity  
   \[
   \mu(x) := \#\{\, i \mid L(i) = x \,\}.
   \]
4. Declare \(x\) **admissible** if and only if \(\mu(x) = 1\).

---

## Observed Results (Finite Range)

Over the tested range:

- Every admissible value \(x\) is a prime number.
- No composite number is admissible.
- No divisibility tests, sieves, or primality checks were used at any stage.
- Admissibility depended only on internal multiplicity, not on numerical properties of \(x\).

These statements are empirical and limited strictly to the verified range.

---

## Non-Claims

This verification does **not** assert:

- That all primes appear.
- That infinitely many admissible values exist.
- That admissible values follow any density, spacing, or distribution law.
- That behavior observed in the verified range persists beyond it.

Such questions are intentionally left open.

---

## Reproducibility

The verification is fully reproducible given:

- The fixed enumeration of the input domain.
- The fixed algebraic definition of the carrier.
- The multiplicity-based admissibility criterion.
- The explicit bound \(C \leq C_{\max}\).

No external data, heuristics, or analytic assumptions are required.
