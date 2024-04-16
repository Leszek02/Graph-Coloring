# Graph Coloring - Genetic Algorithm

A heuristic approach to graph coloring problem. This project was developed for academic purpose. The program first generates a population by:
- randomly pick `random_vertices` vertices and give them all different colors
- iterate through not colored vertices and try to color them with already used color
- repeat until required population is generated

After population is created algorithm goes over these steps 'iterations' times:
- RouletteWheel_Selection - each Specimen is given a score (more conflicting edges - worse score). Specimens with better score have better chances of being chosen. After scoring every Specimen, function randomly picks Specimens until population is full.
- crossover - randomly pick pivot number for two Specimens. Leave values left to the pivot indices unchanged, switch values between two Specimens right to the pivot indices.
- mutation - each Specimen has 'mutationChance' to mutate. Depending on mutation, every vertices can have their color changed or only conflicting vertices can have their color changed.
- poplationElimination - leave half of the best Specimens. Randomly pick from the rest of the population until the population limit is reached.

Every 10 iterations program prints currently found solution.
