# Breast_cancer_study-

## Overview
Analyzing the well-known breast cancer dataset with seaborn plots. Based on this, a feature selection step is also included by filtering redundant correlated features along with eliminating some non-predictive features. The ML models then finally take advantage of this exploratory analysis.

## About the dataset
The [Breast Cancer Diagnostic](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29) data is available on the UCI Machine Learning Repository.

Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image.

The label is a final diagnosis, hence binary - M = Malignant, B = Benign. There are 10 real valued features :

1. radius (mean of distances from center to points on the perimeter)
2. texture (standard deviation of gray-scale values)
3. perimeter
4. area
5. smoothness (local variation in radius lengths)
6. compactness (perimeter^2 / area - 1.0)
7. concavity (severity of concave portions of the contour)
8. concave points (number of concave portions of the contour)
9. symmetry
10. fractal dimension ("coastline approximation" - 1)

The mean, standard error and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.

Class distribution: 357 benign, 212 malignant


## Technical details

 - This [notebook](https://github.com/jyotisman-ds/Breast_cancer_study-/blob/master/BreastCancer_EDAandML.ipynb) does an extensive exploratory data analysis using the impressive visualization tools provided by seaborn.
 - Violin plots, for instance is very useful for binary data. It plots the distribution of each label side by side for each feature in the dataset. This could help determine which features can help separate the labels more than some other features.
 - An alternative to violin plots is box plot which instead of showing the entire distribution, only focuses on the quantiles for each feature. Box plots are also useful in figuring out outliers.
 - Other options explored here are joint plots, pair grids and swarm plots.
 - Another important visualization tool is heatmap that helps find the correlations between features. This helps eliminate redundant features and hence reduces dimensionality.

### Machine Learning models

- Here, we use sklearn's support vector classifier (SVC) and also a gradient boosted tree to train our model.

- Finally, a grid search is employed to find the best parameters for the model.
