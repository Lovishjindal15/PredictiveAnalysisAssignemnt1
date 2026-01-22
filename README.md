# PredictiveAnalysisAssignemnt1

Learning Probability Density Function using MLE
 Introduction
In this assignment, the objective is to estimate the probability density function (PDF) of real-world environmental data using Maximum Likelihood Estimation (MLE).
The given dataset contains NO₂ concentration values, which are first cleaned and transformed, and then modeled using a Gaussian distribution.
All implementation and analysis are performed using Google Colab.

Dataset Description
The dataset file data.csv contains multiple air quality attributes.
For this assignment, only the NO₂ (no2) column is used.
Preprocessing steps:
Missing values were removed
Non-numeric entries were discarded
Only positive NO₂ values were retained for analysis
After preprocessing, the data becomes suitable for statistical modeling.

Methodology
1. Roll Number Based Parameters
To ensure that every student gets a unique result, two parameters are derived from the roll number:
ar = 0.05 × (roll number mod 7)
br = 0.3 × (roll number mod 5 + 1)
These parameters control the transformation applied to the data.


2. Data Transformation
The original NO₂ values are denoted as x.
A non-linear transformation is applied to generate a new variable z:
          z=x+asin(bx)
This step slightly modifies the data while maintaining its overall distribution structure.


3. Assumed Probability Model
The transformed data is assumed to follow a Gaussian (Normal) distribution.
The probability density function is written as:

        

Where:
μ represents the mean of the distribution
λ controls the spread of the curve
c is a normalization constant


4. Parameter Estimation using MLE
Maximum Likelihood Estimation is used to learn the unknown parameters of the PDF.
The mean (μ) is calculated as the average of transformed data
The variance (σ²) is computed from the data
λ is calculated using 

​	
 
c is computed as 

​	
 
​	
 
These values represent the best-fit parameters for the given data.
