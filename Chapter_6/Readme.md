6.5	How to use the source files associated with this Chapter?
The source files needed to reproduce the investigation laid out in this chapter are available in the GitHub repository linked at: 
https://github.com/KriteshKG/ML4AtomisticSimulations/tree/main/Chapter_6
The link consists of two different folders one for conducting the MD simulations and the other folder for ML model formation. 
6.5.1. MD simulation
The folder pertaining to MD simulations (named as MD_Simulations) consists of the required files to perform the nanoscale simulation of high velocity impact over bilayer graphene. The MD_Simulations folder namely consists of the following files: 
LAMMPS input script:	input.in
Tersoff IP: (for modelling silicon impactor)	SiC.tersoff
AIREBO-m: (for modelling bilayer graphene)	CH.airebo-m
Datafiles:	BLG_20_20.xyz

The set of LAMMPS input script, IP files, and the datafile, can be used to perform the MD simulation. To run the simulation, the terminal is to be opened in the directory, and the following string of instructive code is to be entered:
lmp -in input.in -pk omp 4 -sf omp
The MD simulations results in a text file named “output_data_bball.txt” which records the temporal variation in kinetic energy of the impactor, which is used to obtain the pre-impact and post-impact kinetic energy of projectile, which is then used to calculate specific penetration energy by utilizing the equation 6.1. 
6.5.2. Machine Learning
Another folder in the provided GitHub repository, named as Machine Learning consists of three files, first, the excel file (Data_regression.xlsx) which is the dataset for the discussed regression problem, second, the excel file (Data_classification.xlsx) which is the dataset for the discussed classification problem, the third file (Chapter_6.ipynb) is a python (COLAB) notebook for executing the ML model-based investigation reported in this chapter. This notebook can be opened within Google COLAB environment or by using Jupyter notebooks in the local machine. 
