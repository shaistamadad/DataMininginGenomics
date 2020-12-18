The Wisconsin Cancer dataset("data.csv" file)

The four features we are  interested in are 
radius_mean, texture_mean, smoothness_mean, compactness_mean.	
1.	Remove 20% of your data and save it as	test_set and the other 80% as training_set. 
a.	Make sure your datasets will have the same  ratio  of Benign and Malignant.

Part 1: SVM	
Build a predictive model with SVM using the training_set with the four different variables listed above to predict a benign or malignant tumour diagnosis.

a.	Try using different values for c. Which c gives the best performance?
b.	Use test_set to calculate the AUC of the best model created using the training_set.

Part 2. Neuralnet
 Build a predictive model with Neuralnet to classify the test_set based on the values from training_set.
a.	Try different size of hidden layers, ( 1, 10, 20). 
Calculate the AUC of the Neuralnet models to determine which gives the best result? 



