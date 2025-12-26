# Code and data for the paper: Variance in C. elegans gut bacterial  load suggests complex host-microbe dynamics

All the data required to generate the figures are assumed to be in a subfolder named "Data" and all the corresponding code is assumed to be in a subfolder named "code". Outfil files for Maximum likelihood estimation (Figure 3) are also in the subfolder "code".

Analysis notebooks are independent and can be run in any order.

Analyses were done with the following package versions:

    - python: 3.11.4
    - matplotlib: 3.7.1
    - scikit-learn: 1.3.0
    - pandas: 1.5.3
    - numpy: 1.24.3
    - scipy: 1.10.1
    - seaborn: 0.12.2

## Figure 1
Figure 1 in the main text is generated in notebook "WormMatters_Fig1.ipynb" using data files:
* MYbSpecies.csv - datafile with bacterial loads inside worms for all the bacterial species
* invitro_082819.csv - datafile with bacterial growth outside the worm
* MYb71.csv - datafile with bacterial loads for the species MYb71
* MYb120.csv - datafile with bacterial loads for the species MYb120

## Figure 2
Figure 2 in the main text is generated in notebook "HetCarryingCap_fig2.ipynb" using data files:
* MYb71 CD.csv - datafile with bacterial loads for the species MYb71 at different colonization densities    
* MYb120 CD.csv - datafile with bacterial loads for the species MYb120   at different colonization densities 

## Figure 3
Figure 3 in the main text is generated in notebook "HetGrowthCol_Fig3.ipynb" using data files:
* MYb71.csv - datafile with bacterial loads for the species MYb71  
* MYb120.csv - datafile with bacterial loads for the species MYb120
Bacteria-specific MLE parameters for the logistic growth model are generated in notebooks "MLE Gridsearch for MYb71.ipynb" and "MLE Gridsearch for MYb120.ipynb" using the same data files.

## Figure 4
Figure 4 in the main text is generated in notebook "Inhibition_Fig4.ipynb" using data file:
* Inhibition_compiled.csv - datafile with bacterial loads for MYb14 under varying levels of chloramphenicol inhibition (25-500 ug/mL) and over time

## Figure 5
Figure 5 in the main text is generated in notebook "Migration_Fig5.ipynb" using data files:
* Migration_compiled.csv - datafile with Biosorter data for worms colonized with MYb14-GFP, 24 and 48 hours after being sorted into "low" and "high" GFP gates
* Migration_T0_fill.csv - datafile with Biosorter data for the initial population of MYb14-GFP colonized worms, from which the initial low/high sort was carried out

## Figure 6, 8, and 9
Figures 6, 8, and 9 in the main text are generated in notebook "MultistabilityModelSimulations_Fig6.ipynb". No data files are called.

## Figure 7
The GFP to CFU mapping in Figure 7 is generated in notebook "MappingGFPtoCFU.ipynb" using data files:
* CFU Mapping.csv - datafile with bacterial loads for the species MYb14 and the corresponding GFP reads in the experiment shown in Figure 6 in SI.
* LowInhT24.csv - datafile with bacterial loads for the species MYb14 and the corresponding GFP reads in the lowest-inhibition condition (chloramphenicol 25 ug/mL, no inhibition of bacterial growth inside worms) also shown in Figure 4

## SI Text
### Figure A in SI Text. Bacterial load in individual worms over time.
Figure A is generated in notebook "SI_Monocolonization.ipynb" and calls data files:
* MYb27.csv
* MYb45.csv
* MYb53.csv
* MYb238.csv
each of which contains data for bacterial loads of the indicated species in individual worms, in the same format as used in Figure 1.

### Figure B in SI Text. Fluorescent bead accumulation in adult worms
Figure B is generated in R script "SI_GreenBeadAccumulationN2.R" and calls data file:
* GreenBeadFeed1219.csv - datafile with Biosorter data for N2 worms allowed to ingest green fluorescent beads

### Figure C in SI Text. Bacterial load distributions under additional levels of inhibition of growth within hosts.
Figure C is generated in notebook "SI_Inhibition.ipynb" using data file:
* Inhibition_compiled.csv - datafile with bacterial loads for MYb14 under varying levels of chloramphenicol inhibition (25-500 ug/mL) and over time. Also used in Figure 4.

### Figure D in SI Text. Bacterial load switching between modes in an additional experimental run
Figure D is generated in notebook "SI_Migration.ipynb" using data file:
* Migration_run2_Compiled.csv - datafile with Biosorter data for worms colonized with MYb14-GFP as in Figure 5, but representing an independent run of the experiment

### Figure E. State switching in N2 adults colonized with Salmonella enterica LT2
Figure E is generated in R script "SI_SEStateSwitch.R" using data file:
* WormShedCFU.csv - datafile containing bacterial load data from a separate set of experiments, including colonization (bacterial load) data for individual worms exposed to GFP-labeled Salmonella enterica and sorted into low- and high-GFP bins

### Figure F. Probability distributions of GFP and CFU data
Figure F is generated in notebook "MappingGFPtoCFU.ipynb" using data files as in Figure 7.

### Figure G (Predictions of dynamics in the 6th order polynomial potential (5th order force) model) and H (Predictions of dynamics in the state switching model)
Figures G  and H are generated in notebook "MultistabilityModelSimulations_Fig6.ipynb". No data files are called.

