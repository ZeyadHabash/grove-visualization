# Detailed Explanation of Grove's "Two Modellings for Theory Change"

## 1. Purpose and Context of the Paper

Grove's 1988 paper addresses a fundamental need in the theory of belief revision: providing intuitive semantic models that characterize Gärdenfors' postulates for belief change. While Alchourrón, Gärdenfors, and Makinson (AGM) had established a syntactic representation theorem through their partial meet contraction approach, Grove notes Segerberg's critique that this representation wasn't "entirely satisfactory" because it lacked "models that are plausible and natural."

Grove's contribution is significant for several reasons:

1. He connects belief revision to David Lewis's work on counterfactual logic, revealing underlying unity between these logical frameworks
2. He provides two equivalent but conceptually distinct models:
   - A "systems of spheres" model that offers a geometric/visual interpretation
   - An "ordering on sentences" model that more directly captures belief entrenchment
3. He proves that both models are equivalent to AGM's approach, showing that all three capture exactly the class of revision functions satisfying postulates (+2) through (+8)
4. He demonstrates that different variants of AGM's approach (maxichoice, full meet, partial meet) correspond to special cases in his framework

## 2. Systems of Spheres Model - Detailed Explanation

Grove's first model adapts Lewis's "sphere semantics" for counterfactuals to belief revision. This provides a visual and intuitive way to understand belief change based on possible worlds.

### Mathematical Definition

A system of spheres S centered on a set X of possible worlds must satisfy:

1. **(S1) Total ordering**: If U and V are spheres in S, then either U ⊆ V or V ⊆ U (spheres are nested)
2. **(S2) Minimum element**: X is the smallest sphere in S (innermost sphere)
3. **(S3) Maximum element**: ML (the set of all possible worlds) is in S (outermost sphere)
4. **(S4) Limit assumption**: If any sphere intersects |A|, then there exists a smallest such sphere

### Conceptual Interpretation

Imagine concentric circles representing degrees of plausibility:

- The innermost sphere contains worlds compatible with current beliefs
- Moving outward corresponds to increasingly implausible worlds
- When new information A arrives, we find the closest A-worlds to our current beliefs

This can be interpreted as a similarity ordering where worlds closer to the center are more similar to what we currently believe is the case.

### Formal Revision Process

When revising a theory T with a sentence A:

1. Find c(A), the smallest sphere intersecting |A|
2. Identify fs(A) = |A| ∩ c(A), the "closest" A-worlds
3. The revised theory T+A is t(fs(A)), which contains exactly those sentences true in all these closest A-worlds

Grove shows this process precisely captures the AGM postulates for belief revision.

### Alternative Relational Formulation

Grove also provides an equivalent formulation using a relation < on ML satisfying:

1. **(S<1)** < is connected
2. **(S<2)** < is transitive
3. **(S<3)** For any consistent |A|, there exist "best" (<-minimal) A-worlds
4. **(S<4)** x is <-minimal if and only if x ∈ X

This relational view helps connect the spheres model to AGM's approach.

## 3. Ordering on Sentences Model - Detailed Explanation

The second model represents belief change through an ordering relation on sentences themselves.

### Mathematical Definition

An ordering relation ≤ on F (all sentences) must satisfy:

1. **(≤1) Connectedness**: For any sentences A and B, either A ≤ B or B ≤ A
2. **(≤2) Transitivity**: If A ≤ B and B ≤ C, then A ≤ C
3. **(≤3) Disjunction property**: If A→B∨C is in L, then either B≤A or C≤A
4. **(≤4) Minimal elements**: A is ≤-minimal if and only if ¬A ∉ T
5. **(≤5) Maximal elements**: A is ≤-maximal if and only if ¬A ∈ L

### Conceptual Interpretation

This ordering captures the relative "importance" or "entrenchment" of sentences:

