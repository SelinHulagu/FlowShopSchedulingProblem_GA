# FlowShopSchedulingProblem_GA
The flow shop scheduling problem is solved using genetic algorihtms

1)	Solution Representation: Permutation encoding is selected, where whole solution is held within a one dimensional array with the size of number of jobs.

2)	Initial population: Initial population is generated randomly according to the given population size. 

3)	Parent Selection: In order to give randomization to the algorithm routlette wheel selection is used to draw parents from the population. Within roulette wheel selection method, the parent selection step is biased by the parents that has better objective values, here lower makespan. 

4)	Crossover operator: Two-point crossover operator is selected. Within two-point crossover, randomly two points are selected, where the jobs between these two points are always inherited from one parent to the child. Other jobs are placed in the same order as they are in the other parent. A representative example is given below:
P1= [ 1 2 | 3 6 5| 4 ]            P2= [ 3 4 | 5 1 2| 6 ] 
P2= [ 3 4 | 5 1 2| 6 ]            P1= [ 1 2 | 3 6 5| 4 ]            
C1= [ 4 1 | 3 6 5| 2 ]            C2= [ 3 6 | 5 1 2| 4 ]

5)	Mutation: Two job exchange mutation operator is employed to the children with a probability defined, where randomly selected two jobs are exchanged. A representative example is given below:
C1= [ 4 1 3 6 5 2 ]            Mutated C1= [ 4 5 3 6 1 2 ]

6)	Substitution/Replacement: Within the GA generated, whole produced children are placed to the population without checking their objectives. In this context, as many parents as the number of children are substituted from solution. For substitution process, roulette wheel selection is employed again, where selection is biased by the worse solution, here longer makespan. 

7)	Stopping condition: Number of generations is selected as the stopping criteria. 
After trial-error processes, population size, number of generations, mutation probability is set respectively to 5, 1000, and 1 considering the CPU time as well. 
