# Chapter 3 - Strategic Form Solution Concepts
## 3.1 - Dominant Strategy Equilibrium
__Definition__
An action $a_i\in A_i$ _weakly dominates_ action $b_i\in A_i$ for player $i$ if
$$u_i(a_i, a_{-i})\geq u_i(b_i,a_{-i})\quad\text{ for all }a_{-i}\in A_{-i}$$
and 
$$u_i(a_i, a_{-i})>u_i(b_i,a_{-i})\quad\text{ for some }a_{-i}\in A_{-i}.$$
If _strictly dominates_ $b_i$ if
$$u_i(a_i, a_{-i})>u_i(b_i,a_{-i})\quad\text{ for all }a_{-i}\in A_{-i}.$$

__Definition__
An action $a_i\in A_i$ is _weakly dominant_ if it weakly dominates every action in $A_i.$ It is called _strictly dominant_ if it strictly dominates every action in $A_i.$

__Definition__
_Weakly dominant strategy equilibrium_ of a game $G$ in strategic form is defined as the weakly dominant action profile, and is denoted by $D^w(G).$ Replacing the word "weakly" with "strictly" yields the definition for _strictly_ dominant strategy equilibrium, which is denoted by $D^s(G).$
## 3.2 - Dominance Solvability
__Definition__
Take a game in strategic form and consider any two actions $a_i,b_i\in A_i$ for any player $i\in N.$ We say that $a_i$ is _strictly dominated_ by $b_i$ if
$$u_i(a_i, a_{-i})<u_i(b_i, a_{-i})\quad\text{ for all }a_{-i}\in A_{-i}.$$
We say that $a_i$ is _weakly dominated_ by $b_i$ if
$$u_i(a_i, a_{-i})\leq u_i(b_i, a_{-i})\quad\text{ for all }a_{-i}\in A_{-i}$$
while
$$u_i(a_i, a_{-i})< u_i(b_i, a_{-i})\quad\text{ for some }a_{-i}\in A_{-i}$$

__Proposition 3.1__
_If both players have strictly dominant actions, then IESD actions leads to the unique dominant strategy equilibrium._

__Definition__
A strategic form game is _dominance solvable_ if IESD actions leads to a unique outcome.
## 3.3 - Nash Equilibrium
__Definition__
_Nash equilibrium_ of game $G$ in strategic form is defined as any outcome $(a_1^*,\dots,a_n^*)$ such that
$$u_i(a_i^*, a_{-i}^*)\geq u_i(a_i, a_i^*)\quad\text{ for all }a_i\in A_i$$
holds for each player $i.$ The set of all Nash equilibria of $G$ is denoted by $N(G).$

__Proposition 3.2.__
_For any 2-person game in strategic form $G$, we have $(a_1^*, a_2^*)\in N(G)$ if, and only if_
$$a_1^*\in B_1(a_2^*)\quad\text{ and }\quad a_2^*\in B_2(a_1^*).$$
## 3.4 - Nash Equilibrium and Dominant/Dominated Actions
__Proposition 3.3__
_A Nash equilibrium need not survive the IEWD actions._

__Proposition 3.4__
_Let $G$ be a game in strategic form with finite action spaces. If the iterared elimination of weakly dominated actions results in a unique outcome, then this outcome must be a Nash equilibirium of $G.$_

__Proposition 3.5__
_Let $G$ be a 2-person game in strategic form. If $(a_1^*, a_2^*)\in N(G),$ then a_1^* and a_2^* must survive the iterated elimination of strictly dominated actions._
## 3.5 - Difficulties with Nash Equilibrium
### 3.5.1 - A Nash equilibrium may involve a weakly dominated action by some players
__Definition__
An __undominated Nash equilibrium__ of a game $G$ in strategic form is defined as any Nash equilibrium $(a_1^*,\dots,a_n^*)$ such that none of the $a_i^*$s is a weakly dominated action. The set of all undominated Nash equilibria of $G$ is denoted $N_\text{undom}(G).$

__Definition__
A __Pareto optimal Nash equilibrium__ of game $G$ in strategic form is any Nash equilibrium $a^*=(a_1^*,\dots,a_n^*)$ such that there does not exist another equilibrium $b^*=(b_1^*,\dots,b_n^*)\in N(G)$ with
$$u_i(a^*)<u_i(b^*)\quad\text{ for each }i\in N.$$
We denote the set of all Pareto optimal Nash equilibrium of $G$ by $N_\text{PO}(G).$

__Definition__
A __Strong Nash equilibrium__ of a game $G$ in strategic form is any outcome $a^*=(a_1^*,\dots,a_n^*)$ such that, for all nonempty coalitions $K\subseteq N$ and all $a_K\in A_K,$ there exists a player $i\in K$ such that
$$u_i(a_K^*,a_{-K}*)\geq u_i(a_K, a_{-K}^*).$$
We denote the set of all strong Nash equilibrium of $G$ by $N_S(G).$
