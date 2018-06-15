SIRs Model - Imran Marwat

The SIRs model (susceptible, infected, recovered) model is a mathematical model to simulate the spread of infectious disease. See https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIR_model for more details

SIRS_Class.py contains all methods to simulate and sample such a system as a 2D lattice. SIRS_Script.py contains the instructions for different tasks. 

To Run: python3 SIRS_Script.py <dimension> <p1> <p2> <p3> <task>

p1,p2,p3 are probabilities of a cell switching from S->I, I->R, R->S. Where the following numbers represent each state: -1=S, 0=I, 1=R.
Available 'tasks' in the script are:
- <task> = "viz" creates an animation of the system with the user defined probabilities.
(0.8,0.1,0.01 creates recurring waves of infection)

- <task> = "phase" simulates the SIRs model for a range of probs of S->I & I->R. p2 should be set to 0.5. In this task the lattice is sampled routinely and the average infected fraction density and variance in the infected fraction desnity are presented as contour plots. 

- <task> = "immune" simulates the SIRs model with an increasing fraction of fixed immune cells. A graph is produced which indicates the minimum immune fraction to reduce the average infected fraction to 0. p1=p2=p3=0.5.

