5.1	How to use the source files associated with this Chapter?
The source files needed to reproduce the investigation laid out in this chapter are available in the GitHub repository linked at: 
https://github.com/KriteshKG/ML4AtomisticSimulations/tree/main/Chapter_5
The link consists of two different folders one for conducting the MD simulations and the other folder for ML model formation. 
5.5.1. MD simulation
The folder pertaining to MD simulations (named as MD_Simulations) consists of the required files to perform the nanoscale simulation of uniaxial tensile deformation over different configurations of monolayered graphene. The MD_Simulations folder namely consists of the following files: 
LAMMPS input script:	input_deformation.in
Tersoff IP:	SiC.tersoff
Datafiles:	
	•	Perfect graphene:                                       	data_perfect.xyz
	•	Single vacancy (SV) defected graphene:	data_sv.xyz
	•	Si doped graphene:                                     	data_si.xyz
	•	Combined SV and Si graphene:                	data_combined_sv_si.xyz

At a time, the set of LAMMPS input script, Tersoff IP, specific datafile, can be used to perform the MD simulation. To run the simulation, the terminal is to be opened in the directory, and the following string of instructive code is to be entered [5.11]:
lmp -in input_deformation.in -pk omp 4 -sf omp
The same LAMMPS input script can be used by changing the specific command within the script-
read_data	 <use the specific file>.xyz
The MD simulations results in a text file which records the increment in strain and the corresponding stress in X (along the loading direction) and Y (lateral direction), which can be used to deduce the stress-strain profile of the graphene configurations, in terms of fracture strength. 
5.5.2. Machine Learning
Another folder in the provided GitHub repository, named as Machine Learning consists of two files, first, the excel file (Dataset.xlsx) which is the dataset obtained from the MD simulations, second, python (COLAB) notebook for executing the ML model-based investigation reported in this chapter. This notebook can be opened within Google COLAB environment or by using Jupyter notebooks in the local machine. 

