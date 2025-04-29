9.6	How to use the source files associated with this Chapter?
The source files needed to reproduce the investigation laid out in this chapter are available in the GitHub repository linked at: 

https://github.com/KriteshKG/ML4AtomisticSimulations/tree/main/Chapter_9

The link consists of two different folders one for conducting the MD simulations and the other folder for ML model formation. 

9.6.1. MD simulation

The folder pertaining to MD simulations (named as MD_Simulations) consists of the required files to perform the nanoscale simulation of uniaxial tensile deformation over designed configuration of high entropy alloy. The MD_Simulations folder namely consists of the following files: 

LAMMPS input script:	input.in
Interatomic potential: for modelling HEA	FeNiCrCoAl.eam.alloy
Interatomic potential: for modelling Au projectile	Au_5T.eam.alloy
Datafile:	Fe_29.57Cr_12.71Ni_7.2Co_40.47Al_10.xyz


The set of LAMMPS input script, datafile and IP files, can be used to perform the MD simulation. To run the simulation, the terminal is to be opened in the directory, and the following string of instructive code is to be entered:

lmp -in input.in -pk omp 4 -sf omp

The MD simulations results in a text file (output_impactor.txt) which records the temporal variation in kinetic energy of the impactor, which is used to obtain the pre-impact and post-impact kinetic energy of projectile, which is then used to calculate kinetic energy dissipation (ΔKE) by utilizing the equation 9.2. 
 
9.6.2. Machine Learning

Another folder in the provided GitHub repository, named as Machine_Learning consists of two files, first, the excel file (Impact_Dataset.xlsx) which is the dataset for the discussed regression problem, second, the python notebook (Chapter_9.ipynb) for executing the ML model-based investigation reported in this chapter. This notebook can be opened within Google COLAB environment or by using Jupyter notebooks in the local machine. Other necessary excel files used in the python notebook is also provided in this folder.
