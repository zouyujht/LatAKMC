# LatAKMC
##A Lattice based Adaptive KMC code with basin code function

### Requirements
LAKMC Graphs, NEB, Lattice, Minimise, Input, Vectors modules <br>
lkmcInput.IN    - input file from LAKMC <br>
md directory    - directory full of information for MD (LBOMD or LAMMPS) <br>

### About to code
This script runs KMC on a hexagonal <b>ZnO(0001)</b> surface (to be generalised later) <br>
Assumes PBC in <i>x</i> and <i>z</i> directions and deposition in <i>y</i> <br>
Grid positions start at (0,0,0) <br> 


### Setup:
KMC.py            - main source code (python)<br>
Parameters.py     - module for reading input parameters
input.IN          - input parameters file
lattice.dat      - initial lattice file<br>
Volumes.txt           - File containing transitions for each volume<br>
Output            - directory containing lattices after KMC steps<br>

#### Volumes.txt
Format:<br>
Hashkey, Number of directions, Number of barriers<br>
Displacement vectors in integer lattice units (x y z)<br>
Final hashkeys, barrier, rate, reverse barrier<br>

#### Output
Each ouput file is called KMC + step.dat<br>
Format:<br>
Number of atoms in lattice<br>
Simulation time<br>
Barrier height (or equivalent for deposition)<br>
Simulation cell dimensions<br>
List of atoms in lattice (species, x, y, z coordinates, charge)<br>
