# Adult’s PSTRE Level Prediction

This project is to be conducted on a (part of) international large-scale assessments for adults –The Programme for the International Assessment of Adult Competencies (PIAAC). This study is to use process variables, behavioral variables or background variables, apply supervised machine learning methods, to make a prediction on the problem- solving skill levels (PS_class) as accurate as possible.

## Dataset

- PIAAC_US_2012_subsample.csv

The dataset includes 664 respondents, all of them took 14 PSTRE items. A total of 588 variables are used, including the gold standard “PS_class” as the final variable.

- Variable information.xlxs

This document provides a codebook to explains about variable labels and values (esp. for nominal and ordinal variables) in the PIAAC_US_2012_subsample.csv

Variables 3-139 are related to behavioral variables, variables 139-587 are related to background variables, variable 588 is the gold standard “Class”.

More information can be found on [OECD PIAAC website](https://www.oecd.org/skills/piaac/data/).

## Data Wrangling and Data Exploration

- Deal with missing values
- Remove some character variables from behavior features
- Calculate Pearson correlations and keep those variables that have higher correlations with target variable “PS Class”
- Create a new variable that sums the numbers of actions for 14 different problem-solving units

## Methods
The project randomly selects roughly 20% of the sample (127 observations) as the test set, and the train set is separated into ten folds for the training-validation purposes.

Three supervised methods are utilized:
- Conditional Inference Tree
- Support Vector Machine with Linear Kernel and Radial Basis Kernel
- Random Forest
