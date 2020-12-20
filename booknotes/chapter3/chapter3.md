# 3 - Solving Problems By Searching
_In which we see how an agent can find a sequence of actions that achieves its goals when no single action will do._

This chapter has introduced methods that an agent can use to select actions in environments that are deterministic, observable, static, and completely known. In such cases, the agent can construct sequences of actions that achieve its goals; this process is called __search__.
* Before an agent can start searching for solutions, a __goal__ must be identified and a well-defined __problem__ must be formulated.
* A problem consists of five parts: the __initial state__, a set of __actions__, a __transition model__ describing the results of those actions, a __goal test__ function, and a __path cost__ function. The environment of the problem is represented by a __state space__. A __path__ through the state space from the initial space to a goal state is a __solution__.
* Search algorithms treat states and actions as __atomic__: they do not consider any internal structure they might posssess.
* A general TREE-SEARCH algorithm considers all possible paths to find a solution, whereas a GRAPH-SEARCH algorithm avoids consideration of redundant paths.
* Search algorithms are judged on the basis of __completeness, time complexity,__ and __space complexity__. Complexity depends on $b$, the branching factor in the state space, and $d$, the depth of the shallowest solution.
* __Uninformed search__ methods have access only to the problem definition. The basic algorithms are as follows:
    * __Breadth-first search__ expands the shallowest nodes first: it is complete, optimal for unit step costs, but has exponential space complexity.
    * __Uniform-cost search__ expands the node with lowest path cost, $g(n)$, and is optimal for general step costs.
    * __Depth-first search__ expands the deepest unexpanded node first. It is neither complete nor optimal, but has linear space complexity. __Depth-limited search__ adds a depth bound.
    * __Iterative deepening search__ calls depth-first search with increasing depth limits until a goal is found. It is complete, optimal for unit step costs, has time complexity comparable to breadth-first search, and has linear space complexity.
    * __Bidirectional search__ can enormously reduce time complexity, but it is not always applicable and may require too much space.
* __Informed search__ methods may have access to a __heuristic__ function $h(n)$ that estimates the cost of a solution from $n$.
    * The generic __best-first search__ algorithm selects a node for expansion according to an __evaluation function__
    * __Greedy best-first search__ expands nodes with minimal $h(n)$. It is not optimal but is often efficient.
    * __A* search__ expands nodes with minimal $f(n)=g(n)+h(n)$. A* is complete and optimal, provided that $h(n)$ is admissible (for TREE-SEARCH) or consistent (for GRAPH-SEARCH). The space complexity of A* is still prohibitive.
    * __RBFS__ (recursive best-first search) and __SMA*__ (simplified memory-bounded A*) are robust, optimal search algorithms that use limited amounts of memory; given enough time, they can solve problems that A* cannot solve because it runs out of memory.
* The performance of heuristic search algorithms depends on the quality of the heuristic function. One can sometimes construct good heuristics by relaxing the problem definition, by storing precomputed solution costs for subproblems in a pattern database, or by learning from experience with the problem class.