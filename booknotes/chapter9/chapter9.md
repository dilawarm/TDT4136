# 9 - Inference In First-Order Logic
_In which we define effective procedures for answering questions posed in first-order logic._
We have presented an analysis of logical inference in first-order logic and a number of algorithms for doing it.
* A first approach uses inference rules (__universal instantation__ and __existential instantation__) to __propositionalize__ the inference problem. Typically, the approach is slow, unless the domain is small.
* The use of __unification__ to identify appropiate subsitutions for variables eliminates the instantation step in first-order proofs, making the process more efficient in many cases.
* A lifted version of __Modus Ponens__ uses unification to provide a natural and powerful inference rule, __generalized Modus Ponens.__ The __forward-chaining__ and __backward-chaining__ algorithms apply this rule to sets of definite clauses.
* Generalized Modus Ponens is complete for definite clauses, although the entailment problem is __semidecidable.__ For __Datalog__ knowledge bases consisting of function-free definite clauses, entailment is decidable.
* Forward chaining is used in __deductive databases,__ where it can be combined with relational database operations. It is also used in __production systems,__ which perform efficient updates with very large rule sets. Forward chaining is complete for Datalog and runs in polynomial time.
* Backward chaining is used in __logic programming systems,__ which employ sophisticated compiler technology to provide very fast inference. Backward chaining suffers form redundant inferences and infinte loops; these can be alleviated by __memoization.__
* Prolog, unlike first-order logic, uses a closed world with the unique names assumption and negation as failure. These make Prolog a more practical programming language, but bring it further from pure logic.
* The generalized __resolution__ inference rule provides a complete proof system for first-order logic, using knowledge bases in conjunctive normal form.
* Several strategies exist for reducing the search space of a resolution system without compromising completeness. One of the most important issues is dealing with equality; we showed how __demodulation__ and __paramodulation__ can be used.
* Efficient resolution-based theorem provers have been used to prove interesting mathematical theorems to verify and synthesize software and hardware.