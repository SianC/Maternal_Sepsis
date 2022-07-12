# Maternal_Sepsis
This repository contains code associated with my work on Fair Reinforcement Learning for Maternal Sepsis.

Corresponding author: Siân Carey - mm16s4c@leeds.ac.uk

The data use in this research is from MIMIC-III (https://mimic.physionet.org/).

The code contained in this repository is detailed below.

Data is formatted using (in order):
1. Add_vaso_fluid_1
2. Add_rewards_2
3. Normalising_post_rewards_3

Maternal and matched patients are found using:
1. Cohorts

The RL model is run using:
1. RL_main_model

The physicians decisions were estimated suing:
1. MIMICIII_Physician

The visualisations were created using (order not necessary):
1. Feature_importance
2. Error_bars_graph
3. Heatmaps_and_graphs

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

