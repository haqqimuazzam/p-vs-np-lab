# P vs NP Lab

A rigorous, falsifiable research laboratory for studying the P vs NP problem.

## Mission
We do not assume P = NP or P != NP. Every proposed argument is treated as a conjecture until its definitions, quantifiers, complexity bounds, and proof obligations have been checked.

We prioritize explicit mathematics, proof audits, counterexample searches, formal verification, and recording failed approaches.

## Current research target
Polynomial Self-Reference Lemma (PSRL).

Given a polynomial-time candidate-set function f for SAT, can we construct in polynomial time a satisfiable formula phi_f such that f(phi_f) contains no satisfying assignment of phi_f?

A successful proof could yield P != NP. This lemma is OPEN here; no proof is claimed.

## Rules
1. Never label an argument a proof until every step is justified.
2. Distinguish syntax equality from semantic or computational equivalence.
3. Track input lengths and polynomial exponents explicitly.
4. Finite experiments can falsify universal claims but cannot prove them.
5. External papers are sources to audit, not premises.
6. Record failed approaches.
7. No circular use of P = NP, P != NP, or equivalent unproved statements.
8. No hidden oracle, nonuniform advice, or unbounded search disguised as polynomial time.

## Status
- P vs NP: OPEN
- PSRL: OPEN
- Finite candidate-list exclusion: PROVED
- Unrestricted literal fixed-point claim for the diagonal construction: DISPROVED
