# Lewis's System of Spheres and Its Relation to Grove's Models

## Lewis's System of Spheres for Counterfactual Logic

David Lewis developed his "system of spheres" semantics in his influential 1973 book "Counterfactuals" to provide truth conditions for counterfactual conditionals of the form "if A were the case, then B would be the case" (written as A □→ B).

### Key Features of Lewis's Model

1. **Structure**: A system of nested spheres centered on a particular possible world w
2. **Interpretation**: Each sphere represents a set of possible worlds with comparable similarity to the central world w
3. **Properties**:

   - Spheres are totally ordered by inclusion (nested)
   - The innermost sphere contains only the world w itself
   - The outermost sphere contains all logically possible worlds
   - The "limit assumption" ensures that for any proposition, if any sphere contains worlds where it's true, there is a smallest such sphere

4. **Truth Conditions**: A counterfactual "if A were the case, then B would be the case" is true at w if either:
   - No A-world is accessible (vacuous truth), or
   - Some sphere contains at least one A-world, and in the smallest such sphere, all A-worlds are also B-worlds

### Visual Representation

Lewis's model can be visualized as concentric circles around a world w, with progressively more dissimilar worlds in the outer circles.

## How Grove Adapted Lewis's Model for Belief Revision

As Grove explains in his 1988 paper, he adapted Lewis's framework in several significant ways to model belief revision:

> "The first, the 'spheres' modelling for theory change, is in form very similar to the 'sphere' semantics for counterfactual logic proposed by Lewis [2]. However, this modelling is also very directly related to the modelling in [1], despite the quite different appearance of the two."

### Key Adaptations by Grove

1. **Center of the System**: While Lewis centers spheres on individual worlds, Grove centers them on theories (sets of beliefs):

   - The innermost sphere contains all worlds compatible with the current theory T
   - Written formally as |T| = {m ∈ ML: T ⊆ m}

2. **Interpretation**: In Grove's model, spheres represent degrees of plausibility rather than similarity:

   - Inner worlds are more plausible candidates for the actual world
   - Outer worlds are progressively less plausible

3. **Revision Operation**: Grove defines revision of T by A as:

   - Find c(A), the smallest sphere intersecting |A|
   - Select fs(A) = |A| ∩ c(A), the "closest" A-worlds
   - Define T+A as t(fs(A)), the theory containing all sentences true in these worlds

4. **Formal Properties**: Grove's spheres satisfy conditions (S1)-(S4), which are analogous to but not identical with Lewis's conditions:

   - (S1) S is totally ordered by ⊆
   - (S2) X is the ⊆-minimum of S
   - (S3) ML is in S
   - (S4) If any sphere intersects |A|, there is a smallest such sphere

## Conceptual and Mathematical Connections

The deep connection between Lewis's and Grove's systems reflects the philosophical relationship between counterfactual reasoning and belief revision:

1. **Minimal Change Principle**: Both approaches embody the principle that when considering hypothetical situations or revising beliefs, we should make minimal changes to our current understanding

2. **Selection Functions**: Both use similar mechanisms to select the most relevant possible worlds:

- Lewis selects the most similar worlds where the antecedent is true
- Grove selects the most plausible worlds where the new information is true

3. **The Ramsey Test Connection**: This connection aligns with the Ramsey Test, which suggests that we evaluate "if A, then B" by hypothetically adding A to our beliefs and seeing if B follows

- Lewis provides semantics for this in terms of counterfactuals
- Grove provides a mechanism for actually performing the revision

4. **The Limit Assumption**: Grove explicitly acknowledges the problematic nature of the limit assumption (S4), just as Lewis did:
   > "Lewis discusses the condition S4, which he calls the 'limit assumption', at some length, and concludes that, while it simplifies part of his theory, it cannot be justified under his intended interpretation of spheres. Similarly, it seems difficult to provide any reasonable 'explanation' for this condition in the current context."

## Formal Equivalence to AGM Framework

Grove proves that his spheres model is formally equivalent to the AGM partial meet contraction approach, showing that both capture exactly the class of revision operations satisfying the rationality postulates (+2) through (+8):

> "The spheres modelling for theory change, is in form very similar to the 'sphere' semantics for counterfactual logic proposed by Lewis [2]. However, this modelling is also very directly related to the modelling in [1], despite the quite different appearance of the two."

In section 4 of his paper, Grove establishes a bijection between maximal subsets in AGM's M(T,A) and elements of |¬A|, showing that Lewis's geometric approach and AGM's more syntactic approach are ultimately capturing the same formal structure.

## Significance

The connection Grove establishes between Lewis's counterfactual semantics and belief revision theory reveals a deep unity between these two areas of logic:

1. It shows that the formal structure for reasoning about hypotheticals provides a natural semantics for belief change
2. It provides an intuitive geometric interpretation of the AGM postulates
3. It demonstrates that different reasoning tasks (counterfactual evaluation and belief revision) have similar underlying logical structures
4. It connects belief revision to a broader tradition in modal and conditional logic

This elegant connection has had lasting influence on subsequent work in belief revision, conditional logic, and formal epistemology.