- Lower-ranked sentences are more easily given up during revision
- Higher-ranked sentences are more firmly held beliefs
- Condition (≤3) ensures logical coherence when eliminating sentences
- Conditions (≤4) and (≤5) anchor the ordering to the current theory T

### Formal Revision Process

The revision T+A is defined as {B ∈ F: (A∧B) ≤ (A∧¬B)}, meaning:

- A sentence B is included in the revised theory when, in the context of accepting A, the conjunction A∧B is more entrenched than A∧¬B
- This elegantly captures the idea that we retain beliefs that cohere best with the new information

Grove proves this approach is equivalent to the systems of spheres model, showing that any ordering relation ≤ corresponds to some system of spheres S.

## 4. Theorems - Comprehensive Explanation

### Theorem 1

**Statement**: If S is any system of spheres centered on |T| for theory T, and T+A is defined as t(fs(A)), then this revision operation satisfies AGM postulates (+2) to (+8).

**Significance**: This establishes that Grove's spheres model is sound - it never produces a revision function that violates AGM's rationality requirements.

**Proof Outline**: Grove demonstrates that each postulate follows from the properties of the spheres model:

- (+2) A ∈ T+A follows because T+A = t(|A|∩c(A))
- (+3) When ¬A ∉ T, the innermost sphere |T| intersects |A|, so c(A) = |T|
- (+4) Consistency follows from the non-emptiness of fs(A) when ¬A ∉ L
- (+5) follows from the logical equivalence of A and B
- (+7) and (+8) follow from the nested structure of spheres and properties of intersection

### Theorem 2

**Statement**: For any revision function satisfying AGM postulates (+2) to (+8), there exists a system of spheres S centered on |T| such that T+A = t(fs(A)) for all A.

**Significance**: This establishes completeness - Grove's model can represent any AGM-compliant revision function.

**Proof Approach**: Grove constructs a system of spheres from an existing revision function by defining:

- S' as the class of sets U satisfying specific conditions related to T+A
- S = S' ∪ {ML} (or S' ∪ {ML,∅} if T is inconsistent)
- He then proves this system generates the original revision function

### Theorem 3

**Statement**: For any revision function satisfying AGM postulates (+2) to (+8), there exists an ordering relation ≤ on F such that T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)}.

**Significance**: This shows that the sentence ordering model is also complete.

**Approach**: Grove derives this from Theorem 2, constructing an ordering from a system of spheres.

### Theorem 4

**Statement**: If ≤ is any relation on F satisfying conditions (≤1) to (≤5), then the revision function defined as T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)} satisfies AGM postulates (+2) to (+8).

**Significance**: This establishes the soundness of the sentence ordering model.

**Proof Approach**: Grove constructs an equivalent system of spheres from the ordering relation ≤:

- He defines "cuts" (sets of sentences where if A ≤ B and A is in the cut, then B is too)
- Associates each cut with a "co-sphere" in ML
- Shows this system of spheres generates the same revision function as the original ordering

## 5. Definition of Symbols - With Examples

- **L**: Set of logical theses (tautologies) of the underlying logic

  - Example: L contains sentences like A→A, A∨¬A

- **F**: Set of all sentences in the language

  - Example: If working with propositional logic, F contains A, B, A∧B, A∨B, etc.

- **_T_**: A theory, i.e., a set L ⊆ T ⊆ F that is closed under logical consequence

  - Example: If T contains A→B and A, then T must contain B

- **T**: The set of all theories

  - Example: T includes L, F, and all consistent deductively closed sets between them

- **Cn(X)**: The logical consequence operator, giving the set of all sentences logically entailed by X

  - Example: If X = {A, A→B}, then Cn(X) includes B, A∧B, A∨B, etc.

- **Con(T)**: T is consistent (not equal to F)

  - Example: Con(T) holds when T doesn't contain both A and ¬A

- **T+A**: Theory resulting from revising T with A

  - Example: If T = Cn({B,C}) and A = ¬B, then T+A might equal Cn({¬B,C})

