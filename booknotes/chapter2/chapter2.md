# 2 - Intelligent Agents
_In which we discuss the nature of agents, perfect or otherwise, the diversity of environments, and the resulting menagerie of agent types._

This chapter has been something of whirlwind tour of AI, which we have conceived of as the science of agent design. The major points to recall are as follows:
* An __agent__ is something that percieves and acts in an environment. The __agent function__ for an agent specifies the action taken by the agent in response to any percept sequence.
* The __performance measure__ evaluates the behavior of the agent in an environment. A __rational agent__ acts so as to maximimize the expected value of the performance measure, given the percept sequence it has seen so far.
* A __task environment__ specification included the performance measure, the external environment, the actuators, and the sensors. In designing an agent, the first step must always be to specify the task environment as fully as possible.
* Task environments vary along several significant dimensions. They can be fully or partially observable, single-agent or multiagent, deterministic or stochastic, episodic or sequential, static or dynamic, discrete and continuous, and known or unknown.
* The __agent program__ implements the agent function. There exists a variety of basic agent-program designs reflecting the kind of information made explicit and used in the decision process. The designs vary in efficiency, compactness, and flexibility. The appropiate design of the agent program depends on the nature of the environment.
* __Simple reflex agents__ respond directly to percepts, whereas __model-based reflex agents__ maintain internal state to track aspects of the world thare not evident in the current percept. __Goal-based agents__ act to achieve their goals, and __utility-based agents__ try to maximimize their own expected "happiness."
* All agents can improve their performance through __learning.__