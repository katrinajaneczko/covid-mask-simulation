# The Effect of Mask Type on the Spread of COVID-19 on a College Campus: An Agent-Based Model (MATH 2121 Final Project)
### Katrina Janeczko   -  May 3, 2022

This code simulates the effect of mask type on the spread of COVID-19 on a college campus. Beginning with an initial number of `N=395` agents (a scaled-down version of Temple's student population) and an initial positivity rate of `i=0.019`, agents are randomly placed on a 10x10 grid with their assigned attribute of mask type (or infected). They will wander the grid for about the duration of a semester where each time step is an hour, and when another agent is present in a grid square with an infected agent, they have a certain probability of becoming infected that is determined by the base probability modified by the probability dictated by their mask type. Once an agent is infected for 6 days, they are removed (to quarantine) and are reintroduced as immune (regardless of mask type) to the population. With each time step, with a small probability, a new infectious agent may be introduced into the population. The code plots a 10x10 grid on the left representing the campus where each student is a colored dot representing mask type of infection status, and a line graph on the right showing the proportion of infected students over time (with a bar for current population size).

To run, choose from the experimental distribution arrays (q_percentages) which dictate reasonable percentages of all agents wearing each mask type (no mask, cloth mask, surgical mask, or respirator, respectively). Uncomment the experiment of choice and then press the Run button under Editor in MATLAB, or type `janeczko_final_project` in the Command Window. Only one experiment may be uncommented at a time, the others must remain commented out using `%` at the beginning of the line. The options are the following: <br>
`q_percentages = [1, 1, 1, 1]; % no masks at all` <br>
`q_percentages = [0.5, 0.75, 0.9, 1]; % no mask mandate` <br>
`q_percentages = [0.01, 0.7, 0.9, 1]; % regular mask mandate` <br>
`q_percentages = [0.01, 0.05, 0.9, 1]; % surgical mask mandate` <br>
`q_percentages = [0.01, 0.05, 0.1, 1]; % respirator mask mandate` <br>
`q_percentages = [0, 0, 0, 1]; % only respirators` <br>
As an example of how the values in the array correspond to the distribution of mask types, the “no mask mandate” experiment has 50% no mask agents, 75%-50%=25% cloth mask agents, 90%-75%=15% surgical mask agents, and 100%-90%=10% respirator agents. 

One may also choose to modify other values such as `N` (the starting population) or `i` (the initial infection rate) to model this phenomenon on another college campus, since these values are based off Temple University’s statistics in 2020 found [here](https://temple-news.com/trackingcovid19/) in Temple News’s COVID-19 case tracker. 

For more information on the model and for citations, see the [project report](https://docs.google.com/document/d/1KheKYWURzTDuskav3Wl9sTiYpqedVGGxiG-bVWamwQM/edit?usp=sharing).
