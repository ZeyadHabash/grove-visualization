# Two Modellings for Theory Change

## Adam Grove (1988)

---

## 1. Introduction

### Motivation and Context

- **Problem**: How can we formally model rational belief revision?
- **Previous work**: Alchourrón, Gärdenfors, and Makinson (AGM) established postulates and partial meet contraction
- **Segerberg's critique**: AGM's representation "not entirely satisfactory" - lacks "plausible and natural" models
- **Grove's aim**: Provide semantic models that characterize AGM postulates

### Key Contributions

- Connects belief revision to Lewis's work on counterfactual logic
- Provides two equivalent semantic models:
  1. Systems of spheres (geometric/visual)
  2. Ordering on sentences (direct belief entrenchment)
- Proves these models precisely capture AGM-compliant revision functions
- Shows different AGM contraction variants correspond to special cases in his framework

---

## 2. Background & Preliminaries

### Mathematical Framework

- **L**: Set of logical theses (tautologies) of the logic
- **F**: Set of all sentences in the language
- **T**: A theory; a set L ⊆ T ⊆ F closed under logical consequence
- **Con(T)**: T is consistent (not equal to F)
- **Cn(X)**: The logical consequence operator, giving all sentences logically entailed by X
- **M<sub>L</sub>**: Set of all maximal consistent extensions of L (possible worlds)
- **|T|**: Set of worlds compatible with theory T = {m ∈ M<sub>L</sub>: T ⊆ m}
- **t(S)**: Theory determined by a set S of worlds = ∩{x ∈ S}
- **c(A)**: Smallest sphere in S intersecting |A|
- **fs(A)**: Function that selects "closest" A-worlds = |A| ∩ c(A)

### AGM Postulates for Revision

