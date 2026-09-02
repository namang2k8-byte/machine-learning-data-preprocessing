# Machine Learning Data Preprocessing Using Python

## Project Overview
This project demonstrates a basic Machine Learning data-preprocessing workflow using Python, Pandas and NumPy. The sample dataset represents student performance and intentionally includes missing values and a duplicate record.

## Objectives
- Load and inspect a sample dataset using Pandas.
- Identify missing values and duplicate records.
- Handle missing numerical and categorical values.
- Select useful features and remove an identifier column.
- Encode categorical variables using one-hot encoding.
- Normalize numerical features using Min-Max normalization.
- Perform basic exploratory data analysis (EDA).
- Produce a clean modelling-ready dataset.

## Dataset
The dataset contains student demographic information, study behaviour, attendance, internet access and final score.

### Files
- `data/student_performance.csv` — raw dataset.
- `data/cleaned_student_performance.csv` — final preprocessed dataset.
- `data_preprocessing.ipynb` — complete Python/Jupyter workflow.
- `Machine_Learning_Python_Preprocessing_Report(2).docx` — project report.
- `requirements.txt` — required Python packages.

## Preprocessing Steps

### 1. Data Loading
The CSV file is loaded into a Pandas DataFrame using `pd.read_csv()`.

### 2. Initial Inspection
The project checks dataset shape, data types, missing values and descriptive statistics.

### 3. Duplicate Removal
The repeated record is removed with `drop_duplicates()`.

### 4. Missing-Value Handling
- `Age` — median
- `Study_Hours` — median
- `Attendance` — median
- `Gender` — mode

### 5. Feature Selection
`Student_ID` is removed because it is an identifier. `City` is excluded from the modelling-ready example. The selected features are:
`Age`, `Gender`, `Study_Hours`, `Attendance`, `Internet_Access`, and `Final_Score`.

### 6. Categorical Encoding
`Gender` and `Internet_Access` are converted to binary numerical columns using one-hot encoding.

### 7. Normalization
Min-Max normalization scales `Age`, `Study_Hours`, and `Attendance` to the 0–1 range.

### 8. Exploratory Data Analysis
Descriptive statistics and correlations are calculated. The sample indicates positive relationships between study hours, attendance and final score, but the dataset is small and these observations are not definitive.

## How to Run

1. Install Python 3.
2. Install the packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `data_preprocessing.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells from top to bottom.

## Conclusion
The project demonstrates a complete basic data-preprocessing workflow: inspection, duplicate removal, missing-value imputation, feature selection, categorical encoding, normalization and EDA. The final CSV is prepared for use as input to a machine-learning model.
