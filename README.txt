
 ## Investigating trends in COVID-19 survey responses based on patient status using SVM ##


## Project components: ##
- BIOF509 OOP. py (SVM script using OOP) 
- BIOF509 Final Project.py (SVM script written linearly to use if you want to visualize each step in the pipeline)
- COVID19_Data.xlsx 

## BIOF OOP.py ##
Overview: Defines a class SVM which does the following:
- pre-processes data
- scales data using normalization
- reduces dimensions using PCA
- splits dataset into training and testing
- fits data to SVM
- returns accuracy of the model and confusion matrix
- returns name of each feature that was most important for each principal component

Inputs: 
- excel: predefined variable with path to your data sheet (make sure this is an excel spreadsheet)
	-put your labels in the first column of dataset, and all features in the following columns\
- kernel: specify the type of kernel you would like to use\
	- options include "linear," "rbf," "poly," "sigmoid," 
- n_components: specify how many components to use for PCA

Outputs: 
- accuracy of model (decimal format)
- confusion matrix
- name of each feature that was most important for each principal component

## Example: ##
data= '/Users/goyalsl/Desktop/COVID19_DATA.xlsx'
demo = SVM(data)
demo.svm(kernel="rbf")
demo.scale()
demo.pca(4)
demo.confusion_matrix()
demo.pca_features()
demo.accuracy()
