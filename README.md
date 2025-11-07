Data Organization:
  A main folder for each experiment is created
  The main folder contains multiple subfolders named n°1, n°2, …
  Each subfolder contains a file named marche_aleatoire.txt (random walk data).
Random Walk Generation is done with Benzen_Sorter.ipynb

Benzen_Sorter.ipynb contains three types of programs:
  Preprocessing Program
    Reads molecule_energies.txt
    Generates a formatted file compatible with the rest of the workflow: analyse_matrices.json
  Random Walk Generators (four types):
    Type 1: Randomly selects molecules from molecule_energies.txt
    Type 2: Each step changes only one substituent from analyse_matrices.json
    Type 3: Type 2 + substituent change with rules specifying which substituents can change into which from analyse_matrices.json
    Type 4: type 3 + constraints on substituent positions relative to others from analyse_matrices.json. this code has not been used in the report    
  Single Experiment Data Collector
    Generates data from a single experiment
    Possibility to plot only a part of the data with molecules for each step


Multiple Experiment Data Collector : These codes should be executed from the folder containing the subfolders  n°1, n°2, … to properly read marche_aleatoire.txt.

  Autocorrelation_ploter.ipynb: Used to analyze autocorrelation in the random walk data.
  Energy_ploter.ipynb: Used to plot the energy values of the random walks.
  
