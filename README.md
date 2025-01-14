Project Overview
This project focuses on predicting Covid-19 mortality rates in India using machine learning models. The primary goal is to develop an accurate predictive model to forecast pandemic deaths, employing extensive data preprocessing, feature engineering, and model optimization techniques.

Data Preprocessing
Understanding the data was crucial for determining the necessary preprocessing steps before applying any machine learning algorithm. The key preprocessing steps include:
Date and Time Conversion: We converted the date and time to integer type to facilitate correlation analysis between the columns and model training.
Label Encoding: The 'State/Union' column contained string values incompatible with the model’s requirements. We utilized Label Encoder to assign unique integer values to all 39 states.
Handling Missing Values: Columns containing numerous '-' values were replaced with 'NaN' values. We then filled the missing values with the median.
Correlation Analysis: We plotted the correlation matrix to identify relationships between each column. Columns such as Sno, Time, ConfirmedIndian, and ConfirmedForeignNational had minimal significance with respect to the death column and were dropped.
Standard Scaling: We applied Standard Scaler to normalize all integer values within a common scale without altering the underlying distribution.

Model Development and Optimization
Decision Tree Algorithm: We utilized the Decision Tree algorithm, which yielded high accuracy and minimized loss. Hyperparameter tuning was conducted using RandomizedCV, reducing the error significantly.
Model Stacking: We employed model stacking using the Decision Tree Regressor and Gradient Boost Regressor. This approach resulted in the highest accuracy of 99.8% and minimized loss to 2900.

Consistency in Data Preprocessing
To ensure consistency between the training and test datasets, we preprocessed the test data similarly to the training data. This involved converting dates and times to integers and removing columns with minimal correlation. We also identified and replaced values in the 'State/Union Territory' column in the test data that were absent in the training data.
