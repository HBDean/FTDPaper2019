# FTDPaper2019
Input files for the 2019 Frontiers Neurology manuscript entitled "Neurodegenerative disease–associated variants in TREM2 destabilize the apical ligand-binding region of the immunoglobulin domain."

For more information, please contact the corresponding authors: Yuhua Song (yhsong@uab.edu) or Erik Roberson (eroberson@uabmc.edu)

Each subdirectory contains the necessary input files used for the simulation of a single variant model.
Subdirectories are named according to the variant name within the manuscript.

UAB High Performance Computing's Cheaha cluster only allows individual runs up to 150 hours, so simulations are split into multiple segments.    
The order of these segments from the end of the heating protocol (at 300K) for each variant is as follows: 

  eq-300K.rst  --md.in-->  md.rst  --ext.in-->  ext.rst  --ext.in-->  ext2.rst  --ext.in-->  ext3...

Types of input files:

  .rst -> "restart" coordinate files for the starting frame of each segment of the trajectory.
           
  .prmtop -> parameter/topology files describing the atoms (protein, solvent, ions) associated with the simulations. 
           Each variant was run with a single .prmtop file throughout.
           
  .in -> input parameters to begin a run from a set of coordinates and a parameter/topology using Amber14. 
           As stated above, md.in was used for the initial step of the simultaion and ext.in was used to extend the MD simulations for all following steps.
            
Final trajectories in binary .binpos format are available from the Open Science Framework at (https://osf.io/a6yqv/). Other trajectory formats (including human readable or containing unit cell information) are available upon request.

All simulations were carried out using the AMBER14 suite (ambermd.org) and AMBER ff14sb force fields. 
Additional information, including hardware specifications, is contained within the manuscript text. 
DOI: Pending
