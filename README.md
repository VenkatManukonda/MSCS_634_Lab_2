### MSCS_634_Lab_2
Lab Overview

In this lab, I compared K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) using the Wine dataset from scikit-learn. The goal was to see how changing the neighborhood settings affects classification accuracy and to better understand how distance-based classifiers behave under different parameter values.

What I Did

I loaded the Wine dataset, explored the feature information and class distribution, and split the data into training and testing sets. Since both KNN and RNN rely on distance calculations, I standardized the features before training the models.

For KNN, I tested k values of 1, 5, 11, 15, and 21. For RNN, I tested radius values of 350, 400, 450, 500, 550, and 600. After training each model, I recorded the accuracy and created visualizations to compare the results.

What I Learned

The KNN model performed very well on this dataset. Accuracy increased from 97.22% to 100% as the value of k increased. Once k reached 11, the model classified all test samples correctly and maintained that performance for larger values.

The RNN results were unexpected because every radius value produced the same accuracy of 38.89%. After investigating the results, I found that the selected radius values were extremely large compared to the scaled feature range. Because of this, almost all training samples were treated as neighbors, which prevented the model from capturing meaningful local patterns.

Key Takeaway

The biggest lesson from this lab was that model parameters must be considered together with the scale of the data. KNN performed well because it used a fixed number of neighbors and preserved local information. RNN was much more sensitive to the radius setting, and the chosen values resulted in neighborhoods that were too large for effective classification.

Based on the results, KNN was clearly the better choice for the Wine dataset and produced the most accurate predictions.

Challenges

The most challenging part was understanding why RNN produced identical accuracy values for every radius. At first, it looked like the model was not responding to parameter changes. After examining the scaled feature range, it became clear that the radius values were so large that they created nearly identical neighborhoods for every prediction.
