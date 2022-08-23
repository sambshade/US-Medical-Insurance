# US-Medical-Insurance
 US Medical Insurance predictions from Kaggle dataset

Python Analysis and Visualization Project from Codecademy
This project analyzes the CSV file from Kaggle regarding Medical Cost Personal Datasets. The dataset includes the following information:
* age: age of primary beneficiary
* sex: insurance contractor gender, female, male
* bmi: Body mass index, providing an understanding of body, weights that are relatively high or low relative to height, objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9
* children: Number of children covered by health insurance / Number of dependents
* smoker: Smoking
* region: the beneficiary's residential area in the US, northeast, southeast, southwest, northwest.
* charges: Individual medical costs billed by health insurance

The goal of this project is to understand which characteristics drive the cost of insurance the most and model the data to provide a reasonable estimate for insurance costs.


# Conclusions:

Based on visualizations, there are no obvious difference in insurance charges based on the sex of the patient or the region in which the patient is from. The biggest indicator for increased insurance charges is whether or not the patient smokes.

While the AdaBoost model is more accurate, we can utilize the linear regression model to make a simple equation to reasonably predict the insurance charges. Utilizing the coefficients and intercept given from the Linear Regression Model, we can predict the insurance costs with the linear equation below to approximately 78% accuracy and a MSE value of approximately 36,000,000. These numbers vary once the program is ran multiple times; however, the initial test yielded the following equation:

* charges = 256.372*age + 150.931*sex + 319.395*bmi + 518.989*children + 23593.569*smoker + 254.553*region - 12440.587 
 
This model verifies what was previously visualized: smoking has the most dramatic increase in the cost of insurance. BMI and number of children then play the most dramatic increase in the cost of insurance, while the sex of the patient is the least important factor. 
