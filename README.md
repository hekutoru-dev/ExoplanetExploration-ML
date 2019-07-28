# ExoplanetExploration-ML
Create machine learning models capable of classifying candidate exoplanets from a raw dataset

## Background
Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.
To help process this data, we need to create machine learning models capable of classifying candidate exoplanets from the raw dataset.

What we will find in this assignment:

1. Preprocess of the raw data
2. Tune the models
3. Comparasion of models

### Preprocess of the Data

We started by cleaning the data, removing unnecessary columns, and scaling the data.<br>
The raw data used in this analysis initially is a 5 roxs x 50 columns data set. In this dataset there are some columns that won't be needed nor useful for our analysis. So we started by droping those columns.<br>
At the end of this process of cleaning data, and keeping the data we are interested in we end up with a 5 rows x 40 columns features dataset and a "y" target values vector.<br><br>

We scale the data using the MinMaxScaler to add robustness to a very small standard deviations of features. Ee can see that for original dataset differences of values between features are in some cases are very big.

Once the dataset is cleaned and optimized for analysis, our next step is to Scale the data and create a SVC model and train it.

We can see that there a 3 labels that we want to classify: CANDIDATE, CONFIRMED & FALSE POSITIVE. Meaning that we need to discover how to predict new classifications in these 3 classes, for each new data coming up.

### Tunning

We used GridSearch and set the hyperparameters to generate candidates for the estimator and passed the parameters'C': [30, 32, 34, 36, 38, 40, 42, 44, 46, 48], and 'gamma': [1, 3, 5, 7, 10]}. By doing this we found that the best C = 42, and gamma = 1 for these parameters that we have tried. Also by looking at the confusion matrix we can see that there is a fine accuracy. Althoug there is a cosiderable amount of missings for the first classification when using the test data. Still, there is a good amount of success hits for all  3 classes. So, at these values for gamma & C is where the models seems to be stable.



### Evaluation





### Conclusions





