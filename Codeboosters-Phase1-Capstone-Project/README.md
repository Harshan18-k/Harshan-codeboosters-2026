# Student Performance Analysis and Big Data Processing

This notebook demonstrates a comprehensive workflow for analyzing student performance data using traditional data science tools (Pandas, SQLite, Matplotlib, Scikit-learn) and also explores big data processing with PySpark for sales data.

## Table of Contents
1.  [Data Loading and SQLite Integration](#data-loading-and-sqlite-integration)
2.  [SQL Queries for Data Exploration](#sql-queries-for-data-exploration)
3.  [Data Visualization with Matplotlib](#data-visualization-with-matplotlib)
4.  [Machine Learning Models for Programming Score Prediction](#machine-learning-models-for-programming-score-prediction)
5.  [PySpark for Big Data Sales Analysis](#pyspark-for-big-data-sales-analysis)

---

### 1. Data Loading and SQLite Integration

This section focuses on loading student performance data from a CSV file into a Pandas DataFrame and then integrating it with a SQLite database for efficient querying. It covers:
-   Loading data using `pandas.read_csv`.
-   Connecting to an in-memory SQLite database.
-   Writing the DataFrame to a SQLite table.
-   Basic data inspection and schema printing.

### 2. SQL Queries for Data Exploration

Various SQL queries are executed against the `internship.db` SQLite database to perform data exploration and aggregation. Examples include:
-   Selecting specific columns and filtering rows.
-   Ordering results and limiting output.
-   Grouping data by department and gender to calculate average scores and attendance.
-   Using `HAVING` clause for filtered aggregations.

### 3. Data Visualization with Matplotlib

This section uses Matplotlib to create various charts and visualizations to understand the student performance data better. Visualizations include:
-   Bar charts to compare average math scores, attendance across departments and genders.
-   Horizontal bar chart for top-performing students.
-   Pie chart for student distribution by department.
-   Scatter plot to show the relationship between math score and programming score.

### 4. Machine Learning Models for Programming Score Prediction

This part of the notebook builds and evaluates machine learning models to predict student programming scores. It covers:
-   Data preprocessing: Label Encoding for categorical features (gender, department, semester).
-   Feature selection (`math_score`, `science_score`, `attendance_percentage`, `gender`, `department`).
-   Splitting data into training and testing sets (`train_test_split`).
-   Feature scaling using `StandardScaler`.
-   Training and evaluating a Linear Regression model.
-   Training and evaluating a Decision Tree Regressor model.
-   Reporting metrics such as MAE, MSE, R2, and RMSE.

### 5. PySpark for Big Data Sales Analysis

This section shifts focus to big data processing using Apache Spark (via PySpark) to handle a large sales dataset. It includes:
-   Installation of PySpark.
-   Initialization of a SparkSession.
-   Loading a large sales CSV file into a Spark DataFrame.
-   Inspecting the schema and basic statistics of the Spark DataFrame.
-   Converting the CSV data to Parquet format for optimized storage and reading.
-   Comparing the size reduction achieved by using Parquet over CSV.

## Data Sources
-   `student_performance.csv`: Contains individual student performance metrics.
-   `large_sales_data.csv`: A large dataset simulating sales transactions for big data processing demonstration.

## Key Libraries Used
-   **pandas**: Data manipulation and analysis.
-   **sqlite3**: Database interaction.
-   **matplotlib**: Data visualization.
-   **scikit-learn**: Machine learning model building and evaluation.
    -   `LabelEncoder`, `StandardScaler`
    -   `LinearRegression`, `DecisionTreeRegressor`
    -   `train_test_split`, `mean_absolute_error`, `mean_squared_error`, `r2_score`
-   **pyspark**: Big data processing and analysis.

## How to Run
1.  Ensure all necessary files (`student_performance.csv`, `large_sales_data.csv`) are accessible in the specified paths (e.g., Google Drive).
2.  Run all cells sequentially. Some cells require previous cells to be executed to define variables or set up the environment.
3.  Observe the outputs, visualizations, and model performance metrics.

---

This notebook serves as a practical demonstration of various data science and big data techniques, from data wrangling and visualization to predictive modeling and large-scale data handling.
