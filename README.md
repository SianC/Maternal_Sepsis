# Maternal_Sepsis
This repository contains code associated with my work on Fair Reinforcement Learning for Maternal Sepsis.

Corresponding author: Siân Carey - mm16s4c@leeds.ac.uk

The data use in this research is from MIMIC-III (https://mimic.physionet.org/).

The code contained in this repository is detailed below.

Data is formatted using (in order):
1. Add_vaso_fluid_1: This code requires the dataset of sepsis patients and relevant features. This code returns the dataset with additional columns for the grouped vasopressor and IV fluid dosages.
2. Add_rewards_2: This code requires the dataset resulting from the code above. This code returns the dataset with additional columns for rewards (both intermediate and final). This code requires you to pick the weighting for the intermidiate rewards.
3. Normalising_post_rewards_3: This code requires the dataset resulting from the code above. This code requires the patient ids for the respective chosen cohorts. This code returns scaled and unscaled normalised data for each given cohort and each test/train/validation set and the scaled normalised data with an additional column noting the change in vasopressor.

Maternal and matched patients are found using:
1. Cohorts: This code requires the original sepsis data (or any dataset that is this with additional columns) and the list of pregnant ids. This code returns all the information in the original dataset for each cohort.  

The RL model is run using:
1. RL_main_model: This code requires the train/test/validate and cohort data sets that are normalised with change in vasopressor added. This code returns the actions taken by the model throughout training and to the test and cohort data sets. This code requires that you pick a number of steps to train the model for.

The physicians decisions were estimated suing:
1. MIMICIII_Physician: This code requires the train/test/validate and cohort data sets that are normalised with change in vasopressor added. This code returns the actions taken by the model (that estimate the original clinicians actions) throughout training and to the test and cohort data sets. This code requires that you pick a number of steps to train the model for.

The visualisations were created using (order not necessary):
1. Feature_importance: This code requires the test, train and validation data sets and their relevant actions. This code returns graphs of feature importance.
2. Error_bars_graph: This code requires model results as above for 10 models. This code returns graphs of feature importance with error bars.
3. Heatmaps_and_graphs: This code requires the data sets for the cohorts and the relevant actions. This code returns heatmaps for the actions of the cohorts.

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

