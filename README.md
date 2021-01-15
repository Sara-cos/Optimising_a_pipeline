# Optimising_a_pipeline

## Overview

This project is part of the Udacity Azure ML Nanodegree. In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model. This model is then compared to an Azure AutoML run. This is the analysed report or the research summary.

## Summary

The dataset used here is a information of Portuguese Bank Marketing. The informations is based on phone calls , age, type of job, marital, education, has credit in defualt, housing, loan, type of contact , last contact, day of the week of the contact, duration in seconds, campaigns, and other variables. We want to predict if the client has subscribed a term deposit. The csv file consist of 32950 row and 21 columns. 
The csv file(https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv). 

The best performed model was Voting Ensemble obtained through AutoMl with the primary metric accuracy as '0.9163'

## Scikit-learn Pipeline

First the workspace, experiment is created and compute configuaration is set with vm_size STANDARD_D2_V2 and max_nodes = 4. This set the infrastructure to run the projects.After that the details about the run were set, such as parameter sampling, policy and estimator SKlearn and the hyperdrive config created where the train.py file was called.

In the train.py, the data from url made into TabularDataset with TabularDatasetFactory. The data was cleaned, text variables were transformed into numerical variable. The clean data was split to train and test. In the main function of train.py the arguments were added, containing maximum iteration and regulation strength.
The model choosen was Logistic Regression.

