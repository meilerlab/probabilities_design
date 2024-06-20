# Code for "Self-supervised machine learning methods for protein design improve sampling, but not the identification of high-fitness variants"
![figure_1_overview_horizontal (2)](https://github.com/meilerlab/probabilities_design/assets/59534445/35dd28d5-2c5a-4245-81ad-8fc8c30eaeb7)

This repo contains the code for reproducing the results of the publication "Self-supervised machine learning methods for protein design improve sampling, but not the identification of high-fitness variants". If you are interested instead in using the implemented features for your own work, an overview of them [can be found in the Rosetta documentation here](https://www.rosettacommons.org/docs/latest/scripting_documentation/RosettaScripts/composite_protocols/Working-with-PerResidueProbabilitiesMetrics), and a tutorial is available from the Meiler Rosetta workshop 2023 ["Tutorial 2: Machine Learning in Rosetta"](https://meilerlab.org/rosetta-workshop-2023/).

## Running the different design protocols
Code for running the different design protocols can be found in the folder of each dataset, e.g. `emi/avg03.sh`. All scripts use the RosettaScripts XML provided in the main folder which are named after the different protocols shown in the paper. 

## Sequences and metrics of resulting designs
The unique sequences and calculated metrics of each design protocol are available in the dataset folders ("dataset/dataset_designs.csv"), e.g. `emi/emi_designs.csv`.

## Analysis of designs
The code for analyzing the resulting designs and reproducing figures can be found in the `design_analysis.ipynb` notebook. In order to run the jupyter notebooks, first create a python environment using the `environment.yaml` file with either conda or mamba:

```
# create environment
conda env create -f environment.yaml
# activate environment
conda activate probs_design
```

## Oracle model data and training
The code for training and evaluating the oracle models for each dataset can be found in the `model_training.ipynb` notebook. The datasets used for training can be found in each dataset folder, e.g. `gb1/gb1_mutations_full_data.csv`. The already trained models are also available, e.g. `gb1/gb1_ridge.joblib`.

## Rosetta code
The Rosetta source code can be found at https://github.com/RosettaCommons/rosetta/. Docker containers for Rosetta (including the Tensorflow/LibTorch extras version) can be found at https://hub.docker.com/r/rosettacommons/rosetta. 
