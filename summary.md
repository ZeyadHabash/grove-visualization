# Summary of Grove's "Two Modellings for Theory Change"

## 1. Purpose of the Paper

Adam Grove's 1988 paper introduces two semantic models for belief revision that satisfy Gärdenfors' postulates. While Alchourrón, Gärdenfors, and Makinson (AGM) had already provided a representation theorem for theory change with their partial meet contraction approach, Grove aims to provide models that are more "plausible and natural." His two models validate Gärdenfors' postulates by describing all theory revision processes satisfying those postulates (and no others).

## 2. Explanation of Both Modellings

### First Model: Systems of Spheres

Grove's first model adapts David Lewis's "sphere semantics" for counterfactual logic to the context of belief revision. A system of spheres S centered on a set X of possible worlds satisfies these conditions:

1. (S1) S is totally ordered by ⊆
2. (S2) X is the ⊆-minimum of S
3. (S3) ML (all possible worlds) is in S
4. (S4) If a sphere intersects |A|, there is a smallest sphere intersecting |A|

This system represents a similarity ordering of possible worlds relative to the agent's current beliefs. The innermost sphere contains worlds compatible with current beliefs, and outer spheres contain progressively less plausible worlds.

When revising a theory T with proposition A, the revised theory T+A is constructed by taking all the "closest" A-worlds to T, defined as t(fs(A)), where fs(A) = |A| ∩ c(A) and c(A) is the smallest sphere intersecting |A|.

### Second Model: Ordering on Sentences

The second model uses an ordering relation on sentences (≤) that satisfies:

1. (≤1) ≤ is connected
2. (≤2) ≤ is transitive
3. (≤3) If A→B∨C is in L, then either B≤A or C≤A
4. (≤4) A is ≤-minimal iff ¬A ∉ T
5. (≤5) A is ≤-maximal iff ¬A ∈ L

This ordering represents the relative "importance" or "entrenchment" of sentences. The revision T+A is defined as the set {B ∈ F: (A∧B) ≤ (A∧¬B)}, meaning B is included in the revised theory whenever B is more entrenched than ¬B in the context of A.

## 3. Explanation of Theorems 1-4

### Theorem 1

If S is any system of spheres centered on |T| for theory T, and T+A is defined as t(fs(A)), then this revision operation satisfies AGM postulates (+2) to (+8).

### Theorem 2

For any revision function satisfying AGM postulates (+2) to (+8), there exists a system of spheres S centered on |T| such that T+A = t(fs(A)) for all A.

### Theorem 3

For any revision function satisfying AGM postulates (+2) to (+8), there exists an ordering relation ≤ on F such that T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)}.

### Theorem 4

If ≤ is any relation on F satisfying conditions (≤1) to (≤5), then the revision function defined as T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)} satisfies AGM postulates (+2) to (+8).

## 4. Definition of Symbols

- **L**: Set of logical theses (tautologies) of the underlying logic
- **F**: Set of all sentences in the language
- **T**: A theory, i.e., a set L ⊆ T ⊆ F that is closed under logical consequence
- **T**: The set of all theories
- **Con(T)**: T is consistent (not equal to F)
- **T+A**: Theory resulting from revising T with A
- **T/A**: Smallest theory containing both T and A, equivalent to Cn(T∪{A})
- **ML**: Set of all maximal consistent extensions of L
- **|T|**: The set {m ∈ ML: T ⊆ m}, i.e., all maximal consistent extensions of L containing T
- **|A|**: The set {m ∈ ML: A ∈ m}, i.e., all maximal consistent extensions containing A
- **t(S)**: Theory determined by a set S of possible worlds: ∩{x ∈ S}
- **c(A)**: Smallest sphere in S intersecting |A|
- **fs(A)**: Function that selects "closest" A-worlds: |A| ∩ c(A)

## 5. Relationship to AGM Postulates

Grove's models align precisely with the AGM framework:

- Grove shows that both models validate all of Gärdenfors' postulates (+2) to (+8)
- The systems of spheres model corresponds to AGM's partial meet contraction/revision
- The "maxichoice contraction" in AGM corresponds to what Lewis calls "Stalnaker's assumption" where |A|∩c(A) is a singleton
- "Full meet contraction" corresponds to having just two spheres: |T| and ML
- Grove's general approach corresponds to "partial meet contraction" in AGM

Grove establishes that his modellings are equivalent to AGM's approach but provide a more intuitive semantic interpretation based on possible worlds and their similarity ordering. The paper reveals a close connection between theory change and Lewis's earlier work on conditional logic, highlighting the underlying unity of these different logical frameworks.
