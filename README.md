# ExoplanetExploration-ML
Data Analytics (Assignment 21)

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

### SVM
By itself, the SVM algorithm gave us a Training Data Score: 0.8995120463555962 and Testing Data Score: 0.8870082342177493. This values are nice fit. We cannot see over fitting nor underfitting. This parameters were given by having values of gamma = 1 and C = 40. <br><br>

### GridSearch & Tunning

After GridSearch and set the hyperparameters to generate candidates for the estimator and passed the parameters'C': [30, 32, 34, 36, 38, 40, 42, 44, 46, 48], and 'gamma': [1, 3, 5, 7, 10]}. By doing this we found that the best C = 42, and gamma = 1 for these parameters that we have tried. Also by looking at the confusion matrix we can see that there is a fine accuracy. Althoug there is a cosiderable amount of missings for the first classification when using the test data. Still, there is a good amount of success hits for all  3 classes. So, at these values for gamma & C is where the models seems to be stable.<br>
At these level of gamma there is a great influence in what X features are doing.
<br><br>

### Logistic Regression Model
The logistic regression model gives an accuracy of 0.84568 for the training data & 0.83714. This model it is also closer between training and test meaning we have a nice fit.

### Comparison of Models
As we can see, when using the SVM model we got a test score of 0.88700. After the GridSearch tunning we got that the best test score was 0.8824336688014639. There is not a big difference between these values, but it seems that the SVM alone is working a little beter.<br>
Looking at both confusion matrixes we can see that there is a slightly difference in the first class (CANDIDATE label). It seems that there is better accuracy at hitting the positive values when using the GridSearch tunning than the SVM alone. <br><br>

Comparing these models with the logistic regression model. The logistic regresion model a little worse, although there is not a big difference with the socres. It is cleary visible that the confusion matrix is showing bad behavior for the first class. <br><br>

Aware from this. We can see that for the 3rd class, all models are working nice, as they are hitting most of the values as positive.



