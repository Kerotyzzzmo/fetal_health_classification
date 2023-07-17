# fetal_health_classification

## Introduction 
In recent years, machine learning has shown great potential in predicting fetal health status by
analyzing Cardiotocograms (CTG) data. The ability to correctly classify fetal health status using machine learning algorithms can assist healthcare providers in detecting potential issues in the early stage and providing intervention to improve fetal health. This analysis employed a data-driven approach using CTG data in predicting fetal health in three categories: normal, suspicious, and pathological. Additionally, we will apply two dimension reduction techniques: principal component analysis (PCA) and t-Distributed Stochastic Neighbor Embedding (t-SNE) to reduce complexity while retaining valuable information for analysis.

## Data Exploration 
The dataset consists of 2126 records, including 23 features and 3 classifications (Normal, Suspect, Pathological). The dataset is well-suited for building classification machine learning models to predict fetal health status based on the available feature. This is a highly imbalanced dataset, with 1655 cases classified as normal, 295 classified as suspect and 176 classified as pathological. Such a pattern is very normal for medical diagnoses. To address the issue of imbalanced data, we use random oversampling to increase the pathological and suspect cases.

## Data Visualization 
* Dropdown menu that enables to select an attribute to visualize its skewness.
* Interactive 3D PCA visualization
* Interactive 3D t-SNE visualization 

## Algorithms 
* Adaboost
  * Applied grid search with 10-fold cross-validation to find the best hyperparameters for Adaboost on the original dataset and oversampled dataset.
* SVM
  * The hyperparameter kernel = 'linear' is set in this analysis.
* Naive Bayesian
  * Assumed that the likelihood function follows Gaussian distribution.
 
## Results 
* Adaboost has the best overall performance with an accuracy of 0.91 on oversampled data. SVM has 0.87 and Naive Bayes has 0.72.
* From the interactive PCA plot, there are several points in the top right corner that are far away from most of the data points. These could be potential outliers. The clusters of data points
that are close to each other indicate that they share similar characteristics or belong to the same group.
* Compared to PCA, there are no clear outliers in the t-SNE plot. The proximity between data points in the t-SNE plot suggests that each class shares similar characteristics, which is also
consistent with the result from the PCA analysis. 
