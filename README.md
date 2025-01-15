# Statistics for Data Science: From Zero to Hero

## **Course Overview**
This repository contains a comprehensive course designed to take learners from the basics of statistics to advanced concepts, all tailored for applications in data science. With interactive Jupyter Notebooks, real-world case studies, and modern tooling, this course provides an engaging and practical approach to mastering statistics.

---

## **Table of Contents**

- [Statistics for Data Science: From Zero to Hero](#statistics-for-data-science-from-zero-to-hero)
  - [**Course Overview**](#course-overview)
  - [**Table of Contents**](#table-of-contents)
  - [**Course Index**](#course-index)
    - [**1. Getting Started**](#1-getting-started)
    - [**2. Foundations of Statistics**](#2-foundations-of-statistics)
    - [**3. Probability Essentials**](#3-probability-essentials)
    - [**4. Inferential Statistics**](#4-inferential-statistics)
    - [**5. Regression Analysis**](#5-regression-analysis)
    - [**6. Exploratory Data Analysis (EDA)**](#6-exploratory-data-analysis-eda)
    - [**7. Advanced Topics**](#7-advanced-topics)
    - [**8. Statistics in Machine Learning**](#8-statistics-in-machine-learning)
    - [**9. Practical Applications**](#9-practical-applications)
    - [**10. From Data to Decisions**](#10-from-data-to-decisions)
    - [**11. Final Project**](#11-final-project)
  - [**Features**](#features)
  - [**Folder Structure**](#folder-structure)
  - [**Initial Setup**](#initial-setup)
    - [**On Linux**](#on-linux)
    - [**On Windows**](#on-windows)
  - [**Using This Repo**](#using-this-repo)
    - [**Run with Docker**](#run-with-docker)
    - [**Run Locally with Poetry**](#run-locally-with-poetry)
    - [**Run Tests**](#run-tests)
  - [**Updating a Package**](#updating-a-package)
  - [**Contributing**](#contributing)
  - [**GitHub Actions**](#github-actions)
  - [**Beyond the Course**](#beyond-the-course)


---

## **Course Index**

### **1. Getting Started**
- **Introduction**:
  - What is Statistics? Why is it important for Data Science?
  - Overview of the course structure and objectives.
- **Setting Up the Environment**:
  - Python setup (Jupyter, Pandas, NumPy, Matplotlib, Seaborn, Statsmodels, Scipy).
  - Introduction to statistical tools and datasets.

### **2. Foundations of Statistics**
- **Basic Terminology**:
  - Population vs. Sample
  - Types of Data: Categorical, Numerical, Ordinal
- **Descriptive Statistics**:
  - Central Tendency: Mean, Median, Mode
  - Variability: Range, Variance, Standard Deviation
  - Skewness and Kurtosis
- **Data Visualization**:
  - Graphical Representations: Histograms, Boxplots, Scatterplots, Heatmaps

### **3. Probability Essentials**
- **What is Probability?**
  - Definitions and Basic Rules
  - Conditional Probability
- **Distributions**:
  - Discrete: Binomial, Poisson
  - Continuous: Uniform, Normal
  - The Role of Probability in Data Science
- **Bayes' Theorem**:
  - Intuition and Applications

### **4. Inferential Statistics**
- **Sampling and Sampling Distributions**:
  - Methods: Random Sampling, Stratified Sampling
  - Central Limit Theorem
- **Hypothesis Testing**:
  - Null and Alternative Hypotheses
  - One-tailed vs. Two-tailed Tests
  - Types of Errors (Type I and Type II)
- **Tests for Means and Proportions**:
  - Z-test, T-test, ANOVA
- **Chi-Square Tests**:
  - Goodness of Fit, Independence Tests

### **5. Regression Analysis**
- **Introduction to Regression**:
  - Simple Linear Regression
  - Multiple Linear Regression
- **Model Assumptions and Diagnostics**:
  - Multicollinearity, Homoscedasticity, Independence
- **Regression Metrics**:
  - R-squared, Adjusted R-squared
  - MSE, RMSE, MAE

### **6. Exploratory Data Analysis (EDA)**
- **The EDA Workflow**:
  - Data Cleaning and Preprocessing
  - Identifying Patterns and Trends
- **Visualization for EDA**:
  - Pair Plots, Correlation Heatmaps
- **Outlier Detection and Treatment**:
  - Z-scores, IQR Method

### **7. Advanced Topics**
- **Time Series Analysis**:
  - Components of Time Series (Trend, Seasonality)
  - Stationarity and Differencing
  - ARIMA Models
- **Survival Analysis**:
  - Kaplan-Meier, Hazard Functions
- **Resampling Techniques**:
  - Bootstrapping, Cross-Validation
- **Non-Parametric Statistics**:
  - Mann-Whitney U Test, Kruskal-Wallis Test

### **8. Statistics in Machine Learning**
- **Role of Statistics in ML**:
  - Data Preprocessing, Feature Engineering
- **Evaluating Models with Statistics**:
  - Confusion Matrix, Precision, Recall, F1 Score
  - AUC-ROC Curve, Log-Loss
- **Bias-Variance Tradeoff**

### **9. Practical Applications**
- **Real-World Case Studies**:
  - A/B Testing for Marketing Campaigns
  - Predictive Modeling for Sales Forecasting
  - Customer Segmentation with Clustering
- **Interpreting Outputs**:
  - Using Statsmodels, Scikit-Learn, Pandas

### **10. From Data to Decisions**
- **Storytelling with Data**:
  - Effective Communication of Results
  - Visualization Best Practices
- **Using Statistics for Decision-Making**
- **Ethics in Data Science**

### **11. Final Project**
- **End-to-End Data Science Project**:
  - Define a Problem Statement
  - Perform EDA and Statistical Analysis
  - Build Predictive Models
  - Interpret and Present Results

---

## **Features**
- **Interactive Learning**: Jupyter Notebooks for hands-on practice.
- **Visual Insights**: Graphs and charts for better understanding.
- **Modern Tooling**:
  - Docker for consistent development.
  - Poetry for dependency management.
  - Pre-commit hooks for code quality.
  - GitHub Actions for automation.
- **Real-World Applications**: Practical use cases and projects.

---

## **Folder Structure**

```plaintext
.
├── LICENSE                  # License file for the project
├── README.md                # Main documentation for the repository
├── book                     # Jupyter Book content
│   ├── _build               # Built files for the Jupyter Book
│   ├── _config.yml          # Global configuration
│   ├── _toc.yml             # Table of contents
│   └── ... (source content)
├── notebooks                # Interactive notebooks
├── poetry.lock              # Poetry lock file
├── pyproject.toml           # Poetry configuration
└── tests                    # Unit tests for the project
```

---

## **Initial Setup**

### **On Linux**
1. Install Python and Poetry.
2. Clone this repository.
3. Run `poetry install` to install dependencies.

### **On Windows**
1. Use pyenv-win for Python installation.
2. Install Poetry and clone this repository.
3. Run `poetry install` to install dependencies.

---

## **Using This Repo**

### **Run with Docker**
1. Build the Docker image:
   ```bash
   docker build -t stats-ds-book -f dockerfiles/Dockerfile .
   ```
2. Run the container:
   ```bash
   docker run -it -p 8888:8888 -p 8000:8000 -v $(pwd):/app stats-ds-book
   ```

### **Run Locally with Poetry**
1. Activate the Poetry environment:
   ```bash
   poetry shell
   ```
2. Run Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

### **Run Tests**
Run all unit tests with:
```bash
pytest
```

---

## **Updating a Package**
1. Add or update a dependency:
   ```bash
   poetry add <package-name>
   ```
2. Rebuild the Docker image if necessary:
   ```bash
   docker build -t stats-ds-book -f dockerfiles/Dockerfile .
   ```

---

## **Contributing**
1. Fork this repository.
2. Clone your fork and create a feature branch.
3. Make your changes and commit with clear messages.
4. Push your branch and open a Pull Request.

---

## **GitHub Actions**
This repository uses GitHub Actions for:
- **Linting**: Ensure code quality with pre-commit hooks.
- **Testing**: Run all unit tests automatically.
- **Book Deployment**: Deploy the Jupyter Book to GitHub Pages.

---

## **Beyond the Course**
- **Resources for Further Learning**:
  - Recommended Books, Online Courses, and Tutorials.
- **Practice Platforms**:
  - Kaggle, DataCamp, Analytics Vidhya.
- **Staying Updated**:
  - Communities, Blogs, and Research Papers.
