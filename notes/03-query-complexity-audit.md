# Research Note 03 — Query-Complexity Audit

## 2026-09-18

We audited the proposed "bounded/nonadaptive witness finding" direction against the literature.

Kawachi, Rossman, and Watanabe proved an information-theoretic lower bound of Omega(n^2) for nonadaptive randomized witness finding with NP queries in a black-box model. The same work gives matching O(n^2) upper bounds. A later/related formulation also studies affine witness sets, which are especially relevant because every affine subspace of {0,1}^n can be represented by a polynomial-size system of linear equations.

## Important limitation

This does NOT prove P != NP.

The lower bound is for a black-box witness set W and a restricted query model. A concrete SAT algorithm receives an explicit formula encoding W and may exploit its structure. Therefore the black-box lower bound cannot simply be transferred to unrestricted polynomial-time SAT algorithms.

## Useful verified fact

For the unrestricted black-box model:
- deterministic adaptive search can use n queries;
- nonadaptive randomized search has an Omega(n^2) lower bound for NP queries;
- an O(n^2) nonadaptive upper bound is known.

So the gap between adaptive and nonadaptive access is real in that model, but it is already understood.

## New research target

We should now investigate whether a **computationally natural restriction on SAT instances or query circuits** can make the black-box lower bound transfer to an explicit, polynomial-size SAT family.

A promising subtarget is:

> Find a natural polynomial-size family of SAT formulas whose satisfying-assignment sets are affine subspaces, and characterize exactly which polynomial-time nonadaptive query circuits can recover a witness.

Any theorem here must be compared against the known affine-subspace lower bounds before being called new.

## Anti-overclaim rule

A black-box lower bound is not a circuit lower bound.

A query lower bound is not automatically a time lower bound.

A lower bound for affine formulas is not automatically a lower bound for all SAT.

Status: KNOWN BASELINE / RESEARCH TARGET OPEN.
