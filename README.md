# Global COVID-19 and Socioeconomic Indicators: An Exploratory and Inferential Analysis

**Python | Data Cleaning | Exploratory Data Analysis | Statistical Inference | Regression Modelling | Data Visualisation**

## 1. Project Overview

This project presents an exploratory and inferential statistical analysis of global COVID-19 statistics alongside selected socioeconomic indicators. Using Python, the analysis examines patterns in the data, compares indicators across countries and continents, investigates relationships between selected numerical variables, and applies simple linear regression to explore potential statistical associations.

The project follows a structured data analysis workflow, beginning with data inspection and preparation, followed by descriptive analysis, visualisation, statistical testing, regression modelling and diagnostic assessment.

The main objective is to demonstrate how statistical and computational techniques can be applied to real-world datasets to extract meaningful information, identify patterns and communicate findings through appropriate visualisations and statistical interpretation.

## 2. Project Objectives

The specific objectives of the analysis are to:

- Inspect and understand the structure, variables and quality of the dataset.
- Identify missing observations, duplicate records and data inconsistencies.
- Clean and prepare the data for subsequent statistical analysis.
- Generate descriptive statistics to summarise the distribution and characteristics of key variables.
- Examine the distribution of selected indicators using graphical and numerical methods.
- Compare COVID-19 and socioeconomic indicators across countries and continents.
- Visualise geographical patterns using interactive country-level maps.
- Investigate relationships between selected numerical variables using correlation analysis.
- Conduct pairwise statistical tests to assess the significance of observed correlations.
- Fit simple linear regression models to examine selected relationships between variables.
- Evaluate regression models using statistical significance, confidence intervals and diagnostic plots.
- Interpret the findings while recognising the limitations of observational data.

## 3. Dataset Description

The analysis uses a global dataset containing COVID-19 statistics and selected socioeconomic indicators at the country level.

The dataset includes variables used to examine differences between countries, describe the distribution of key indicators and investigate relationships between health-related and socioeconomic measures.

**Dataset file:** `covid19_global_statistics_2026_with_imf_gdp.csv`

**Geographical coverage:** Multiple countries across different continents.

**Unit of analysis:** Country-level observations.



## 4. Analytical Workflow and Methodology

The project follows the stages below.

### 4.1 Data Loading and Initial Inspection

The dataset is imported into Python using Pandas. Initial inspection is performed to understand its dimensions, variable names, data types and general structure.

The inspection includes:

- Viewing sample observations.
- Checking the number of rows and columns.
- Examining variable data types.
- Identifying missing values.
- Checking for duplicate records.
- Reviewing the distribution and characteristics of selected variables.

This stage provides an initial assessment of data quality and helps determine the preparation required before analysis.

### 4.2 Data Cleaning and Preparation

Data preparation is undertaken to improve consistency and ensure that variables are suitable for statistical analysis.

The cleaning process includes:

- Standardising column names for easier referencing.
- Converting relevant variables into appropriate numerical formats.
- Identifying and assessing missing observations.
- Checking for duplicate records.
- Removing observations without identifiable country information where necessary.
- Preparing country-level identifiers for geographical visualisation.

The objective is to minimise data inconsistencies while retaining observations that are relevant to the analysis.

### 4.3 Descriptive Statistical Analysis

Descriptive statistics are used to summarise the main characteristics of the numerical variables.

Measures considered include:

- Mean and median.
- Standard deviation.
- Minimum and maximum values.
- Quartiles and interquartile range.
- Skewness and kurtosis.

These measures help describe central tendency, variability, distributional characteristics and potential extreme observations.

### 4.4 Exploratory Data Analysis and Visualisation

Exploratory data analysis is conducted to identify patterns, differences and unusual observations within the dataset.

The visualisation techniques include:

- Histograms for examining variable distributions.
- Country-level comparisons using horizontal bar charts.
- Continent-level summaries for comparing geographical groups.
- Interactive choropleth maps for displaying country-level geographical patterns.
- Correlation heatmaps for exploring relationships between numerical variables.
- Pairwise plots and other graphical summaries where appropriate.

These visualisations support the interpretation of numerical results and make geographical and statistical patterns easier to communicate.

### 4.5 Correlation Analysis and Statistical Testing

Pearson correlation analysis is used to examine the direction and strength of linear relationships between selected numerical variables.

The analysis also includes pairwise correlation significance tests to assess whether the observed relationships provide sufficient statistical evidence against the null hypothesis of zero population correlation.

To account for multiple hypothesis testing, the Benjamini–Hochberg procedure is applied to adjust the resulting p-values and control the false discovery rate.

Correlation results are interpreted as measures of statistical association rather than evidence of causation.

### 4.6 Simple Linear Regression Modelling

Simple Ordinary Least Squares (OLS) regression models are fitted to investigate selected relationships between individual explanatory variables and response variables.

The models are assessed using:

- Regression coefficients and their direction.
- Statistical significance of the estimated slopes.
- Confidence intervals.
- Coefficient of determination (R-squared).
- Root Mean Squared Error (RMSE).
- Overall model summaries.

Several individual regression models are compared using their in-sample R-squared values and other reported performance measures.

The comparison provides an indication of how well each explanatory variable accounts for variation in its corresponding response variable within the observed dataset.

Importantly, the models are exploratory and do not establish causal relationships.

### 4.7 Regression Diagnostics

Diagnostic plots are used to assess important aspects of the fitted regression models.

The analysis includes:

