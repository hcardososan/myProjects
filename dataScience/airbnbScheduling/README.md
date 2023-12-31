# Airbnb Scheduling Forecast

Data Science project to forecast Airbnb scheduling. <br> Disclaimer: this project was made with academic and research purposes. The proposed solution does not contain official codes used by the company. Case studies are completely fictional and all references to real-life events are a mere coincidence.

<div align="center">
    <img src="https://www.imobzi.com/papoimobiliario/wp-content/uploads/2017/11/Airbnb.png" width='100%' height='320' alt="image">
</div>

## 1) Business Problem:

> The data and the description were copied from the Kaggle Competition [Airbnb Recruting New User Booking](https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings).

New users on Airbnb can book a place to stay in 34,000+ cities across 190+ countries. By accurately predicting where a new user will book their first travel experience, Airbnb can share more personalized content with their community, decrease the average time to proceed to the first booking, and better forecast the demand.

In this project, I aim to predict in which country a new user will make their first booking.

## 2) Business Assumptions:

The strategy to use a machine learning model to predict the country for the new user may improve the scheduling optimization for new locations.

## 3) Solution Strategy:

This project will have a machine learning model which can predict the country that a new user might choose.

Step 1 - Data Description: In this first section, I will start with the data survey and analysis. The missing values will be treated or removed. Finally, an initial data description will be carried out to know the data. Therefore, some calculations of descriptive statistics will be made, such as kurtosis, skewness, media, fashion, median and standard deviation.

Step 2 - Feature Engineering: In this section, a mind map will be created to assist the creation of the hypothesis and the creation of new features. These assumptions will help in exploratory data analysis and may improve the model scores.

Step 3 - Data Filtering: Data filtering is used to remove columns or rows that are not part of the business. For example, columns with customer ID, hash code or rows with age that does not consist of human age.

Step 4 - Exploratory Data Analysis: The exploratory data analysis section consists of univariate analysis, bivariate analysis and multivariate analysis to assist in the understanding of the database. The hypothesis created in Step 2 will be tested in the bivariate analysis.

Step 5 - Data Preparation: In this section, the data will be prepared for the machine learning modelling. Therefore, they will be transformed to improve the learning of the model. Henceforth, they can be encoded, oversampled, subsampled or rescaled.

Step 6 - Feature Selection: After the data preparation in the previous section, algorithms like PCA will select the best columns to be used for the training of the machine learning model. This reduces the dimensionality of the database and decreases the chances of overfitting.

Step 7 - Machine Learning Modelling: This step aims to train the machine learning algorithms on how they can predict the data. For validation, the model is trained, validated and applied to cross validation to know the learning capacity of the model.

Step 8 - Hyperparameter Fine Tuning: When selected the best model to be applied in the project, it's important to make a fine tuning of the parameters to improve its scores. The same model performance methods apllied in the Step 7 are used.

Step 9 - Conclusions: This is a conclusion stage in which the generation capacity model is tested using unseen data. In addition, some business questions are answered to show the applicability of the model in the business context.

Step 10 - Model Deploy: This is the final step of the project. So, in this step, the Flask API is created and the model and the functions are saved to be implemented in the API.

## 4) Top 3 Data Insights:

* ### 80% or more of the first booking occurred at least one day after the account is created.

    **FALSE**: 80% of the first booking occurred more than one day.

    !["H1 Hypothesis"](/reports/figures/c1_h1.png)

* ### At least 80% of clients speak the English language.

    **TRUE**: The total of customers who speak English is 96.7%.

    !["H6 Hypothesis"](/reports/figures/c1_h6.png)

* ### Most of accesses occurred by using the iOS.

    **TRUE**: Most users accessed the platform using an iOS device. It's about 58.4%.

    !["H10 Hypothesis"](/reports/figures/c1_h10.png)

## 5) Machine Learning Applied:

Here are all the models implemented during the project. The results were gathered from cross validation tests.

### Dummy Model

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.0833 +/- 0.0 | 0.0487 +/- 0.0 | 0.5848 +/- 0.0 | 0.0615 +/- 0.0 | 0.0 +/- 0.0 |

### Logistic Regression

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.0998 +/- 0.0065 | 0.0239 +/- 0.0327 | 0.0078 +/- 0.001 | 0.0106 +/- 0.0006 | 0.0006 +/- 0.0026 |

### Random Forest

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.166 +/- 0.0007 | 0.1643 +/- 0.0022 | 0.8511 +/- 0.0017 | 0.16 +/- 0.0012 | 0.7281 +/- 0.0027 |

### Extra Trees

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.1659 +/- 0.0013 | 0.1656 +/- 0.0025 | 0.829 +/- 0.002 | 0.1641 +/- 0.0017 | 0.6928 +/- 0.0032 |

### CatBoost

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.1748 +/- 0.004 | 0.1735 +/- 0.0029 | 0.6073 +/- 0.0031 | 0.1212 +/- 0.0025 | 0.395 +/- 0.0036 |

## 6) Machine Learning Performance:

The chosen model was **CatBoost**. Below, there's a table with the capacity of the model to learn.

| Accuracy | Precision | Recall | F1 | Kappa |
|:---:|:---:|:---:|:---:|:---:|
| 0.1748 +/- 0.004 | 0.1735 +/- 0.0029 | 0.6073 +/- 0.0031 | 0.1212 +/- 0.0025 | 0.395 +/- 0.0036 |

## 7) Business Results:

The result shows that the accuracy of the model is very low.
Furthermore, the valid results are very different from the cross validation results. It shows that it can predict only about 20% of the locations where the user will decide to book, and the model may be overfitted.

## 8) Conclusions:

The model doesn't have a good accuracy even using Principal Component Analysis (PCA) to improve the features, staying being below 20%.

## 9) Lessons Learned:

* The importance of the data.

* How to fix the problem of the imbalanced data.

* Improving the the features using PCA.