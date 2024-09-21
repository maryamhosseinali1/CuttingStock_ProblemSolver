

This project addresses the **Cutting Stock Problem (CSP)** by applying three powerful optimization techniques: **Genetic Algorithm (GA)**, **Simulated Annealing (SA)**, and **Hill Climbing (HC)**. The CSP is a combinatorial problem commonly encountered in manufacturing, where raw materials such as rolls or sheets need to be cut into smaller pieces according to specific orders. The challenge lies in minimizing waste and using the fewest possible number of raw material rolls.

By leveraging bio-inspired algorithms, this project explores different ways to efficiently solve the problem, each with its strengths in terms of exploration, exploitation, and convergence speed.



The **Cutting Stock Problem** is a key challenge in industries like paper, metal, and textile manufacturing, where raw material needs to be cut into specific sizes to fulfill customer orders. Minimizing material waste and the number of rolls used is essential for cost-effective production. 

This project implements three different optimization algorithms to solve CSP:
- **Simulated Annealing (SA)**: A probabilistic technique inspired by the annealing process in metallurgy, capable of escaping local optima by accepting worse solutions with a certain probability.
- **Genetic Algorithm (GA)**: A population-based method that mimics the process of natural evolution, applying crossover and mutation to generate better solutions over time.
- **Hill Climbing (HC)**: A straightforward iterative algorithm that continuously improves the solution by making small adjustments, quickly converging to a local optimum.

Each of these algorithms brings unique strengths to the table:
- **SA** allows extensive exploration of the solution space early on and gradually focuses on optimization.
- **GA** explores a diverse range of solutions through crossover, improving the population over generations.
- **HC** converges rapidly but may get stuck in local optima, making it suitable for simpler CSP cases.


### Simulated Annealing Algorithm

The **Simulated Annealing (SA)** algorithm works as follows:
- **Initialization**: Begins with a randomly generated solution and tracks the waste over multiple iterations.
- **Main Loop**: Generates new solutions by reassigning orders between rolls. Over time, it reduces the chance of accepting worse solutions by decreasing the temperature (`temp`).
- **Metropolis Criterion**: A probabilistic rule that decides whether to accept new solutions. Good solutions are always accepted, while worse solutions are accepted with a certain probability, controlled by the temperature.
- **Temperature Control**: As the temperature decreases, the algorithm becomes more focused on exploitation, moving towards a more refined solution.

### Genetic Algorithm (GA)

The **Genetic Algorithm** mimics natural selection and evolution:
- **Population**: A set of randomly generated solutions (individuals) representing different allocations of orders to rolls.
- **Crossover**: Combines two parent solutions to create new offspring, mixing their characteristics to produce potentially better solutions.
- **Mutation**: Introduces small random changes to some offspring, encouraging diversity and preventing premature convergence to local optima.
- **Selection**: Chooses the best solutions from the population to continue evolving, ensuring that the best characteristics are preserved over generations.

### Hill Climbing Algorithm

The **Hill Climbing (HC)** algorithm is a simpler, iterative technique:
- **Single Solution**: Starts with a single random solution and makes incremental adjustments to improve it.
- **Greedy Improvement**: It accepts changes only if they result in a better solution (i.e., less waste or fewer rolls).
- **Local Optima**: While it converges quickly, HC can get stuck in local optima, making it less effective for larger or more complex CSP instances.

## Results

The project demonstrates how each of these algorithms solves the Cutting Stock Problem:
- **Simulated Annealing** offers a balance between exploration and exploitation, making it suitable for complex CSP cases where global optimization is needed.
- **Genetic Algorithm** leverages diversity and evolutionary principles to avoid local optima and explore a wider range of solutions.
- **Hill Climbing** provides a fast and simple approach for smaller CSP instances but is more prone to local optima due to its greedy nature.

