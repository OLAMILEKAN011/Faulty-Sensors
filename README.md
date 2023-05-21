# Faulty-Sensors
ML classification to identify faulty machines by sensor readings on azure databricks

## Overview
This is a project I built for predictive maintenance of machineries along a production line. This could be useful in production companies where a lot of different machines work simultaneously and breakdown has to be prevented or minimized to the barest minimum by equipping the machines with vibration sensors for monitoring.  The historical data collected from individual sensors could be used to build models which could be helpful to make informed predictive maintenance plans.

I was able to build a model that predicts fault status of machines in a production line from their vibration sensor readings with 96.8% accuracy after tuning. To get this result, I have used decision tree and random forest classifier to train the dataset collected from sensors in machines to build this model.

## Notes
This notebook takes you through the process of predicting if a machine will fail or not by classifying based on the sensor readings on the machine parts. [Fauly_machine](https://github.com/OLAMILEKAN011/Faulty-Sensors/blob/main/Faulty%20Machine%20Sensor.ipynb)

## Config
I recommend using pyspark in azure datbrick notebook for this project for easy running. This code can also be viewed in jupyter notebook. Login to databrick environment and create ML cluster. The dataset folder was uploaded to databricks and unzipped. Databrick MLflow was imported and instantiated to help monitor and log the entire ml process.  Dataset was imported into the databrick code environment and viewed for observations. Necessary packages were imported for data wrangling and visualization.

## Data
The dataset is a numerical data for nine thousand, two hundred and ninety-two machine readings with twenty sensor readings each. The data is labelled and the label column is categorical.

## EDA
The statistical information of the dataset was checked and studied to better understand. The dataset was converted to dataframe and further wrangling was done with pandas. A TempView of the dataset was created to enable further wrangling and analysis using SQL codes.

## Data Processing & ML
Data was converted into vectors with RFormula to perform ML operations. 
Dataset was then splitted to training set and test set in the ratio of 0.8 : 0.2 respectively.
The training dataset was trained with decision tree classifier, evaluated with the test data, optimized and evaluated again to get the it best performance result. This procedure was repeated using random forest classifier and conpared with the decision tree classifier for best performance. 

## Evaluation
After so much training and opetimization, it was observed that the random forest classifier outperformed the decision tree classifier with accuracy of 96.8%.

## Recommendation
It is recommended that this model should be used with the following parameters for the best model:
MaxDepth Parameter: 7, Impurity Parameter: entropy, MaxBins Parameter: 32
