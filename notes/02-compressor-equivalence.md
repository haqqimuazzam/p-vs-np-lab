# Research Note 02 — Candidate Compressor Equivalence

## Key observation

Define a polynomial-time candidate compressor for SAT as a polynomial-time function f that, on every satisfiable formula phi with n variables, outputs at most p(n) assignments and guarantees that at least one output assignment satisfies phi.

### Lemma

Such an f exists if and only if P = NP.

### Proof: f => P = NP

Given phi:
1. Compute A = f(phi).
2. Verify every assignment a in A directly against phi.
3. Accept iff one verifies.

The output contains polynomially many assignments and each verification is polynomial, so SAT is in P. Since SAT is NP-complete, P = NP.

### Proof: P = NP => f

If P = NP, SAT is decidable in polynomial time. SAT is self-reducible, so a polynomial-time SAT decider can construct a satisfying assignment by fixing variables one at a time. Therefore define f(phi) to output that one assignment when phi is satisfiable, and an empty list otherwise. This is polynomial-time.

Hence the candidate-compressor existence statement is equivalent to P = NP.

## Consequence for PSRL

The earlier target

"for every polynomial-time candidate compressor f, construct a satisfiable phi_f for which f(phi_f) contains no satisfying assignment"

is not a weaker intermediate theorem.

If a compressor exists, the target immediately contradicts its defining guarantee. If no compressor exists, the universal statement is vacuously true.

Therefore, under the exact quantifiers, PSRL is equivalent in strength to P != NP.

This is a crucial negative result: diagonalizing an arbitrary polynomial-time witness finder is not a shortcut around P vs NP.

## Research pivot

Do not spend the main effort trying to prove unrestricted PSRL.

Instead investigate restrictions or structural properties where:
- the theorem is genuinely weaker than P != NP;
- the restriction is mathematically meaningful;
- the resulting lower bound is not already known;
- the theorem could plausibly be strengthened later.

Candidate directions:
1. restricted circuit classes for SAT search;
2. bounded-query/nonadaptive witness finding;
3. proof systems and automatizability;
4. explicit SAT families with provable search lower bounds;
5. structural invariants preserved under self-reduction.

Status: PROVED (equivalence lemma); research pivot OPEN.
