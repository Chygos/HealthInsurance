# HealthInsurance
Project to predict the medical costs (in charges) to be covered by a health Insurance

### link to dataset (https://www.kaggle.com/mirichoi0218/insurance) 

# Objective 
To build a machine learning model to predict the charges to be paid (as charges) by an insurance company, as a health Insurance cover.

### Evaluation Metric: R$^2$  

The solution contains seven linear models. It is found that beneficiaries who are smokers incur a lot of medical bill for the insurance company.
For smokers, the BMI is strongly related (positively) to the amount of charges. As the BMI increases, the medical costs increases too.

## Polynomial and Feature Interactiins
Using the raw features wasn't enough to predict the amount of charges. As a result interactions between the age and smoker = 'Y' and BMI and smoker = 'Y'. 
As a baseline, the R$^2$ stands at about 75 (for test set) for all seven models. 
Feature interaction improved the R$^2$ (amount of variance explained by the model) to between 79-80. 
As a final technique, second order polynomial of the age and BMI or beneficiaries was added as features. This slightly increased the R$^2$ by ~0.03. 


### Other techniques for improvement
1. Since the dataset is small, a non-linear model such as decision trees and random forests can be used
2. If linear models are to be used, a feature selection technique could be used to select relevant features and drop the redundant ones. This selection is best evaluated using the Adjusted R$^2$ as the Adjusted R$^2$ penalises more features to be added.
Another method could be to create higher polynomial orders but this tend to overfit the data as higher orders are chosen. 
3. Weak learners could be bagged for more robust predictions.

