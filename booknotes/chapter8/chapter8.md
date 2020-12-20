# 8 - First-Order Logic
___
_In which we notice that the world is blessed with many objects, some of which are related to other objects, and in which we endeavor to reason about them._

This chapter has introduced __first-order logic,__ a representation language that is far more powerful than propositional logic. The important points are as follows:

* Knowledge representation languages should be declerative, compositional, expressive, context independent, and unambigiuous.
* Logics differ in their __ontological commitments__ and __epistemological commitments.__ While propositional logic commits only to the existence of facts, first-order logic commits to the existence of objects and relations and thereby gains expressive power.
* The syntax of first-order logic builds on that of propositional logic. It adds terms to represent objects, and has universal and existential quantifiers to construct assertions about all or some of the possible values of the quantified variables.
* A __possible world,__ or __model,__ for first-order logic includes a set of objects and an __interpretation__ that maps constant symbols to objects, predicate symbols to relations amoing objects, and function symbols to functions on objects.
* An atomic sentence is true just when the relation named by the predicate holds between the objects named by the terms. __Extended interpretations,__ which map quantifier variables to objects in the model, define the truth of quantified sentences.
* Developing a knowledge base in first-order logic requires a careful process of analyzing the domain, choosing a vocabulary, and encoding the axioms required to support the desired inferences.