# Vehicle Mileage Prediction using Machine Learning

## Project Overview

This project focuses on analyzing vehicle performance data and developing a Machine Learning model to predict vehicle mileage (kilometers per liter).

Using Python, statistical analysis and Scikit-learn, I explored the relationship between vehicle specifications and fuel efficiency, performed feature analysis, and trained a Multiple Linear Regression model.

The project covers the complete workflow, from data exploration and preprocessing to model development, evaluation and making predictions for new vehicles.

## Project Objectives

- Understand the factors influencing vehicle mileage.
- Perform exploratory data analysis (EDA).
- Identify relationships between vehicle specifications and mileage.
- Apply statistical analysis and hypothesis testing.
- Build a Multiple Linear Regression model.
- Evaluate predictions using R² Score.
- Develop a function for predicting mileage of new vehicles.

## Dataset Information

- **Dataset:** Vehicle Performance
- **Records:** 398
- **Columns:** 9
- **Target Variable:** Kilometer_per_liter
- **File Format:** CSV

### Dataset Features

| Feature | Description |
|---|---|
| origin | Vehicle origin category |
| cylinders | Number of engine cylinders |
| displacement | Engine displacement |
| horsepower | Engine horsepower |
| weight | Vehicle weight |
| acceleration | Vehicle acceleration |
| year | Manufacturing year |
| name | Vehicle name |
| Kilometer_per_liter | Vehicle mileage (target) |

## Tools & Technologies

| Technology | Purpose |
|---|---|
| Python | Programming |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| SciPy | Statistical testing |
| Statsmodels | ANOVA and statistical modeling |
| Scikit-learn | Machine Learning |
| Jupyter Notebook | Development environment |

## Project Workflow

### 1. Data Exploration

Performed initial dataset inspection using:

- `head()`
- `shape`
- `describe()`
- `info()`
- `dtypes`
- `isnull().sum()`
- `duplicated()`
- `unique()`

Identified the dataset structure, feature types and data quality issues.

### 2. Data Cleaning & Preprocessing

- Identified missing horsepower values represented by `?`.
- Replaced `?` with NaN.
- Converted horsepower from object to numerical format.
- Imputed missing horsepower values using the median.
- Removed the vehicle name column from model features.
- Separated independent variables and the target variable.

### 3. Exploratory Data Analysis

Used Seaborn and Matplotlib to understand feature distributions and relationships.

Visualizations included:

- Distribution plots.
- Boxplots.
- Count plots.
- Scatter plots.
- Feature-wise comparison charts.
- Correlation analysis.

### 4. Statistical Analysis

Applied statistical methods to understand relationships between vehicle specifications and mileage.

Techniques explored:

- Correlation analysis.
- ANOVA testing.
- Null and alternative hypotheses.
- F-statistic and p-value interpretation.

### 5. Feature Analysis

Analyzed correlations between important features and vehicle mileage.

| Feature | Correlation with Mileage |
|---|---:|
| Weight | -0.832 |
| Displacement | -0.804 |
| Horsepower | -0.778 |
| Year | +0.579 |
| Acceleration | +0.420 |

Key observation:

Vehicle weight, displacement and horsepower showed strong negative correlations with mileage, while manufacturing year showed a positive correlation.

### 6. Machine Learning Model Development

Implemented Multiple Linear Regression using Scikit-learn.

**Model:** Linear Regression

**Target Variable:** Kilometer_per_liter

**Independent Variables:**
- Origin
- Cylinders
- Displacement
- Horsepower
- Weight
- Acceleration
- Year

**Train-Test Split:**
- Training: 80%
- Testing: 20%
- Random State: 0

### 7. Model Evaluation

Evaluated the model using the R² Score.

| Evaluation | R² Score |
|---|---:|
| Training | 0.8189 |
| Testing | 0.8195 |

The model explains approximately 81.95% of the variation in mileage on the test dataset.

The similar training and testing scores indicate consistent performance on these two subsets.

### 8. Actual vs Predicted Comparison

Created a DataFrame containing actual and predicted mileage values for the 80 test observations.

Used Matplotlib to plot actual and predicted values and visually examine the model's predictions.

### 9. Custom Mileage Prediction Function

An additional feature of this project is a custom Python function named `predict_mpg()`.

The function accepts vehicle specifications as user input:

- Origin
- Number of cylinders
- Displacement
- Horsepower
- Weight
- Acceleration
- Manufacturing year

It creates a DataFrame from the entered specifications and passes it to the trained model to predict vehicle mileage.

**Example Prediction:**

For the following vehicle specifications:

- Origin: 1
- Cylinders: 5
- Displacement: 250
- Horsepower: 100
- Weight: 2600
- Acceleration: 15
- Year: 1980

Predicted mileage: **12.43 km/l**

## Key Learnings

Through this project, I gained practical experience in:

- Data cleaning and preprocessing.
- Handling missing values and incorrect data types.
- Exploratory Data Analysis.
- Correlation and statistical interpretation.
- ANOVA and hypothesis testing.
- Feature selection and target variable separation.
- Train-test splitting.
- Multiple Linear Regression.
- Model evaluation using R² Score.
- Comparing actual and predicted values.
- Building custom prediction functions.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-link>
```

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Load the Dataset

```python
import pandas as pd

data = pd.read_csv("vehicle_performance.csv")
```

### 5. Execute the Notebook

Run the notebook cells sequentially to perform data exploration, preprocessing, statistical analysis, model training and mileage prediction.

*This project represents my progress from exploratory data analysis towards practical Machine Learning implementation, with a focus on understanding how vehicle specifications influence fuel efficiency and using those relationships to make predictions.*
