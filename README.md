# Simple Linear Regression Project

## 📌 Project Overview

This project demonstrates the use of **Simple Linear Regression** to model the relationship between a company's **radio promotion budget** and **sales revenue**. The analysis aims to provide insights into how radio marketing investments impact sales performance.

## 📊 Dataset

- The dataset includes marketing campaign data for TV, radio, and social media advertisements, along with the corresponding sales revenue.
- The primary focus of this study is on the **Radio promotion budget** and **Sales revenue**.
- The dataset used is fictional and was designed for educational purposes.
- 📂 **Download the dataset**: [marketing_sales_data.csv](https://drive.google.com/file/d/1BWQfmdeW83BXIgXCDQHPxPLczmcv55Fs/view?usp=sharing)

## 🏗️ Project Structure

```
├── Simple_Linear_Regression.ipynb  # Jupyter Notebook with cleaned code and analysis
├── Run simple linear regression.pdf  # Original project reference (optional)
├── marketing_sales_data.csv  # Dataset (Ensure it is uploaded in the repo)
└── README.md  # Project documentation
```

## 📝 Steps in Analysis

1. **Data Import & Cleaning**

   - **Loading Data:** Use `pandas.read_csv()` to load the dataset into a DataFrame.
   - **Handling Missing Values:** Use `.isna().sum()` to check for missing values and `.dropna()` to remove them.

2. **Exploratory Data Analysis (EDA)**

   - **Summary Statistics:** Use `data.describe()` to get an overview of numerical features.
   - **Pairwise Relationships:** Use `seaborn.pairplot(data)` to visualize variable relationships.

3. **Model Building**

   - **Feature Selection:** Extract relevant columns using `data[['Radio', 'Sales']]`.
   - **OLS Regression:** Use `statsmodels` to implement Ordinary Least Squares (OLS) regression.
   - **Formula Definition:** Use `ols_formula = 'Sales ~ Radio'` to define the regression equation.

4. **Model Evaluation**

   - **Regression Summary:** Call `model.summary()` to check R-squared, p-values, and coefficients.
   - **Assumption Checks:**
     - **Linearity:** Use `sns.regplot(x='Radio', y='Sales', data=data)`.
     - **Normality:** Plot residuals using `sns.histplot(residuals)` and `sm.qqplot(residuals, line='s')`.
     - **Homoscedasticity:** Scatter residuals against fitted values using `sns.scatterplot(x=fitted_values, y=residuals)`.

## 📌 Key Findings

- The regression equation obtained:\
  **Sales = 8.17 × Radio Budget + 41.53**
- The model shows a **strong positive relationship** between radio advertising and sales revenue.
- The p-value for the radio budget coefficient is **0.000**, indicating statistical significance.
- The R-squared value is **0.757**, meaning **75.7%** of the variation in sales is explained by radio promotion.
- The residuals follow a normal distribution, confirming model validity.

## ⚡ Technologies Used

- **Python** (Pandas, Seaborn, Matplotlib, Statsmodels)
- **Jupyter Notebook** for analysis and visualization

## 🚀 How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/niamat-habibi/simple-linear-regression.git
   ```
2. Navigate to the project folder:
   ```bash
   cd simple-linear-regression
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Simple_Linear_Regression.ipynb
   ```
4. Follow the steps in the notebook to execute the analysis.

## 📢 Contributing

Feel free to contribute by improving the project, adding more visualizations, or testing with different datasets!

## 📌 Author

[Niamat Habibi](https://www.linkedin.com/in/niamatullah-habibi)
