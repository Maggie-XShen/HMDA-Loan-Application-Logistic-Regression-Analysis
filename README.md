# HMDA-Loan-Application-Logistic-Regression-Analysis
Logistic Regression Analysis of HMDA Loan/Application Records - Loan Amount v.s. Socioeconomic &amp; Demographic Variables

## Dataset
Full dataset can also be found at: https://ffiec.cfpb.gov/data-publication/snapshot-national-loan-level-dataset/2022. To analyze more easily, I randomly sampled 20000 rows (with no outliers) of the original dataset which contains 99 columns and 16080210 observations.

## Methods
### Assumptions
#### Normality
Square root transformation of variable "loan_amount" ensured the originally right skewed distribution of loan_amount was set to a roughly normal distribution (disregarding outliers).
#### linearity, homoskedasticity, and independence are assumed and confirmed

### Statistical Approach
- H0: Demographic factors have no significant impact on loan approval rates and terms.
- H1: Demographic factors significantly influence loan approval rates and terms.

Using the glm() function in R Studio, I fit a linear regression on the response variable "sqrt(loan_amount)" and 11 predictor variables.

## Results
Results rejects H0 that that demographic factors have no significant impact on loan approval rates and terms (see Section III of paper).
