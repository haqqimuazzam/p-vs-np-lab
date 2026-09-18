# P vs NP Lab

A rigorous, falsifiable research laboratory for studying the P vs NP problem.

## Mission
We do not assume P = NP or P != NP. Every proposed argument is treated as a conjecture until its definitions, quantifiers, complexity bounds, and proof obligations have been checked.

We prioritize explicit mathematics, proof audits, counterexample searches, formal verification, and recording failed approaches.

## Current research target
The first diagonalization idea has now been audited. Its unrestricted fixed-point form is invalid, and the stronger "candidate compressor" formulation is essentially equivalent to P vs NP rather than an easier intermediate theorem.

The next goal is to identify a strictly weaker structural theorem whose proof would still give new information about SAT but would not simply restate P != NP.

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
- Finite candidate-list exclusion: PROVED
- Arbitrary syntactic fixed point for the diagonal construction: DISPROVED
- Compressor formulation as a route to P != NP: equivalent in strength to the target; not an independent proof
