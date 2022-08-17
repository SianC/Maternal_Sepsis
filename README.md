# Maternal_Sepsis
This repository contains code associated with my work on Fair Reinforcement Learning for Maternal Sepsis (https://doi.org/10.1101/2022.08.09.22278582).

Corresponding author: Siân Carey - mm16s4c@leeds.ac.uk

The data use in this research is from MIMIC-III (https://mimic.physionet.org/).

To recreate these results:
1. Download MIMIC-III
2. Find the sepsis patients in MIMIC-III using AI Clinician Code (https://github.com/matthieukomorowski/AI_Clinician/blob/master/AIClinician_sepsis3_def_160219.m) - this requires MatLab.
3. Build the full database for required time periods using AI Clinician Code (https://github.com/matthieukomorowski/AI_Clinician/blob/master/AIClinician_mimic3_dataset_160219.m) - This requires MatLab.
4. Ensure all required packages are downloaded. More information below.
5. Run the Cohorts file. More information below.
6. Run the Preprocess file. More information below.
7. Run the RL model using RL_main_model and the Clinician model using MIMICIII_Physician. More information below.
8. Visualise the results using Visualisation. More information below.

Code here has been built off code presented by Jia (https://github.com/Yanjiayork/sepsisRL) and Raghu (https://github.com/aniruddhraghu/sepsisrl/tree/master/preprocessing)


Details about the code in this repository are below.

Maternal and matched patients are found using:
1. Cohorts: This code requires the original sepsis data (or any dataset that is this with additional columns) and the list of pregnant ids. This code returns all the information in the original dataset for each cohort.  

Data is formatted using:
1. Preprocess: This code requires the dataset of sepsis patients and relevant features, as well as the pregnant and control cohort patients and relevant features. This code returns scaled and unscaled normalised data for each given cohort and each test/train/validation set and the scaled normalised data with an additional column noting the change in vasopressor.

The RL model is run using:
1. RL_main_model: This code requires the train/test/validate and cohort data sets that are normalised with change in vasopressor added. This code returns the actions taken by the model throughout training and to the test and cohort data sets. This code requires that you pick a number of steps to train the model for.

The physicians decisions were estimated suing:
1. MIMICIII_Physician: This code requires the train/test/validate and cohort data sets that are normalised with change in vasopressor added. This code returns the actions taken by the model (that estimate the original clinicians actions) throughout training and to the test and cohort data sets. This code requires that you pick a number of steps to train the model for.

The visualisations were created using:
1. Visualisation: This code requires the test, train, validation, pregnancy and control cohort data sets and their relevant actions for both RL model and clinician. This code returns a graph of feature importance with error bars and  heatmaps for the actions on the pregnancy and control cohorts.


The Python packages required for this work are detailed below. (Versions as of February 2022):
1. pandas
2. numpy
3. random
4. matplotlib.pyplot
5. math
6. seaborn
7. sklearn.ensemble
8. cPickle
9. tensorflow
10. os
11. copy

