# Evo_simulation

## Description

# Concept
In this project, I want to create my own evolutionary simulation (ES). On a 2D plane, both food patches and agents are generated. The user can print/save a 2D plane, single agent statistics and/or population statistics.
I will use R as programing language.

# Minimal Model
A discription of the most basic model to achieve the described project functions.

*Simulation*
During a discrete time step (TS) transition on a place in the plane, the agent can experience changes in internal states, that are discretely updated and saved in a vector (or list) per agent: a) motor, b) sense, c) action, or d) fitness.

a) Motoric is to take a random step or stay (9 options, like the king in chess)

b) Sensation is wether occupying a non-food or food patch. 
    -> Non-food patch: a random step at the next (+1) TP
    -> Food patch: motoric option "stay" at +1 TP
    
c) Action is whether the agent eats a patch or not
    -> If yes, one patch stack depletes from plane
    -> If not, nothing happens
    
d) Fitness is on a scale causing agent transitions in the extremes of reproducing or vanishing
    -> When exceeding one threshold, the agent reproduces, 
    -> when exceeding the other, it vanishes at that TP
