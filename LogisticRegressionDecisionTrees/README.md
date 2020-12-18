Part 1: Wisconsin Breast Cancer Dataset
The following data was obtained from a study where 3D images were taken of a
breast mass. The features are measurements of the mass, the goal is to use these
measurements to predict the diagnosis (m=malignant and
b=benign). For a more detail understanding of the values see the link below:
https://www.kaggle.com/uciml/breast-cancer-wisconsin-data
The file is provided in as a csv file called data.csv. Read it in and call it cancer_data.
The four features we are interested in are radius_mean, texture_mean,
smoothness_mean, compactness_mean.
1. Create a boxplot for each variable to visualize the distribution of the values
between malignant and benign samples. Which of the four variables will
be most accurate in predicting by itself ? Explain why. (Hint – try creating
boxplots)
2. Randomly remove 20% of our data and save it as test_set and the other 80%
as training_set.
a. Make sure your test_set and training_set datasets will have the same
proportion of Benign and Malignant.
3. Using the training_set, create a logistic regression model using the glm()
function described in our lecture to create a model for each variable
separately.
a. Calculate accuracy, recall, and true negative rate using the test_set to
determine which of the four variables is the most helpful predictor.
4. Repeat step 3 but this time with all the variables together. Does this improve
the performance ? What conclusions can you draw from the coefficients?
Part 2: Using a decision tree.
5. Which variable do you expect to be at the root of the decision tree? Explain
your answer and use a graph to support your answer.
6. Using the same training_set and test_set perform a decision tree using the
“Party” package.
7. Change the max_depth parameter and calculate your accuracy, precision, and
recall for each depth. At which point do you think you have the least amount
of over-fitting?