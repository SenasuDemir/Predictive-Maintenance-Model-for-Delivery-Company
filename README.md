# Build a Predictive Maintenance Model for a Delivery Company

## Project Overview

### Objective
The primary goal of this project is to predict device failures (`failure` column) using a **classification** model. The dataset contains operational data of various devices, with multiple attributes providing insight into each device's status and performance metrics. The challenge lies in handling the **class imbalance** in the `failure` column and identifying patterns that are indicative of failures.

To address the class imbalance issue, we used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset before training the model. This technique helps in generating synthetic samples for the minority class to improve model performance.

By developing a robust predictive model, we aim to improve the accuracy of failure predictions, which can be beneficial for proactive maintenance strategies and reducing downtime for devices.

### Dataset Description
The dataset contains the following columns:

| **Column**     | **Description**                                                                                     |
|-----------------|-----------------------------------------------------------------------------------------------------|
| `date`         | The date when the data was recorded, helping track device performance over time.                    |
| `device`       | A unique identifier for each device to distinguish data from different devices.                     |
| `failure`      | The target variable indicating if a failure occurred. **0** = No failure, **1** = Failure.          |
| `attribute1`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute2`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute3`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute4`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute5`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute6`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute7`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute8`   | A numerical attribute representing a device-specific metric.                                         |
| `attribute9`   | A numerical attribute representing a device-specific metric.                                         |

### Objective of the Model
To predict whether a device will fail (**failure = 1**) or not fail (**failure = 0**) based on the various attributes provided in the dataset.

## Model Performance and Interpretation

The **Random Forest Classifier** outperforms all other models with an impressive **accuracy of 99.33%**, making it the most reliable model for predicting device failures. Below are the performance scores for various models:

| Model                        | Accuracy   |
|------------------------------|------------|
| Random Forest Classifier      | 0.993327   |
| Decision Tree Classifier      | 0.992262   |
| KNeighbors Classifier         | 0.940992   |
| Gradient Boosting Classifier  | 0.924773   |
| Bernoulli Naive Bayes         | 0.873000   |
| Logistic Regression           | 0.762963   |
| Gaussian Naive Bayes         | 0.627181   |

The **Random Forest Classifier** shows the following metrics:
- **Precision**: High accuracy in identifying both failure (class 1) and non-failure (class 0) instances.
- **Recall**: Effective at capturing all actual failures as well as non-failures.
- **F1-Score**: Balanced performance for both failure and non-failure classes.

The **Random Forest Classifier** consistently demonstrates excellent performance, making it the optimal choice for failure prediction in this dataset.

## Handling Class Imbalance
The dataset was found to be imbalanced, with the majority of devices not failing (**failure = 0**) and a smaller number of devices experiencing failures (**failure = 1**). To address this imbalance, we applied **SMOTE (Synthetic Minority Over-sampling Technique)**, which generates synthetic data points for the minority class (failure) to balance the dataset. This helps improve the performance of the model, especially in predicting the minority class (failures).

## Conclusion
This project showcases the effectiveness of using **classification** models, particularly **Random Forest Classifier**, for predicting device failures based on operational data. By utilizing **SMOTE** for balancing the dataset, we achieved high performance and reliable predictions. The high accuracy and robust performance of the Random Forest model highlight its potential in improving maintenance strategies and preventing device downtimes.
