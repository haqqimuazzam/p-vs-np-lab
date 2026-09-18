# Diagonalization Audit

## Finite-list exclusion

Let f(phi) output a finite set A of assignments on n variables.

For each assignment a define C_a(x) = OR_i (x_i != a_i). C_a is false exactly on a.

Define D_A(x) = AND over a in A of C_a(x).

Thus every a in A is excluded. If A and n are polynomially bounded, D_A has polynomial size.

This part is valid.

## Tempting self-reference

A tempting construction is phi = B AND D_{f(phi)}, where B is satisfiable.

If a polynomial-size, polynomial-time constructible fixed point existed for the relevant class of f, the candidate-set guarantee would be contradicted.

## Critical distinction

A recursion theorem normally supplies a program/index that is behaviorally equivalent to a transformed program. It does not automatically supply literal string equality Encode(phi) = T_f(Encode(phi)).

Confusing semantic equivalence with literal syntactic fixed points is a proof gap.

## Counterexample to arbitrary syntactic fixed points

Let B_n be x_1 OR ... OR x_n.

Define f(phi):
- if phi is exactly B_n, output {1^n};
- otherwise output the empty set.

Let T_f(phi) = B_n AND D_{f(phi)}.

If phi != B_n, T_f(phi) = B_n != phi.
If phi = B_n, T_f(phi) = B_n AND D_{1^n} != B_n.

Therefore this T_f has no literal syntactic fixed point.

This does not prove P != NP because this f is not a SAT candidate compressor.

Status: OPEN for the compressor-specific question.
