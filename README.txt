------------------------------------
CSC 473 A2
------------------------------------
Dhowa Husrevoglu
V00955566
--------------
The following are complete:

- Particle system
- Script commands
- Forward Euler
- Verlet
- Symplectic Euler
- Ground collision penalty forces
- Gravity
- Locking of a particle's position
- Particle and spring drawing
---------------
Notes:

- The ground point is set as (0, 0, 0) and ground normal as (0, 1, 0)
- The first step of verlet integration is done with euler
- Ground collision penalty force is set to 0 by default
- Gravity is set to 0 by default
- Global drag is set to 2 by default for minimizing the jittering and oscillation of particles (use command to turn it off to see effectiveness of the hack below)
- Added a little hack when I calculate collision response to stop particles from jittering when timestep is closer to 0.01
---------------



