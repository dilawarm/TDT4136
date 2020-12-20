# 5 - Adversarial Search
_In which we examine the problems that arise when we try to plan ahead in a word where other agents are planning against us._

We have lookes at a variety of games to understand what optimal play means and to understand how to play well in practise. The most importand ideas are as follows:
* A game can be defined by the __initial state__ (how the board is set up), the legal __actions__ in each state, the __result__ of each action, a __terminal test__ (which says when the game is over), and a __utility function__ that applies to terminal states.
* In two-player-zero-sum games with __perfect information__, the __minimax__ algorithm can select optimal moves by a depth-first enumeration of the game tree.
* The __alpha-beta__ search algorithm computes the same optimal move as minimax, but achieves much greater efficiency by eliminating subtrees that are probably irrelevant.
* Usually, it is not feasible to consider the whole game tree (even with alpha-beta), so we need to cut the search off at some point and apply a heuristic __evaluation function__ that estimates the utility of a state.
* Many game programs precompute tables of best moves in the opening and endgame so that they can look up a move rather than search.
* Games of chance can be handles by an extension to the minimax algorithm that evaluates a __chance node__ by taking the average utiligy of all its children, weighted by the probability of each child.
* Optimal play in games of __imperfect information__, such as Kriegspiel and brigdge, requires reasoning about the current and future __belief states__ of each player. A simple approximation can be obtained by averaging the value of an action over each possible configuration of missing information.
* Programs have bested even champion human players at games such as chess, checkers, and Othello. Humans retain the edge in several games of imperfect information, such as poker, bridge, and Kriegspiel, and in games with very large branching factors and litte good heuristic knowledge, such as Go. (?)
