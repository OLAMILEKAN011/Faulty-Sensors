# Faulty-Sensors
ML classification to identify faulty machines by sensor readings

## Overview
This is a project I built for predictive maintenance of machineries along a production line. This could be useful in production companies where a lot of different machines work simultaneously and breakdown has to be prevented or minimized to the barest minimum by equipping the machines with vibration sensors for monitoring.  The historical data collected from individual sensors could be used to build models which could be helpful to make informed predictive maintenance plans.

I was able to build a model that predicts fault status of machines in a production line from their vibration sensor readings with 96.8% accuracy after tuning. To get this result, I have used a decision tree and random forest classifier to train the dataset collected from sensors in machines to build this model.

## Notes
This notebook takes you through the process of predicting if a machine part will fail or not by classifying based on the sensor reading of the machine. [Fauly_machine](https://github.com/OLAMILEKAN011/Faulty-Sensors/blob/main/Faulty%20Machine%20Sensor.ipynb)

## Config
I recommend using pyspark in azure datbrick notebook for this project for easy running. This code can also be viewed in jupyter notebook.

## Data
The dataset is a numerical data for one thousand machines with twenty sensor readings each. The data is labelled and the label column is categorical.
