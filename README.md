Basic Flocking Simulation
Objective: Simulate the flocking behavior of a group of agents (e.g., birds or fish) based on three simple rules: separation, alignment, and cohesion. These rules govern the interactions among agents, leading to emergent flocking behavior. This assignment introduces you to concepts in autonomous agent modeling, simulation, and behavior-based control.
Background
Flocking behavior is a classic example of how complex group dynamics can arise from simple local rules. Craig Reynolds' Boids model (1986) described this behavior, which is often observed in birds, fish, and other animals that travel in groups.
The three primary rules are:
Separation: Avoid crowding neighbors (maintain a comfortable distance).
Alignment: Steer towards the average heading of local flockmates.
Cohesion: Steer towards the average position of local flockmates (stay with the group).
Each agent (boid) is treated as an independent "particle" that reacts based on the positions and velocities of nearby agents.
Task Requirements
Define the Environment:
Set up a 2D space (e.g., 100x100 units) where agents (boids) can move.
Implement boundary conditions (e.g., wrap-around or reflective boundaries) to keep boids within the defined space.
Implement Boid Rules:
For each boid, calculate separation, alignment, and cohesion forces based on its neighbors.
Adjust each boid's velocity according to these rules, ensuring they obey maximum speed limits.
Simulate Flocking Behavior:
Initialize a set of boids with random positions and velocities.
Update each boid’s position and velocity at each time step based on the computed forces.
Plot the position of each boid in each time step to visualize flocking behavior.
Analyze Emergent Behavior:
Observe and record how different parameters affect the flocking dynamics (e.g., separation distance, alignment strength, cohesion strength).
Experiment with different initial conditions and parameters to see how flocking behavior changes.
Step 1: Define Boid Properties and Parameters
Define a structure or array for each boid to store:
Position: [x, y] coordinates.
Velocity: [vx, vy] vector.
Rules Parameters:
separation_distance: Minimum distance to maintain from neighbors.
alignment_strength: How strongly a boid aligns with its neighbors.
cohesion_strength: How strongly a boid is attracted to the group center.
max_speed: Maximum speed to prevent boids from moving too fast.
Step 2: Initialize Boid Positions and Velocities
Randomly initialize each boid's position within the bounds of the environment and assign a small random initial velocity.

Step 3: Define the Flocking Rules
Implement functions for each of the three flocking rules. For each boid, calculate the desired direction based on nearby boids.
Separation Rule
This rule calculates a force to move away from close neighbors, avoiding crowding.
Alignment Rule
This rule steers each boid towards the average heading of nearby boids.
Cohesion Rule
This rule steers each boid towards the average position of nearby boids.
Step 4: Update Boid Velocities and Positions
For each boid, compute the resultant force from separation, alignment, and cohesion rules, then update the velocity and position.

Step 5: Run and Observe the Simulation
Run the simulation and observe how the boids group together, align, and avoid each other. Adjust parameters like separation_distance, alignment_strength, and cohesion_strength to see how they affect the flocking behavior.
Analysis and Experimentation
Experiment with Parameters:
Increase Separation: Larger separation_distance results in boids spreading out more.
Increase Alignment: Higher alignment_strength leads to more synchronized movement.
Increase Cohesion: Higher cohesion_strength makes boids cluster together.
Observe Emergent Flocking Behavior:
Watch for emergent patterns such as clustering, synchronous movement, and formations that resemble real-life flocks.
Extend the Model:
Predator Avoidance: Add a predator boid that other boids try to avoid.
Steps to Add Predator Avoidance
Define Predator Properties:
The predator will have a position and velocity.
We can set its movement behavior to chase the average position of the boids or move randomly within the environment.
Add Avoidance Force for Boids:
Each boid will calculate an avoidance force that pushes it away from the predator if the predator is within a certain distance.
This avoidance force will have a similar effect to the separation force but will act more strongly to simulate an emergency response.
Update Boid Position and Velocity with Predator Avoidance:
The avoidance force is added to the other forces (separation, alignment, cohesion) when calculating each boid's velocity.
Reference: https://en.wikipedia.org/wiki/Boids


