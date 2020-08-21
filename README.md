### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Motivation <a name="motivation"></a>

This is the Udacity experiment design project. I was interestested in using Starbucks promotion experiment data to:

1. Analyze the results of the experiment and identify the effect of the Treatment on product purchase and Net Incremental Revenue;

2. Build a model to select the best customers to target that maximizes the IRR (Incremental Response Rate) and NIR (Net Incremental Revenue), where

   IRR = (# of Purchasers In Treated)/(Total # of customers in Treated)  - (# of Purchasers In Control)/(Total # of customers in Control), 

   NIR = [(# of Purchasers in Treated *$10) – (# of Treated Customers *$0.15)]  -  [# of Purchasers in Control * $10];

3. Score the ‘Test.csv’ using the model and select the best customers for promotion.

## File Descriptions <a name="files"></a>

There is one notebook available here to showcase work related to the above questions. The notebook is exploratory in searching through the data pertaining to the questions showcased by the notebook title.  Markdown cells were used to assist in walking through the thought process for individual steps.  

There are two data files used in the notebook. "training.csv" is the file for taining data and "Test.csv" is the file for test data.

Each data set has the same features as below:

Treatment – Indicates if the customer was part of treatment or control

Purchase – Indicates if the customer purchased the product

ID – Customer ID

V1 to V7 – features of the customer

## Results <a name="results"></a>

The purchase rate is only 1% in the training data. Different classifiers are tried and XGBoostClassifier is chosen to classify potential customer to make purchase. An optimization funcion is used to select the best threshold to maximize IRR and NIR on training data.

The promotion model is testd on the test data and got:
IRR is 0.0176;
NIR is $ 110.55.

## Licensing, Authors, Acknowledgements <a name="licensing"></a>

Must give credit to [Udacity data science nano degree course](https://www.udacity.com/course/data-scientist-nanodegree--nd025) and [Starbucks](https://www.starbucks.com/) for the data. 
