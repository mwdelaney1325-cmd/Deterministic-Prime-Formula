> This file is a verbatim mirror of README.md.  
> README.md is the authoritative specification.
# Deterministic Admissibility Construction

Executable specification defining a deterministic mapping from a discrete
input domain to integer outputs with a multiplicity-based admissibility
partition.

No query is posed by this document.

---

## 1. Domain

Let \( i \in \mathbb{N} \) index a deterministic enumeration of primitive
Pythagorean triples

\[
T(i) = (A(i), B(i), C(i))
\]

such that

\[
A(i)^2 + B(i)^2 = C(i)^2,
\qquad
\gcd(A(i), B(i), C(i)) = 1,
\qquad
A(i), B(i), C(i) \in \mathbb{Z}_{>0}.
\]

Enumeration order is fixed and deterministic.

---

## 2. Carrier

Define

\[
K(i) := \frac{A(i)\,C(i)}{B(i)} \in \mathbb{Q}.
\]

---

## 3. Readout

Define

\[
L(i) := \lfloor K(i) \rfloor \in \mathbb{Z}_{\ge 0}.
\]

---

## 4. Multiplicity

Define

\[
\mu(x) := \#\{\, i \mid L(i) = x \,\}.
\]

---

## 5. Admissibility

Define

\[
\mathrm{Adm}(x) :=
\begin{cases}
1 & \text{if } \mu(x) = 1, \\
0 & \text{otherwise}.
\end{cases}
\]

---

## 6. Admissible Set

Define

\[
\mathcal{A} := \{\, x \in \mathbb{Z}_{\ge 2} \mid \mathrm{Adm}(x) = 1 \,\}.
\]

---

## 7. Execution Protocol (Finite Range)

Given a finite bound \( C_{\max} \):

1. Enumerate all \( T(i) \) with \( C(i) \le C_{\max} \).
2. Compute \( K(i) \) and \( L(i) \).
3. Compute multiplicities \( \mu(x) \).
4. Extract \( \mathcal{A} \).

---

## 8. Observed Property (Finite Ranges)

For all tested finite bounds:

- \( \mathcal{A} \) consists of isolated integer outputs.
- Raw outputs include both composite and non-composite values.
- Admissibility depends only on multiplicity.

---

## 9. Notes

- Construction and execution of the system are fully contained in this document.
- If the system is constructed and produces an output, it guarantees that
  geometry was not used in the readout.
- Accordingly, geometric axioms, geometric interpretations, or geometric
  constraints are inadmissible when applying verification to the outputs.
- No divisibility predicates are evaluated.
- No sieves are applied.
- No ordering, density, or completeness claims are asserted.
- Execution is reproducible by humans or machines.

---

End of specification.
