# MSCS_634_Lab_2

## Purpose

The purpose of this lab was to compare the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classification algorithms using the Wine dataset from scikit-learn. Different k values and radius values were tested to examine how parameter selection affects classification accuracy.

## Key Insights

* KNN achieved accuracies ranging from 97.22% to 100%.
* The best KNN performance was observed at k values of 11, 15, and 21.
* RNN achieved 38.89% accuracy for all tested radius values.
* The results showed that model performance can change significantly depending on how neighborhoods are defined.
* KNN was the more effective classifier for the Wine dataset.

## Observations

* Increasing k improved KNN performance and resulted in perfect classification accuracy.
* RNN performance remained unchanged because the assigned radius values were extremely large compared to the standardized feature range.
* Parameter selection plays an important role in distance-based learning algorithms.

## Challenges

* Understanding why RNN produced the same accuracy across all radius values required additional analysis of the scaled feature space.
* Interpreting the relationship between feature scaling and radius selection was an important part of the experiment.
