# Predicting Malignant Breast Cancer Tumors

## Overview

Using Breast Cancer Tumor data from the State of Wisconsin, the goal of this study was to develop a model that will predict Malignant tumors with the highest possible accuracy, and lowest level of false negatives. After using Logistic Regression, Decision Tree and Random Forest techniques on the data, the model was able to return an accuracy rate of ___.

![image](./PDF/national-cancer-institute-NbZQYileaOI-unsplash.jpg)


## Business and Data Understanding

### Business Understanding

According to healthline, breast imaging techniques such as mammograms, ultrasounds and MRIs can detect suspicious areas, but can’t tell a patient whether they have cancer or not – only a biopsy can fully diagnose cancer*.

An estimated 297,790 women are expected to be diagnosed with breast cancer in 2023, which the American Cancer Society notes is the second leading cause of cancer death in women**. 

What if there was a way, through existing imaging techniques, to get tumor measurements and be able to predict if it was malignant or benign? That is exactly what the purpose of this project is – creating a model that accurately predicts malignant tumors given existing measurements.

Sources: https://www.healthline.com/health/breast-cancer/can-a-radiologist-tell-if-it-is-breast-cancer , https://www.cancer.org/cancer/breast-cancer/about/how-common-is-breast-cancer.html

Using data from the State of Wisconsin on Breast Cancer tumors, can we predict whether a tumor is malignant? Getting an accurate model with a very small level of False Negatives is imperative, and could allow for malignant tumors to be identified faster than they normally would, which could mean better treatment results for the patients. 

We want a high accuracy rate, but ensuring that there are minimal amounts of False Negatives is equally or potentially even more important. If we have false negatives, then those patients could end up having a delayed diagnosis, and delayed treatment, which in some cases can be fatal.

### Data Understanding

The data was pulled from Kaggle.com, an AirBnb for data scientists. Kaggle is a crowd-sourced platform to attract, nurture, train and challenge data scientists.

From there, I pulled a dataset containing measurements and characteristics from breast tumors coming out of the State of Wisconsin, which were classified as malignant or benign.

There are 33 columns, with 569 total rows containing measurements of tumors such as radius, texture, compactness, etc. Our target variable is Diagnosis, which was a categorical variable labeled as B-benign or M-malignant. There were 357 tumors classified as benign, and 212 classified as malignant.


## Modeling and Evaluation

### Data Cleaning

To begin, I removed the "id" and "Unnamed: 32" columns, as they were not needed for the purposes of this model. Since Diagnosis was a categorical variable, I mapped malignant tumors to a value of 1 and benign tumors to a value of 0 so that we are able to work with the model. I checked for null values, but there were none.

Multicollinearity is a problem as it undermines the significance of independent variables. I had a suspicion that it might be present within the variables I had, so I did some additional mapping to see if we needed to exclude any variables from the model. I ended up exluding variables that presented with colinearity. Some of those included certain "mean" columns, the "wosrt columns" and any convavity related variables. I left one variable of each type, and just removed all the variables with colinearity. After doing that cleaning, I ended up with 13 out of the 33 original columns.

### Additional Preprocessing

I split the target variable from the rest of the variables, then split each set into training and testing sets.

Scaling features can improve the optimization process by making the flow of gradient descent smoother and helping algorithms reach the minimum of the cost function faster. We scale so that the algorithm is not biased towards the features with values higher in magnitude. I played around with the MinMax Scaler, but found that the Standard Scaler helped the model perform more accurately.

### Baseline Model

I ran a baseline logistic regression model to be able to compare to, with no parameter tuning. The model showed that out of 143 results, only 3 were classified as a false negative, which is approximately 2.1%. The recall was 95%, which I was happy to see. The accuracy score was 94%, which was also a good result for our purposes.

### Logistic Regression Model

I then ran a GridSearch on the logistic regression model to try and tune the parameters and get better results. These results ended up being the same as  the baseline model results, so I would choose the baseline model over this model as it is slightly less complicated and yields the same restuls.

### Decision Tree Model

I tried running a decision tree model to see if that would outperform the linear regression model. I performed a series of tests to try and tune the parameters. I looked at optimal tree depth, min-samples-split, minimum sample leafs, and maximum feature size. The decision tree model performed considerably worse than the logistic regression model. The number of false negatives was up 3 times that of the logistic regression model, with recall of 83% and accuracy of 74%.

I then performed a decision tree model with no tuning, which actually performed better than the tuned model. This means I must have not tuned the model correctly, there is more work that could be done there to get a better performing model. Although this model performed better than my first decision tree model, it still did not outperform the logistic regression model I initially performed.

### Random Forest Model

I ran a basic random forest model, which still did not outperform the logistic regression model. 


## Conclusion

In the end, our best performing model was the Logistic Regression model in the beggining with a recall of 95%. Next steps to improve this research would be to create pipelines to streamline the model creations. We would need to do more research on each model and tune the hyperparameters so that we can minimize the amount of false negatives, and improve the overall accuracy.

## Repository

An explanation of the repository organization
Links to the final notebook and presentation
Reproduction instructions (or a link to them)

index.ipynb - main notebook containing cleaning and modeling.

Data - Folder that contains the data source.

PDF - folder that contains pdfs of the project template, presentaiton, any images used, and pdfs of the notebook.
