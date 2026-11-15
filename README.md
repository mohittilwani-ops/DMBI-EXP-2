DMBI Experiment 2 – Bank Customer Churn System
Experiment Title
Bank Customer Churn System: Data Preprocessing Using Python
Aim
To perform data preprocessing on the Bank Customer Churn System dataset by handling missing values, removing duplicate records, encoding categorical data, and scaling numerical features.
Objectives
- Load the Bank Customer Churn dataset using Python.
- Identify and handle missing values.
- Identify and remove duplicate records.
- Encode categorical data into numerical form.
- Standardize numerical features.
- Prepare clean data for further analysis and machine learning.
Dataset
- Dataset name: Bank Customer Churn System Dataset
- Expected CSV filename: Churn_Modelling.csv
- Target column: Exited (1 = customer left the bank, 0 = customer stayed)
The dataset includes fields such as CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, and Exited. It may also include identifier columns such as RowNumber, CustomerId, and Surname.
Software and Libraries
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
Files
- bank_customer_churn_preprocessing.py – Python program for preprocessing.
- Churn_Modelling.csv – Input dataset. Keep this file in the same folder as the Python script.
- bank_customer_churn_preprocessed.csv – Output generated after successful execution.
- DMBI_EXP2_Bank_Customer_Churn_System.docx – Experiment write-up.
Preprocessing Steps
1. Load dataset: Read the CSV file into a Pandas DataFrame.
2. Inspect data: Display the first records, dataset shape, information, and missing-value counts.
3. Handle missing values: Replace missing numerical values with the column mean and missing categorical values with the mode.
4. Remove duplicates: Identify and remove repeated rows.
5. Remove identifiers: Drop RowNumber, CustomerId, and Surname from the model input.
6. Separate features and target: Store input features in X and the target Exited in y.
7. Encode categories: Apply One-Hot Encoding to Geography and Gender.
8. Scale features: Apply StandardScaler to numerical input features. The target column Exited is kept separate and is not scaled.
9. Save output: Write the processed data to bank_customer_churn_preprocessed.csv.
How to Run
1. Install required libraries
Open a terminal in the project folder and run:
pip install pandas numpy scikit-learn
2. Place the dataset
Keep Churn_Modelling.csv in the same folder as bank_customer_churn_preprocessing.py.
3. Execute the program
python bank_customer_churn_preprocessing.py
4. Check the output
The program prints the processed dataset preview, final shape, missing-value count, and duplicate count. It also creates:

bank_customer_churn_preprocessed.csv
Expected Verification
After preprocessing, check that:
- Missing-value count is 0 if the input data can be filled using the selected mean/mode strategy.
- Duplicate-record count is 0 after duplicate removal.
- Geography and Gender have been converted into numerical indicator columns.
- Numerical input features have been standardized.
- Exited remains the target column.
Exact output dimensions depend on the CSV file supplied and the records it contains.
Result
The Bank Customer Churn System dataset is preprocessed using Python by handling missing values, removing duplicate records, encoding categorical data, and standardizing numerical features. The resulting dataset is prepared for further analysis and machine learning.
Note
The program follows the preprocessing workflow described in the experiment document. StandardScaler is fitted on the complete dataset here for a basic practical demonstration. In a real machine-learning evaluation, fit preprocessing steps only on the training data and apply the fitted transformations to validation/test data to avoid data leakage.
