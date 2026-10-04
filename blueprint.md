#World
Arena dimension: 10 x 10
Fixed simulation timestep
Current step number: ?
Fish and Shark states: Fiash will be dead or alive, shark will always be alive
Episode time limit: ?
Capture rule: When there is a shark and fish on the same coordinate in the vector space, the fish will die. I plan to add it such that when the Shark
			  eats a certain amount of fishes, e.g. 4, it will grow in size.
Boundary behaviour: It will go in any of the 3 directions excluding the directioin of the Boundary
Random-number generator: 0 to 3, maps to up-down-left-right, respectively
The episode ends through either time limit or capture, whichever one comes first.
##Conceptual operations:
1. Every run starts with a seeded initial state
2. Produce an obseravtion for the fish ? 
3. Accept a fish action
4. Ask the shark policy for its action
5. Advance the world by one fixed timestep
6. Report whether capture or timeout occurred
7. Return episode metrics

#Agent state
Position
Velocity (Not yet)
Radius: Just one coordinate space
Maximum speed: NIL
Maximum acceleration or turning strength: NIL
Alive/eaten state

#Observation
Start with six normalized values:
1. Shark's horizontal position relative to the Fish
2. Shark's vertical position relative to the Fish
3. Fish horizontal Velocity
4. Fish vertical Velocity
5. Shark horizontal Velocity
6. Shark vertical Velocity
