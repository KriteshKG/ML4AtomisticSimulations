7.5	How to use the source files associated with this Chapter?
The source files needed to reproduce the investigation laid out in this chapter are available in the GitHub repository linked at: 
https://github.com/KriteshKG/ML4AtomisticSimulations/tree/main/Chapter_7
The link consists of two different folders one for conducting the MD simulations and the other folder for ML model formation. 

7.5.1. MD simulation
The folder pertaining to MD simulations (named as MD_Simulations) consists of the required files to perform the nanoscale simulation of high velocity impact over bilayer graphene. The MD_Simulations folder namely consists of the following files: 
LAMMPS input script:	input_1.in
Tersoff IP: (for modelling silicon impactor)	SiC.tersoff
Datafiles:	data_perfect.xyz

The set of LAMMPS input script, IP files, and the datafile, can be used to perform the MD simulation. To run the simulation, the terminal is to be opened in the directory, and the following string of instructive code is to be entered:

lmp -in input.in -pk omp 4 -sf omp
The MD simulations results in a text file which records the increment in strain and the corresponding stress in X (along the loading direction) and Y (lateral direction), which can be used to deduce the stress-strain profile of the graphene configurations, in terms of fracture strength. 


7.5.2. Machine Learning
Another folder in the provided GitHub repository, named as Machine Learning consists of two files, first, the excel file (Dataset.xlsx) which is the dataset for the discussed regression problem, second, the python notebook (Chapter_7.ipynb) for executing the ML model-based investigation reported in this chapter. This notebook can be opened within Google COLAB environment or by using Jupyter notebooks in the local machine. Other necessary excel files used in the python notebook is also provided in this folder.
