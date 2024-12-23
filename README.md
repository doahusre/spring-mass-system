------------------------------------
# Spring Mass System
------------------------------------
## Commands:

default system name is partSys
- system <sys_name> dim <Number of Particles>
- system <sys_name> particle <index> <mass> <x y z vx vy vz>
- system <sys_name> all_velocities  <vx vy vz>

default simulator name is partSim
- simulator <sim_name> link <sys name> <Number of Springs>
- simulator <sim_name> spring <index1> <index2> <ks> <kd> <restlength>
- simulator <sim_name> fix <index>
- simulator <sim_name> integration <euler|symplectic|verlet> <time step>
- simulator <sim_name> ground <ks> <kd>
- simulator <sim_name> gravity <g>
- simulator <sim_name> drag <kdrag>
--------------------------------------
## Implemented:

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


https://github.com/user-attachments/assets/284d72e3-471b-40d1-a4ff-b7feefe71b7c





