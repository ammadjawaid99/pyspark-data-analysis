# Predictive Analysis using PySpark Machine Learning Library (MLlib)

This repository contains processing, cleaning, descriptive and predictive analysis on publicly available data set of Titanic passengers. All the processing and analysis has been carried out using PySpark library.

This repository contains a Jupyter Notebook which includes descriptive and predictive analysis carried out on the Titanic Dataset using the PySpark library of Python. The dataset includes the information about the passengers who were on-board in the Titanic. This information includes their age, sex, family size, cabin, fare, survived etc. The data set has been taken from Kaggle. Source: https://www.kaggle.com/c/titanic

### Methodology
The approach which has been followed in solving the problem is give below as the flow chart:
![image](https://user-images.githubusercontent.com/70509472/235535226-0aeceac9-d32e-4f31-acd1-ca825c648560.png)

#### - Reading the dataset
The Titanic data which is available to us as the CSV file is read into the spark data frame by creating a SparkSession object using the PySpark library. And then we use the read.csv() method of the PySpark to store the csv in a variable.

#### - Data Pre-Processing & Cleaning
This step is the most important since it helps to ensure data quality, consistency, completeness, efficiency, as well as analysis accuracy. Cleaning data is important because it helps us to remove outliers and detect and remove missing or duplicate values.

#### - Data Visualization & Analysis
Data visualization is important because it facilitates visual data analysis and decision-making by leveraging human perceptual and cognitive abilities. For this project, we have analysed the different variables in the dataset with Survival variable to get how it is correlated with different features such as 'Sex', 'Fare', 'Pclass', 'Cabin', etc.

#### - Feature Selection
I selected only those columns that will be useful for us in performing the machine learning classification. Since it is reduntant and useless to include the features which don't add any value to the trained machine learning model, therefore we remove such columns. We remove 'PassengerId', 'Name', 'Ticket', and 'Cabin' from the data set.

#### - Machine Learning Classification
Machine learning algorithms can be applied on spark data frames using MLlib library, which provides us a range of ML models for classification and regression tasks. Since our label in the data is binary, therefore we need to perform classification. Two different machine learning models have been trained namely random forest and logistic regression. Before training the models, the dataset is split into training and test data so that the model’s accuracies could be assessed using different parameters such as f1-score, precision, recall, etc. 

### Contributing

If you have any suggestions or find any bugs, feel free to open an issue or submit a pull request.

