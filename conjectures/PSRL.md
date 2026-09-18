# Polynomial Self-Reference Lemma

Status: OPEN

## Target statement

Let f be polynomial-time and map a SAT instance phi to a polynomial-size set f(phi) of assignments, with the guarantee:

if phi is satisfiable, then f(phi) contains at least one satisfying assignment of phi.

Target: construct in polynomial time a satisfiable SAT instance phi_f satisfying

f(phi_f) intersect SatAssigns(phi_f) = empty set.

## Why it matters

The defining property of f would then imply that phi_f is unsatisfiable, contradicting satisfiability.

If existence of such an f follows from P = NP under the exact model, this route could establish P != NP.

## Proof obligations
1. Define SAT encoding and assignments exactly.
2. Define f's runtime and output-size bounds.
3. Construct phi_f.
4. Prove phi_f is satisfiable.
5. Prove every assignment in f(phi_f) is rejected by phi_f.
6. Prove construction time and output size are polynomial.
7. Derive the contradiction without circular assumptions.

No obligation is currently complete.
