# EvoGame

## Description

# Concept
In this project, I createed my own evolutionary simulation. On a 2 dimensional plane, both food patches and agents are generated. The user receives single agent statistics and food information per time point and eventually meta data statistics.

# Summary of Mechanisms and user adjusteable features
Core functions
Simulation function parameter: 1) a function that specifies the size of the 2 dimensional plane, where agents reappear on the other side of the matrix if they move across boundaries
2) amount of initial food and specification of random food generation
3) the initial number of agents to put into the model. 
4) how long should the process run at most.

We are going to discuss now the basic idea of the generating process.

# Base Model
<p> A discription of the most basic model to achieve the described project functions. <br>

*Simulation*
During a discrete time step, agents transition on the plane. The agent can experience changes its internal states, that are discretely updated and those changes are saved in a data frame per agent.

The internal states comprise: a) motor, b) sense, c) action, d) energy, and e) fitness.
In this order, each state is updated for each agent.

a) Motoric is to take a random step or stay (9 options, like the king in chess)

b) Sensation is wether occupying a non-food or food patch. 
    -> Non-food patch: a random step at the next (+1) time step
    -> Food patch: motoric option "stay" at +1 time step
    
c) Action is whether the agent eats a patch or not.
    -> If yes, one patch stack depletes from plane
    
d) & e) Energy and Fitness are discrete scales. Depending on the energy level, the agent can transition its fitness states, namely from normal into reproducing or vanishing.

Beginning after the initial time step, there is also new food generated.

For more information, please view the EvoGame vignette.
