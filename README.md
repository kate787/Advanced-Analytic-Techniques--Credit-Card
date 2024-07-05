# Advanced Analytic Techniques: Prediction of Credit Card Approval

## Description

Credit scores are used as a risk control method in the financial industry. Banks use credit scores and personal information submitted by credit card applicants to decide whether to issue a credit card to the applicant or not. 

### Feature Names and Explanations
| Feature Name    | Explanation                                    | Additional Remarks                          |
|-----------------|------------------------------------------------|---------------------------------------------|
| ID              | Randomly allocated client number               |                                             |
| Income          | Annual income                                  |                                             |
| Gender          | Applicant's Gender                             | Male = 0, Female = 1                        |
| Car             | Car Ownership                                  | Yes = 1, No = 0                             |
| Children        | Number of Children                             |                                             |
| Real Estate     | Real Estate Ownership                          | Yes = 1, No = 0                             |
| Days Since Birth| No. of Days                                     | Count backwards from current day (0), -1 means yesterday |
| Days Employed   | No. of Days                                     | Count backwards from current day (0). If positive, it means the person is currently unemployed. |
| Payment Default | Whether a client has overdue credit card payments | Yes = 1, No = 0                            |

## Problems and Questions
### Problem 1 - (50 points)
1. Import the assignment_data.xlsx file from the data folder into a pandas DataFrame named df.
   - Delete duplicate rows from df according to ID.
   - Delete the ID column.
   - How many rows are left in df? (10 points)

2. Reset the index in df using an appropriate function from pandas so that the new index corresponds to the number of rows (make sure to delete the old index).
   - How many positive values of Days Employed are there?
   - Replace the positive values of Days Employed with 0 (zero) in df. (10 points)

3. Create two new variables in df named:
   - Age
   - Years in Employment
   - Delete the original variables Days Since Birth and Days Employed. (5 points)

4. Create a one-dimensional NumPy array named y by exporting the first 5,000 observations of Payment_Default.
   - Create a NumPy array named X by exporting the first 5,000 observations of the following columns: Gender, Car, Real Estate, Children, Income, Age, Years in Employment. (10 points)

5. Use an appropriate scikit-learn library to create the following NumPy arrays: y_train, y_test, X_train, and X_test by splitting the data into 70% training and 30% test datasets.
   - Set random_state to 0 and stratify subsamples so that train and test datasets have roughly equal proportions of the target's class labels. (5 points)

6. Create new variables by using an appropriate scikit-learn library to standardize the features from the training and test datasets to mean zero and variance one. Name the new variables by appending '_scaled' to the original variable names. (10 points)

### Problem 2 - (20 Points)
7. Fit the following two classifiers to the transformed training dataset using scikit-learn libraries:
   - Perceptron (pc) set random_state=1
   - Logistic Regression (lr) set random_state=1
   - When initializing instances of the above classifiers only set the parameters referenced above and nothing else. (20 points)

### Problem 3 - (30 points)
8. Using a method built into each of the two classifiers compute their prediction accuracies on the training data.
   - Store the accuracy values into variables named according to the following pattern: classifier_name_accuracy_train.
   - Print the two accuracy variables along with their brief descriptions. (10 points)

9. Using a method built into each of the above classifiers compute their prediction accuracy for the test dataset.
   - Store the accuracy values into variables named according to the following pattern: classifier_name_accuracy_test.
   - Print the two accuracy variables along with brief descriptions. (10 points)

10. Using nicely formatted text in Markdown comment on the accuracies computed in Questions 8 & 9 making sure you address:
    - training and test set datasets;
    - Perceptron and Logistic Regression models.
    - Are the results as expected, and why or why not? (10 points)

## Authors

Kate Lee
k4t3l33@gmail.com
