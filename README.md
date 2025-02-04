# Heart-Attack-Risk-Objective of the Analysis
This analysis is intended to provide an overview of the risk of heart attack of various age groups as well as cholesterol and liproprotein levels. The study also provides a predictive model for determining the likelihood of heart attacks.


Questions
1. What is the average distribution for total cholesterol, heart heart and diabetes levels across various age grades?
2. Determines if high cholesterol levels increase heart attack risk?
What is the relationship between Total Cholesterol and Heart Attack?
3. How does LDL and HDL infleunce Total cholesterol levels?
4. Generate the predictive model to determine likelihood of developing a heart attack?

Analysis

Data Collection and Description
The dataset was obtained from https://www.kaggle.com/datasets/shriyashjagtap/heart-attack-risk-assessment-dataset
The obtained csv file was imported into excel using the powerquery wizard and analyzed.
The dataset consist of 10 columns and 1000 rows

Data Transformation
The columns were accessed and set to appropriate data types
A new column "Gender" was created grading 1 as male and 0 as female using power query (=if (sex) = 1 then "Male" else "Female") and the dataset was loaded into ms excel
The dataset was evaluated to remove outliers by evaluating the lower and upper boundaries

First Quartile =QUARTILE.INC(updated_version[age],1)
Third Quartile =QUARTILE.INC(updated_version[age],3)
Interquartile =N6-N5
Lower Boundary =N5-(1.5*N7)
Upper Boundary =N6+(1.5*N7)

=IF([@age]<$N$10, "Wrong", IF([@age]>$N$11, "Wrong", "Correct"))