- **T|A** or **T/A**: Smallest theory containing both T and A, equivalent to Cn(T∪{A})

  - Example: If T = Cn({B}) and A = C, then T/A = Cn({B,C})

- **ML**: Set of all maximal consistent extensions of L

  - Example: In propositional logic with two atoms p,q, ML contains four elements (worlds): {p,q}, {p,¬q}, {¬p,q}, {¬p,¬q}

- **|T|**: The set {m ∈ ML: T ⊆ m}, i.e., all worlds consistent with T

  - Example: If T = Cn({p}), then |T| = {{p,q}, {p,¬q}}

- **|A|**: The set {m ∈ ML: A ∈ m}, i.e., all worlds where A is true

  - Example: |p∨q| = {{p,q}, {p,¬q}, {¬p,q}}

- **t(S)**: Theory determined by a set S of possible worlds: ∩{x ∈ S}

  - Example: t({{p,q}, {p,¬q}}) = Cn({p})

- **c(A)**: Smallest sphere in S intersecting |A|

  - Example: If spheres are |T|⊂U⊂ML and |A|∩|T|=∅ but |A|∩U≠∅, then c(A)=U

- **fs(A)**: Function that selects "closest" A-worlds: |A| ∩ c(A)
  - Example: Continuing above, fs(A) = |A| ∩ U

## 6. Relationship to AGM Postulates - Detailed Analysis

Grove's paper establishes deep connections between his models and the AGM framework:

### Direct Correspondence to Postulates

Grove explicitly proves that both his models satisfy all AGM postulates (+2) to (+8):

- **(+2) Success**: A ∈ T+A
- **(+3) Expansion**: If ¬A ∉ T, then T+A = T/A
- **(+4) Consistency**: T+A is consistent if ¬A ∉ L
- **(+5) Extensionality**: If A↔B ∈ L, then T+A = T+B
- **(+7) & (+8)**: Capture rational behavior for conjunctive revisions

### Correspondence to AGM's Contraction Types

Grove shows that special cases in his framework correspond to different AGM contraction approaches:

1. **Maxichoice contraction**: In AGM, selecting a single maximal subset of T not implying A

   - In Grove's model: System where |A|∩c(A) is always a singleton (Stalnaker's assumption)
   - This creates "complete" theories after revision that introduce unnecessary beliefs

2. **Full meet contraction**: In AGM, intersection of all maximal subsets not implying A

   - In Grove's model: Having just two spheres: |T| and ML
   - This is very conservative, potentially removing too much information

3. **Partial meet contraction**: In AGM, intersection of some selected maximal subsets
   - In Grove's model: Intermediate systems of spheres with finer gradations
   - This provides flexible degrees of belief change

### Equivalence Proof in Section 4

Grove's concluding section proves the equivalence between his approach and AGM's partial meet contraction:

- There is a bijection between maximal subsets in M(T,A) and elements of |¬A|
- The AGM selection function γ that picks "preferred" maximal subsets corresponds to Grove's spheres selecting "closest" ¬A-worlds
- AGM's "transitively relational" partial meet functions correspond to Grove's total preorders on possible worlds

This equivalence demonstrates that Grove's approach doesn't introduce a fundamentally new revision mechanism, but rather provides an equivalent, semantically rich interpretation of AGM's syntactic framework.

## 7. Philosophical Significance

Grove's models offer several conceptual advantages:

1. **Intuitive visualization**: The nested spheres provide a geometric interpretation of belief change
2. **Comparative plausibility**: The models formalize the notion that some worlds are more plausible than others
3. **Minimal change principle**: Revision seeks the "closest" worlds satisfying the new information
4. **Connection to counterfactuals**: Reveals deep connections between belief revision and reasoning about hypotheticals
5. **Unified framework**: Shows that entrenchment relations on sentences and similarity orderings on worlds are two sides of the same coin

This work demonstrates that the formal AGM postulates correspond to natural semantic structures, providing strong evidence for their rationality as constraints on belief revision.