1. **(+1) Closure**: T+A is a logically closed theory (implicit in Grove's framework)
2. **(+2) Success**: A ∈ T+A
3. **(+3) Expansion**: If ¬A ∉ T, then T+A = T/A
4. **(+4) Consistency**: T+A is consistent if ¬A ∉ L
5. **(+5) Extensionality**: If A↔B ∈ L, then T+A = T+B
6. **(+6) Recovery**: T ⊆ (T-A)+A (not directly addressed by Grove)
7. **(+7) Conjunctive Inclusion**: T+(A∧B) ⊆ (T+A)+B
8. **(+8) Conjunctive Vacuity**: If ¬B ∉ T+A, then (T+A)+B ⊆ T+(A∧B)

---

## 3. Systems of Spheres Model

### Key Insight

"Think of concentric circles of possible worlds, where inner worlds are more plausible than outer worlds."

### Formal Definition

A system of spheres S centered on |T| must satisfy:

1. **(S1) Total ordering**: Spheres are nested (U ⊆ V or V ⊆ U)
2. **(S2) Minimum element**: |T| is the smallest sphere (innermost)
3. **(S3) Maximum element**: ML is in S (outermost sphere)
4. **(S4) Limit assumption**: If any sphere intersects |A|, there exists a smallest such sphere

### Relational Formulation of Spheres

1. **(S<1) Connectedness**: < is connected (∀x, y ∈ M<sub>L</sub>: x < y or y < x)
2. **(S<2) Transitivity**: < is transitive
3. **(S<3) Best Elements**: If |A| ≠ ∅, then {x ∈ |A|: x < y ∀y ∈ |A|} ≠ ∅ - this corresponds to S4, and says that if there are any A worlds, then there are some 'best' (<-minimal) such worlds
4. **(S<4) Minimal Worlds**: x in M<sub>L</sub> is < minimal (x < y ∀y) if and only if x ∈ |T|

### S4: The Limit Assumption

- **Problem**: Philosophically questionable (there might not be "closest" worlds)
- **Lewis's stance**: Could be removed from counterfactual logic
- **Grove's stance**: "Plays a crucial role" and "not easily removed" in belief revision
- **Critical difference**: Belief revision requires specific output theories, not just truth values

### Revision Process

1. Find c(A): smallest sphere intersecting |A|
2. Compute fs(A) = |A| ∩ c(A): the "closest" A-worlds
3. Derive T+A = t(fs(A)): theory true in all closest A-worlds

### Example

- **Current theory T**: "The pet is a mammal and has fur"
- **New information A**: "The pet lives in water"
- **Process**:
  - Find closest worlds where "pet lives in water" is true
  - New theory includes "pet is a mammal" (retained) but might exclude "has fur"

---

## 4. Theorem 1: Soundness of Spheres Model

### Statement

If S is any system of spheres centered on |T|, and T+A is defined as t(fs(A)), this revision operation satisfies AGM postulates (+2) to (+8).

### Key Steps in Proof:

1. **Success (+2):**

   - Shows T+A = t(|A|∩c(A)) = t(c(A))/A
   - Since A is true in all worlds in |A|, A ∈ t(fs(A))

2. **Expansion (+3):**

   - When ¬A ∉ T, |T| intersects |A|
   - Since |T| is the smallest sphere, c(A) = |T|
   - Therefore T+A = t(|A|∩|T|) = t(|T|)/A = T/A

3. **Consistency (+4):**

   - If ¬A ∉ L, then |A| ≠ ∅ (there's at least one maximal extension containing A)
   - Since ML intersects |A|, there exists c(A)
   - Therefore |A|∩c(A) ≠ ∅, making T+A consistent

4. **Extensionality (+5):**

   - If A↔B ∈ L, then |A| = |B| (same worlds make both true)
   - Therefore T+A = T+B

5. **Conjunctive Inclusion (+7):**

   - Since A∧B→A, any sphere intersecting |A∧B| intersects |A|
   - Shows |A|∩|B|∩c(A) ⊆ |A∧B|∩c(A∧B)
   - Therefore T+A∧B ⊆ (T+A)/B

6. **Conjunctive Vacuity (+8):**
   - If ¬B ∉ T+A, then |B|∩|A|∩c(A) ≠ ∅
   - This means |A∧B|∩c(A) ≠ ∅, so c(A∧B) ⊆ c(A)
   - Therefore (T+A)/B ⊆ T+A∧B

### Significance

- Proves Grove's model is sound - never produces revisions violating AGM
- Provides geometric intuition for rational belief change

---

## 5. Theorem 2: Completeness of Spheres Model

### Statement

For any revision function satisfying AGM postulates (+2) to (+8), there exists a system of spheres S centered on |T| such that T+A = t(fs(A)) for all A.

### Construction Strategy:

1. **Defining candidate spheres:**

   - S' = class of all nonempty sets U satisfying:
     a. ∀u ∈ U, ∃A ∈ F: u ∈ |T+A|
     b. If |A|∩U ≠ ∅ for any A, then |T+A| ⊆ U
   - S = S'∪{ML} [or S'∪{ML,∅} if T inconsistent]

2. **Proof that S is a system of spheres:**

   - Verifies S is centered on |T| and satisfies S1-S4

3. **Key insight:**

   - Constructs special sphere U = ⋃{|T+B|: |A|⊆|B|, B∈F}
   - Proves |A|∩U = |T+A|, establishing stronger result that |T+A| = |A|∩c(A)

4. **Significance:**
   - Shows sphere model completely characterizes AGM revision
   - Construction not unique - multiple sphere systems can generate same revision function

### Significance

- Proves Grove's model is complete - can represent any AGM-compliant revision
- Shows AGM's abstract postulates have concrete geometric interpretation
- Justifies AGM as capturing rational belief change

---

## 6. Ordering on Sentences Model

### Key Insight

"Instead of ordering possible worlds, we can order sentences themselves by their relative importance."

### Formal Definition

An ordering relation ≤ on F must satisfy:

1. **(≤1) Connectedness**: A ≤ B or B ≤ A (all sentences comparable)
2. **(≤2) Transitivity**: If A ≤ B and B ≤ C, then A ≤ C
3. **(≤3) Disjunction property**: If A→B∨C ∈ L, then B≤A or C≤A
4. **(≤4) Minimal elements**: A is ≤-minimal iff ¬A ∉ T
5. **(≤5) Maximal elements**: A is ≤-maximal iff ¬A ∈ L

### The Disjunction Property Explained

- If A logically implies B∨C, then at least one of B or C must be at least as entrenched as A
- Ensures logical coherence by respecting logical relationships between beliefs
- Prevents keeping belief A while rejecting all its logical consequences
- Example: If "This is a mammal" implies "has lungs OR has gills", we can't reject both methods of breathing

### Revision Process

- T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)}
- Means: B is in the revised theory when, in context of accepting A, A∧B is more entrenched than A∧¬B
- Elegant formulation: retain beliefs that cohere best with new information

---

## 7. Theorems 3 & 4: Equivalence of Models

### Theorem 3 (Sentence Ordering Completeness)

For any revision function satisfying AGM postulates (+2) to (+8), there exists an ordering relation ≤ on F such that T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)}.

