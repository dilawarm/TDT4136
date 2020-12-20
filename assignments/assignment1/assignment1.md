# Assignment 1
_Author_: Dilawar Mahmood
_Date_: 22/08-2020
## Artificial Intelligence Fundamentals and Intelligent Agents
### Theoretical Questions
1. __Define artificial intelligence (AI). Find at least 3 definitions of AI that are not covered in the lecture.__

* "Artificial intelligence (AI), the ability of a digital computer or computer-controlled robot to perform tasks commonly associated with intelligent beings." - [Britannica](https://www.britannica.com/technology/artificial-intelligence)
* "A branch of computer science dealing with the simulation of intelligent behavior in computers." - [Merriam Webster](https://www.merriam-webster.com/dictionary/artificial%20intelligence)
* "The theory and development of computer systems able to perform tasks normally requiring human intelligence, such as visual perception, speech recognition, decision-making, and translation between languages." - [Lexology](https://www.lexology.com/library/detail.aspx?g=5424a424-c590-45f0-9e2a-ab05daff032d)

2. __What is the Turing test, and how is it conducted?__

The Turing test is a test which was desinged to provide a satisfactory operational definition of intelligence. The test is conducted by a human interrogator, who asks some written questions to a computer. The computer passes the test if the interrogator cannot tell whether the written responses come from a human or from a computer. It is important to note that the Turing test avoids direct physical interraction between the interrogator and the computer, because it is irrelevant for intelligence.

3. __What is the relationship between thinking rationally and acting rationally? Is rational thinking an absolute condition for acting rationally?__

Thinking rationally is the process of using your toughts to reach logical conclusions. Acting rationally is to take the _best_ action given the information you have. Rational thinking is not an absolute condition for acting rationally, since the knowledge the rational tought is based on can be incorrect. An agent who has already the rational toughts stored as internal information does not need to think rationally before making the rational action.

4. __Describe rationality. How is it defined?__

For each possible percept sequence, a rational agent should select an action that is expected to maximize its performance measure, given the evidence provided by the percept sequence and whatever built-in knowledge the agent has.

5. __What is Aristotle’s argument about the connection between knowledge and action? Does he make any further suggestion that could be used to implement his idea in AI? Who was/were the first AI researcher(s) to implement these ideas? What is the name of the program/system they developed? Google about this system and write a short description about it.__

Aristotle argued (in _De Motu Animalium_) that actions are justified by a logical connection between goals and knowledge of the action's outcome. To reach a desired goal/outcome, the knowledge is necessary to take the correct action. 
Aristotle's algorithm was a furhter suggestion that could be used to implement his idea in AI. The idea is to assume the goal, and then to consider how and by what means it is attained. This is also known as goal-based analysis.
Aristotle's algorithm was implemented by Allen Newell and Herbert Simon in their GPS program.
General Problem Solver (GPS) was the first useful AI program, and was written in 1959. Simon and Newell made GPS' problem-solving algorithm similar to how humans solve problems, by performing means-ends analysis. The basic algorithm can be summarized as follows:
The ultimate goals are first considered; if they are already achieved, then we're done. Otherwise, the goals can be achieved by applying some operators. An operator is made out of:
* The action
* The preconditions
* The change of conditions from taking the action.

The preconditions are also investigated.

6. __Consider a robot whose task it is to cross the road. Its action portfolio looks like this: look-back, lookforward, look-left-look-right, go-forward, go-back, go-left and go-right.__
__(a) While crossing the road, a helicopter falls down on the robot and smashes it. Is the robot rational?__

Given the actions the robot can perform, and the task it is trying to achieve, the robot is rational. Since the helicopter is coming from above, and the action "looking up" is outside the robots action portfolio, the robot is by definition rational, since it is trying to cross the road given the environment it can observe and actions it can take.

6. __(b) While crossing the road on a green light, a passing car crashes into the robot, preventing it from crossing. Is the robot rational?__

Since the robot can "look-left-look-right" to observe any obstacles coming down the road before crossing the road, and "go-back" if the obstacle prevents the robot from reaching its goal, the robot is not rational.

7. __Consider the vacuum cleaner world described in Chapter 2.2.1 of the textbook. Let us modify this
vacuum environment so that the agent is penalized 1 point for each movement.__
__(a) Can a simple reflex agent be rational for this environment? Explain your answer.__

A simple reflex agent cannot be rational for this environment because if all the tiles are clean, then the agent would just move back and forth infinitely. That would lead to getting penalized infinitely.

7. __(b) Can a reflex agent with state be rational in this environment? Explain your answer.__

A reflex agent with state woulc be rational in this environment since the agent would have an internal state of whether the floor is cleaned or not. When the floor is clean, it would stop moving, thus not loosing points.

7. __(c) Assume now that the simple reflex agent (i.e., no internal state) can perceive the clean/dirty status of both locations at the same time. Can this agent be rational? Explain your answer. In case it can be rational, design the agent function.__

This agent can be rational since it can perceive the clean/dirty status of both locations at the same time, and would then not move when it perceives both to be clean. It is important to notice that the agent would perceive the environment infinitely.
The agent function:
```
function SIMPLE-REFLEX-AGENT([locationA, locationB]) returns an action
if (locationA.status = Clean and locationB.status = Clean) then return;
else if (locationA.status = Clean and locationB.status = Dirty) then return {Right, Suck};
else if (locationA.status = Dirty and locationB.status = Clean) then return Suck;
else if (locationA.status = Dirty and locationB.status = Dirty) then return {Suck, Right, Suck};
```

8. __Consider the vacuum cleaner environment shown in Figure 2.3 in the textbook. Describe the environment using properties from Chapter 2.3.2, e.g. episodic/sequential, deterministic/stochastic etc. Explain selected values for properties in regards to the vacuum cleaner environment.__

* The environment is __partially observable__ since the agent cannot perceive the whole environment at each point in time. The vacuum cleaner does not know if for example location B is dirty or clean before it is besides the relevant tile.
* The environment is __single agent__ since the vacuum cleaner is the only agent in the environment.
* The environment is __deterministic__ since the environment is only influenced by the agent. 
* The environment is __episodic__ since the agent is performing one action at a time, and the next action does not depend on the action before.
* The environment is __static__ since the environment does not change while the vacuum cleaner is deliberating. No more dirt is added or removed from the environment.
* The environment is __discrete__ since there is only a finite number of actions the vacuum cleaner can take and there's a finite number of states the environment can have (dirty or clean).
* The environment is __known__ since the outcome for all the actions the vacuum cleaner takes are given. If the agent sucks, the floor will be cleaned.

9. __Discuss the advantages and limitations of these four basic kinds of agents:__
__(a) Simple reflex agents:__

The advantage of this agent is that it is fairly simple to implement, because it acts on direct knowledge, has no memory and no goal of the action it's performing. The limitation that it is too simple and can only be used for simple controllers.

9. __(b) Model-based reflex agents:__

The advantages of this model is that it can update it's internal state or memory, and it also has a knowledge of how entities relevant to itself work. The limitation is that this agent cannot know about any logic that was not implemented.

9. __(c) Goal-based agents__

The advantage of this agent is that it is able to evaluate sequences of actions and take that action that will get the agent closer to its goal. The agent can easily change its behavior according to the specified goal. The limitation is that the agent is not so effective, and the agent's goal may not be rational.

9. __(d) Utility-based agents__

The advantages of this agent is that it is able to look at several variables at once to determine what the best action is. This agent also learns while doing the actions. The limitation of this agent is that is has no memory of how the environment was, so it looks at the current state of the environment and how it can improve the environment.