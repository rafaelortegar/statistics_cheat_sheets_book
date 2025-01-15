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
    - [**4. Statistical Distributions**](#4-statistical-distributions)
    - [**5. Inferential Statistics**](#5-inferential-statistics)
    - [**6. Regression Analysis**](#6-regression-analysis)
    - [**7. Exploratory Data Analysis (EDA)**](#7-exploratory-data-analysis-eda)
    - [**8. Advanced Topics**](#8-advanced-topics)
    - [**9. Most Common Problems in Data Science**](#9-most-common-problems-in-data-science)
    - [**10. Most Rare Problems in Data Science**](#10-most-rare-problems-in-data-science)
    - [**11. Statistics in Machine Learning**](#11-statistics-in-machine-learning)
    - [**12. Practical Applications**](#12-practical-applications)
    - [**13. From Data to Decisions**](#13-from-data-to-decisions)
    - [**14. Final Project**](#14-final-project)
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
- **Bayes' Theorem**:
  - Intuition and Applications

### **4. Statistical Distributions**
- **Discrete Distributions**:
  - Binomial Distribution: Concepts, Applications, and Examples
  - Poisson Distribution: Modeling Rare Events
  - Geometric and Hypergeometric Distributions
- **Continuous Distributions**:
  - Normal Distribution: Properties, Z-scores, and Applications
  - Uniform, Exponential, Gamma, and Beta Distributions
- **Multivariate Distributions**:
  - Multivariate Normal Distribution, Covariance, and Correlation Matrices
- **Applications**:
  - Simulating Data and Fitting Distributions to Real-World Data

### **5. Inferential Statistics**
- **Sampling and Sampling Distributions**:
  - Methods: Random Sampling, Stratified Sampling
  - Central Limit Theorem
- **Hypothesis Testing**:
  - Null and Alternative Hypotheses
  - Z-tests, T-tests, ANOVA, Chi-Square Tests

### **6. Regression Analysis**
- **Linear Regression**:
  - Simple and Multiple Linear Regression
  - Model Assumptions and Diagnostics
- **Metrics**:
  - R-squared, Adjusted R-squared, RMSE, MAE

### **7. Exploratory Data Analysis (EDA)**
- **Data Cleaning and Visualization**:
  - Pair Plots, Correlation Heatmaps
  - Outlier Detection (Z-scores, IQR)

### **8. Advanced Topics**
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

### **9. Most Common Problems in Data Science**
- **Data Cleaning Challenges**:
  - Handling Missing Values, Outliers, and Duplicates
- **Bias Issues**:
  - Sampling Bias, Data Leakage
- **Scalability**:
  - Optimizing Pipelines for Large Datasets
- **Communication**:
  - Interpreting Results for Stakeholders

### **10. Most Rare Problems in Data Science**
- **Sparse and Rare Data**:
  - Long-Tail Distributions, Multivariate Outliers
- **Unusual Phenomena**:
  - Simpson's Paradox, Extreme Class Imbalances
- **Niche Applications**:
  - Genomics, Astronomy, System Failures

### **11. Statistics in Machine Learning**
- **Role of Statistics in ML**:
  - Data Preprocessing, Feature Engineering
- **Evaluating Models**:
  - Confusion Matrix, Precision, Recall, AUC-ROC

### **12. Practical Applications**
- **Real-World Case Studies**:
  - A/B Testing, Sales Forecasting, Customer Segmentation

### **13. From Data to Decisions**
- **Storytelling and Ethics**:
  - Communication and Ethical Considerations

### **14. Final Project**
- **End-to-End Data Science Project**:
  - Problem Definition, EDA, Statistical Analysis, and Results

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
   docker build -t stats-ds-book -f dockerfiles/Dockerfile_stats_ds_book .
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