### Theorem 4 (Sentence Ordering Soundness)

If ≤ is any relation on F satisfying conditions (≤1) to (≤5), then the revision function defined as T+A = {B ∈ F: (A∧B) ≤ (A∧¬B)} satisfies AGM postulates (+2) to (+8).

### Constructive Proof Approach:

1. **From ordering to spheres:**

   - Define "cut": set W where if A ≤ B and A ∈ W, then B ∈ W
   - Define "co-sphere": maximal consistent extensions not intersecting a cut
   - System S = set of all co-spheres

2. **Verifying S1-S4 for constructed system:**

   - S1 (Total ordering): Follows from cuts being nested (by connectedness ≤1)
   - S2 (Minimum element): Co-sphere of sentences with ¬A ∈ T equals |T|
   - S3 (Maximum element): Co-sphere of maximal sentences equals ML
   - S4 (Limit assumption): Uses closure of cuts under unions

3. **Equivalence of revision operations:**
   - For sphere system S from ordering, proves:
     {B: (A∧B) ≤ (A∧¬B)} = t(|A|∩c(A))
   - Uses lemma to connect cuts and co-spheres
   - Bi-directional proof showing elements match in both directions

### Bridging the Two Models

### From spheres to ordering:

- Define A ≤s B if c(A) ⊆ c(B)
- Ordering captures "A is at least as plausible/entrenched as B"

### From ordering to spheres:

- Define cuts (sets closed upward under ≤)
- Form co-spheres from cuts
- System of co-spheres forms sphere system

### Significance:

- Belief entrenchment and world similarity are two perspectives on same phenomenon
- Directly connects syntactic approach (sentences) to semantic approach (possible worlds)

### Significance

- Shows belief entrenchment and world similarity are two perspectives on same phenomenon
- Unifies two intuitions about belief change: minimize distance to current theory and preserve important beliefs

---

## 8. Contraction in Grove's Framework

### Key Insight

"Contraction is expanding the set of possible worlds just enough to include some worlds where the proposition is false."

### Bijection Between AGM and Grove

For any sentence A where A ∈ T and A ∉ L:

- Each maximal subset of T not implying A corresponds exactly to a world where ¬A is true
- Specifically, |T| ∪ {u} for u ∈ |¬A| gives a maximal subset

### Contraction Process in Grove's Model

1. Identify |¬A| - worlds where A is false
2. Determine which are "closest" to |T| based on sphere system
3. T-A corresponds to expanding |T| to include these closest ¬A-worlds

### Special Cases of Contraction

1. **Maxichoice contraction**:

   - AGM: Select single maximal subset not implying A
   - Grove: |A|∩c(A) is a singleton (Stalnaker's assumption)

2. **Full meet contraction**:

   - AGM: Intersect all maximal subsets not implying A
   - Grove: System with just two spheres |T| and ML

3. **Partial meet contraction**:
   - AGM: Intersect some preferred maximal subsets
   - Grove: Intermediate systems with finer sphere gradations

---

## 9. Philosophical & Practical Significance

### Conceptual Advantages

1. **Intuitive visualization**: Nested spheres provide geometric interpretation
2. **Comparative plausibility**: Formalizes that some worlds are more plausible
3. **Minimal change principle**: Revision seeks "closest" worlds satisfying new information
4. **Connection to counterfactuals**: Reveals deeper unity between reasoning frameworks
5. **Unified framework**: Shows entrenchment and similarity are two sides of same coin

### Validating AGM

- Shows AGM postulates correspond to natural semantic structures
- Strengthens case for AGM as capturing rational belief change
- Proves AGM is not merely syntactic manipulation but has semantic interpretations

### Expanded Horizons

- Opens connection to conditional logics
- Provides foundation for more sophisticated belief revision systems
- Enables visual/geometric thinking about abstract belief operations

---

## 10. Conclusion & Future Directions

### Summary

- Grove provided two "plausible and natural" semantic models for belief revision
- Both precisely capture AGM-compliant revision functions
- Showed deep connection to counterfactual reasoning

### Impact

- Strengthened theoretical foundation of belief revision
- Provided intuitive interpretations of abstract postulates
- Connected different approaches to theory change

### Open Questions

- Addressing limitation of Limit Assumption (S4)
- Extending to iterated belief revision
- Applications to artificial intelligence and knowledge representation

### Final Thought

"Grove's paper shows that rational belief change can be understood through the elegant metaphor of nested spheres of possibility, bringing formal rigor to our intuitive understanding of how beliefs should change in light of new information."