- **Residual-versus-fitted plots:** Used to examine potential systematic patterns, non-linearity and changes in residual variability.
- **Normal Q-Q plots:** Used to assess whether regression residuals approximately follow a normal distribution.

These diagnostic checks help identify potential departures from regression assumptions and inform the interpretation of the fitted models.

## 5. Tools and Technologies

The project was implemented using Python and the following libraries:

| Tool / Library | Application |
|---|---|
| Python | Main programming language |
| Pandas | Data manipulation, cleaning and preparation |
| NumPy | Numerical computations |
| Matplotlib | Statistical and exploratory visualisations |
| Seaborn | Statistical graphics and correlation visualisation |
| SciPy | Statistical tests and computations |
| Statsmodels | Correlation testing and OLS regression modelling |
| Plotly Express | Interactive geographical visualisations |
| Pycountry | Country identification and geographical mapping support |
| IPython | Notebook display and presentation |

## 6. Repository Structure

The repository is organised to make the analysis accessible and reproducible.

```text
covid19-socioeconomic-analysis/
│
├── README.md
│
├── notebooks/
│   └── global_covid19_analysis.ipynb
│
├── outputs/
│   └── figures/
│
└── requirements.txt
```

**Repository contents:**

- `README.md` – Project overview, methodology, tools and reproduction instructions.
- `notebooks/` – Jupyter Notebook containing the analysis, Python code, outputs and interpretations.
- `outputs/figures/` – Selected visualisations exported from the notebook, where available.
- `requirements.txt` – Python dependencies required to reproduce the analysis.

*The structure above is the recommended repository structure. Ensure the folders and files are uploaded with the same names before publishing the repository.*

## 7. Reproducing the Analysis

To reproduce the analysis, follow these steps:

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/covid19-socioeconomic-analysis.git
```

### Step 2: Navigate to the project directory

```bash
cd covid19-socioeconomic-analysis
```

### Step 3: Create a virtual environment (recommended)

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

**macOS/Linux:**
```bash
source venv/bin/activate
```

### Step 4: Install the required libraries

```bash
pip install -r requirements.txt
```

### Step 5: Obtain the dataset

Download the dataset from its original source and place it in the project directory or update the notebook's `DATA_PATH` variable to point to its location.

### Step 6: Run the notebook

Open Jupyter Notebook or JupyterLab:

```bash
jupyter notebook
```

Navigate to:

`notebooks/global_covid19_analysis.ipynb`

Run the notebook cells sequentially to reproduce the analysis.

## 8. Key Analytical Outputs

The notebook produces several analytical outputs, including:

- Data quality and missing-value summaries.
- Descriptive statistics for selected numerical variables.
- Distribution plots for key indicators.
- Country-level and continent-level comparisons.
- Interactive geographical visualisations.
- Correlation matrices and statistical significance tests.
- Simple linear regression results.
- Regression diagnostic plots.
- Comparative summaries of the fitted regression models.

Together, these outputs demonstrate the application of statistical programming, exploratory analysis, inferential techniques and data visualisation to a multidimensional dataset.

## 9. Limitations and Considerations

The findings should be interpreted in light of the following limitations:

1. **Data quality and reporting differences:** Country-level COVID-19 statistics may be affected by differences in reporting practices, testing capacity, definitions and data collection procedures.

2. **Missing observations:** Missing or incomplete records may affect the comparability of some indicators across countries.

3. **Observational nature of the data:** The analysis identifies statistical patterns and associations but does not establish causal relationships.

4. **Linear modelling assumptions:** Simple linear regression may not adequately capture complex or non-linear relationships between variables.

5. **Model scope:** The regression models examine selected variables individually and do not account for all possible confounding factors or interactions.

6. **Temporal limitations:** The analysis is based on the available dataset and does not constitute a longitudinal or time-series forecasting study.

These limitations are important when interpreting the statistical results and considering the extent to which the findings can be generalised.

## 10. Skills Demonstrated

This project demonstrates practical experience in:

- Python programming for statistical analysis.
- Data cleaning, transformation and quality assessment.
- Exploratory data analysis.
- Descriptive and inferential statistics.
- Correlation analysis and multiple-testing adjustment.
- Ordinary Least Squares regression modelling.
- Regression diagnostics and model evaluation.
- Geographical data visualisation.
- Interactive data presentation.
- Statistical interpretation and communication of findings.
- Organising analytical workflows for reproducibility.

## 11. Future Improvements

Possible extensions to the project include:

- Incorporating additional socioeconomic and public health indicators.
- Investigating multivariable regression models to account for multiple explanatory variables simultaneously.
- Exploring non-linear relationships and potential interaction effects.
- Applying more advanced statistical and machine-learning approaches where justified by the research question.
- Improving reproducibility through automated data validation and more comprehensive documentation.
- Developing an interactive dashboard to communicate selected findings.

These extensions would build on the existing exploratory and inferential analysis without changing the scope of the current project.

## 12. Author

**Valentine Mwangi**

BSc Statistics | MSc Applied Statistics (Ongoing)

Jomo Kenyatta University of Agriculture and Technology (JKUAT)

**Areas of interest:** Statistical Modelling, Data Science, Quantitative Research, Applied Statistics and Data Analytics.

- **LinkedIn:** https://www.linkedin.com/in/valentine-njeri-966444256
- **GitHub:** https://github.com/ValentineMwangi1

---

*This project was completed as part of practical statistical programming and data analysis work. The code, visualisations and interpretations are presented for learning, demonstration and reproducibility purposes.*
