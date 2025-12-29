# Examples

This document provides a small number of explicit examples illustrating the construction
defined in `prime_formula.md`.

These examples are included for concreteness only.  
They are not used as evidence for any general claim.

---

## Example Format

Each example consists of:

- A primitive Pythagorean triple \( T(i) = (A,B,C) \).
- The corresponding carrier value \( K(i) \in \mathbb{Q} \).
- The integer readout \( L(i) := \lfloor K(i) \rfloor \).
- The observed multiplicity of \( L(i) \) within the tested range.

Only admissible values (\( \mu(L(i)) = 1 \)) are listed here.

---

## Sample Admissible Outputs

| \(T(i) = (A,B,C)\) | \(K(i)\) (carrier) | \(L(i)\) | Admissible |
|-------------------|-------------------|---------|------------|
| (33, 56, 65)      | rational          | 109     | yes        |
| (45, 28, 53)      | rational          | 101     | yes        |
| (55, 48, 73)      | rational          | 107     | yes        |
| (77, 36, 85)      | rational          | 97      | yes        |
| (75, 308, 317)    | rational          | 149     | yes        |

(All listed \( L(i) \) values are prime.)

---

## Notes

- Carrier values are rational by construction.
- No divisibility tests or primality checks are performed.
- The examples shown here are not exhaustive.
- Composite values do occur as readouts, but always with multiplicity greater than one
  within the tested range, and are therefore excluded by the admissibility criterion.

---

## Purpose of This File

This file exists solely to provide concrete reference points for readers and reviewers.

All formal definitions, claims, and limitations are contained in:

- `prime_formula.md`
- `verification.md`
