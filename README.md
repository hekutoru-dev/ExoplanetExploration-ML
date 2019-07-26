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






### Tunning

The GridSearch





### Evaluation





### Conclusions





