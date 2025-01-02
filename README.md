# Data Scientist Salaries Analysis

## Overview

This project analyzes the salaries of data scientists using a dataset from Kaggle. The analysis includes data cleaning, exploratory data analysis (EDA), hypothesis testing, and linear regression modeling to predict salaries based on various factors.

## Dataset

The dataset used in this analysis is from Kaggle: [2023 Data Scientists Salary](https://www.kaggle.com/datasets/henryshan/2023-data-scientists-salary). It contains information about data scientists' salaries, job titles, experience levels, company sizes, and more.

## Project Structure

- `analysis.ipynb`: Jupyter notebook containing the entire analysis, including data cleaning, EDA, hypothesis testing, and linear regression modeling.
- `cleaned_ds_salaries.csv`: Cleaned dataset after data preprocessing.
- `coefficients.csv`: Coefficients of the linear regression model.
- `linear_regression_model.joblib`: Trained linear regression model saved using `joblib`.
- `remote_ratio_job_title.png`: Bar plot showing the distribution of remote work ratios by job title.
- `feature_impact_plot.png`: Bar plot showing the impact of different features on predicted salaries.

## Data Cleaning

### Steps

1. **Removing Columns with Dominant Categories**: Columns with a single dominant category were removed to ensure quality and reliability.
2. **Restricting Dataset to USA and USD**: The dataset was restricted to entries where the `employee_residence` is the USA and the `salary_currency` is USD.
3. **Adjusting Salaries for Cumulative Inflation**: Salaries from previous years were adjusted to 2023 values using the inflation rate in the US.
4. **Converting Numerical Column `remote_ratio` to Categorical**: The `remote_ratio` column was converted into a categorical column with three categories: `In office`, `Hybrid`, and `Remote`.

## Exploratory Data Analysis (EDA)

### Steps

1. **Distribution of Numerical Columns**: Histograms were plotted for each numerical column.
2. **Distribution of Categorical Columns**: Bar charts were plotted for each categorical column.

## Hypothesis Testing

### Hypotheses and Tests

1. **Experience Level vs. Salary**: Mood’s Median Test was used to compare salaries across different experience levels.
2. **Remote Ratio vs. Salary**: Mood’s Median Test was used to test the association between remote work proportion and salary.
3. **Company Size vs. Salary**: Kruskal-Wallis Test was used to compare salaries across different company sizes.
4. **Job Title vs. Remote Ratio**: Chi-square Test of Independence was used to determine the association between job title and remote work ratio.
5. **Job Title vs. Salary**: Kruskal-Wallis Test was used to compare salaries across different job titles.

## Linear Regression Analysis

### Steps

1. **Encoding Categorical Variables**: Categorical variables were encoded for numerical representation.
2. **Splitting Dataset**: The dataset was split into training and testing subsets.
3. **Training Model**: A linear regression model was trained to predict adjusted salaries.
4. **Evaluating Model**: The model's performance was evaluated using Mean Squared Error (MSE) and R-squared metrics.
5. **Visualizing Results**: The impact of different features on predicted salaries was visualized.

### Requirements

- Python 3.12
- Jupyter Notebook
- Pandas
- Matplotlib
- Seaborn
- Scipy
- Scikit-learn
- Joblib
- Scikit-posthocs

### Running the Analysis

1. Clone the repository.
2. Install the required packages. 
`pip install -r requirements.txt`
3. Open `analysis.ipynb` in Jupyter Notebook.
4. Run the notebook cells sequentially to perform the analysis.

## Conclusion

This project provides a comprehensive analysis of data scientists' salaries, including data cleaning, EDA, hypothesis testing, and linear regression modeling. The findings offer insights into the factors affecting salaries and can help in making informed decisions.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.