# Titanic Survival Prediction

This repository contains a Jupyter Notebook (`.ipynb` file) that demonstrates a basic machine learning workflow for predicting survival on the Titanic. It utilizes the well-known Titanic dataset available on platforms like Kaggle.

## Files in this Repository

* `titanic-problem(1).ipynb`: The Jupyter Notebook containing the Python code for data preprocessing, model training, and prediction.
* `train.csv`: The training dataset for the Titanic problem.
* `test.csv`: The test dataset for which survival predictions are made.
* `gender_submission.csv`: A sample submission file provided with the Titanic dataset (though not directly used in the notebook for training).

## Overview of the Notebook

The Jupyter Notebook performs the following steps:

1.  **Imports Libraries:** Imports necessary Python libraries such as NumPy, Pandas, and scikit-learn.
2.  **Loads Data:** Reads the `train.csv`, `test.csv`, and `gender_submission.csv` files into Pandas DataFrames.
3.  **Handles Missing Data:** Fills missing 'Age' values with the mean age from the training set and missing 'Embarked' values with 'S'.
4.  **Drops Unnecessary Features:** Removes columns like 'Cabin', 'Ticket', 'Name', and 'Fare' from both the training and test datasets. These features are deemed less relevant for this basic prediction model.
5.  **Encodes Categorical Features:** Converts the categorical 'Sex' column to numerical (binary) representation (male: 1, female: 0) and the 'Embarked' column to numerical representation (S: 1, C: 2, Q: 3).
6.  **Splits Data for Training and Validation:** Splits the training data into training and validation sets to evaluate the model's performance.
7.  **Trains a Random Forest Classifier:** Initializes and trains a Random Forest Classifier model using the processed training data.
8.  **Evaluates Model Accuracy:** Predicts survival on the validation set and calculates the accuracy of the model. The accuracy is printed to the console.
9.  **Generates Predictions on Test Data:** Uses the trained model to predict survival for the passengers in the `test.csv` file.
10. **Creates Submission File:** Creates a CSV file (`titanic_predictions.csv`) in the specified format ('PassengerId', 'Survived') containing the survival predictions for the test set. **Note:** There might be a small typo in your notebook where the header is set to 'predictions' instead of the expected 'Survived'.

## How to Run the Notebook

You can run this notebook in several ways:

* **Google Colab:** Upload the `.ipynb` file and the `train.csv`, `test.csv`, and `gender_submission.csv` files to your Google Drive and open the notebook in Google Colab.
* **Jupyter Notebook Locally:** Ensure you have Jupyter Notebook installed along with the necessary libraries (NumPy, Pandas, scikit-learn). Place the `.ipynb` file and the CSV files in the same directory and run the notebook.
* **Kaggle Kernels:** If you have a Kaggle account, you can upload the notebook and the data files as a new kernel and run it there.

## Further Improvements

This notebook provides a basic implementation. Potential improvements could include:

* **Feature Engineering:** Creating new features from existing ones (e.g., family size, title from name) that might improve model performance.
* **More Sophisticated Missing Data Imputation:** Using more advanced techniques to handle missing values.
* **Different Machine Learning Models:** Experimenting with other classification algorithms (e.g., Logistic Regression, Support Vector Machines, Gradient Boosting).
* **Hyperparameter Tuning:** Optimizing the hyperparameters of the chosen model using techniques like GridSearchCV or RandomizedSearchCV.
* **Cross-Validation:** Using cross-validation for a more robust evaluation of the model's performance.

## Author

TrevorOlso
