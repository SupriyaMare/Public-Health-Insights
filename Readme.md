# Public Health Insights: Challenges in Environment

**An Alteryx and Machine Learning Project for Environmental and Healthcare Data Analysis**

## Overview

Public Health Insights explores how environmental pollution indicators and healthcare data can be analyzed together to investigate patterns in public health.

The project combines environmental and healthcare datasets, uses Alteryx Designer for data preparation, creates visualizations to explore regional pollution and medical-condition patterns, and describes a Random Forest Classifier for predicting medical conditions using environmental features.

The goal is to demonstrate how data analytics and machine learning can support public health research and help identify patterns that deserve further investigation.

## Objectives

- Integrate environmental and healthcare datasets for analysis.
- Clean and preprocess data using Alteryx Designer.
- Explore pollution indicators such as SO₂, NO₂, and SPM.
- Visualize pollution patterns across locations.
- Analyze healthcare records by age, blood group, year, and medical condition.
- Develop a Random Forest classification workflow.
- Evaluate the model using accuracy, precision, recall, and F1-score.
- Save the trained model for potential future predictions.

## Dataset Information

The project documentation describes two datasets.

| Dataset | Records | Fields | Format |
|---|---:|---:|---|
| Healthcare | 55,500 | 15 | CSV and PDF sources |
| Environmental | 435,740 | 13 | CSV |

### Healthcare Dataset

The documented features include:

- Age
- Gender
- Blood group
- Medical condition
- Date of admission
- Discharge date

### Environmental Dataset

The documented features include:

- State code
- Sampling date
- State
- Location
- SO₂
- NO₂
- Pollution-related type or category

**Data sources referenced in the project:**

- [Government of India Open Government Data Platform](https://data.gov.in/)
- [World Health Organization Data](https://www.who.int/data)
- [OpenCity](https://opencity.in/)

Refer to the original dataset documentation for the exact source URLs, collection periods, licensing terms, and field definitions.

## Tools and Technologies

- **Alteryx Designer:** Data input, cleansing, selection, filtering, and preparation.
- **Python:** Model development and prediction workflow described in the documentation.
- **Pandas:** Dataset manipulation and merging.
- **Scikit-learn:** Random Forest classification and model evaluation.
- **Joblib:** Saving and loading the trained model.
- **Data visualization:** Charts and geographical maps for exploring environmental and healthcare patterns.

The Python libraries listed above correspond to the documented machine learning workflow. Confirm the actual implementation and library versions before publishing a reproducible environment file.

## Methodology

### 1. Data Collection

Collect environmental and healthcare datasets from public data sources and organize them for analysis.

### 2. Data Preprocessing with Alteryx

The documented Alteryx workflow uses:

- Input Data Tool
- Data Cleansing Tool
- Select Tool
- Filter Tool

These steps are used to clean records, handle missing or null values, remove unwanted whitespace, select relevant fields, and filter unnecessary records.

### 3. Data Integration

The documented machine learning workflow standardizes date formats, identifies common dates, and merges the datasets using the date field.

The merged dataset is then checked for missing values and prepared for modeling.

### 4. Exploratory Data Analysis

The project includes visualizations covering:

- SPM distribution across locations.
- Geographical distribution of SPM levels in India.
- Healthcare patterns involving age, blood groups, and medical conditions.
- Medical-condition counts across years.

### 5. Machine Learning

A Random Forest Classifier is described for classifying medical conditions using environmental features.

The documented workflow includes:

1. Selecting the target variable.
2. Preparing and encoding data.
3. Splitting the dataset into training and testing sets.
4. Standardizing features.
5. Training the Random Forest model.
6. Generating predictions.
7. Evaluating model performance.
8. Saving the trained model.

### 6. Model Evaluation

The project documentation identifies these evaluation metrics:

- **Accuracy:** Overall proportion of correct predictions.
- **Precision:** Proportion of positive predictions that are correct.
- **Recall:** Proportion of actual positive cases correctly identified.
- **F1-score:** Harmonic mean of precision and recall.

Numerical evaluation results should be added here only after verifying the actual model output.

### 7. Model Persistence

The documentation describes saving the trained model as:

`public_health_insights_classifier_model.pkl`

The model can potentially be loaded for predictions on new data that follows the same preprocessing and feature schema.

## Results and Visualizations

The project documentation presents the following findings and visual outputs:

### Environmental Analysis

- An SPM-by-location chart identifies Guwahati, Hyderabad, and Chandigarh among the locations highlighted in the report.
- An India map visualizes SPM levels across locations, with Visakhapatnam marked on the map.

### Healthcare Analysis

- A combination chart explores age-related summaries and medical-condition counts across blood groups.
- A chart displays medical-condition counts across years.

These visualizations describe patterns in the analyzed datasets. They do not independently establish that pollution caused specific medical conditions.

### Model Results

The documentation describes the Random Forest model as performing well, but the numerical scores need to be verified from the actual evaluation output before reporting them.

## Repository Structure

A suggested repository structure is:

```text
public-health-insights/
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── Documentation.pdf
│   └── Presentation.pdf
├── workflow/
│   └── public_health_insights.yxmd
├── results/
│   ├── spm_by_location.png
│   ├── spm_india_map.png
│   ├── healthcare_analysis.png
│   └── model_evaluation.png
├── models/
│   └── public_health_insights_classifier_model.pkl
├── data/
│   └── README.md
└── src/
    └── README.md
```

This is a proposed structure, not a claim that every listed file is already available. Keep only the folders and files you actually add.

## How to Explore the Project

1. Review the documentation and presentation.
2. Open the Alteryx workflow in Alteryx Designer, if the `.yxmd` file is included.
3. Review the exported visualizations in the `results/` folder.
4. Review the model evaluation output, if available.
5. Follow the documented preprocessing and modeling steps to reproduce the analysis when the necessary source data and implementation files are available.

Execution requires the original workflow, compatible software, and the required datasets.

## Limitations

- Findings depend on the quality, completeness, and representativeness of the source datasets.
- Combining datasets by date does not necessarily establish a valid location-level or patient-level relationship.
- The documented results do not provide verified numerical model metrics.
- Healthcare and environmental data may contain inconsistencies, missing values, or differences in collection methods.
- Predictive associations should not be interpreted as proof of causation or used as a substitute for medical advice.

## Future Improvements

- Incorporate additional pollution indicators such as PM2.5 and PM10.
- Explore more machine learning algorithms and compare their performance.
- Add explainability methods to understand which features influence predictions.
- Improve validation across different regions and time periods.
- Explore updated environmental data feeds.
- Develop a reproducible pipeline with documented preprocessing, feature definitions, and model evaluation.

## Team

**Team Data Delvers**

- Mare Supriya
- Lenka Sai Eswari
- Petluri Vyshnavi

## Acknowledgements

The project references publicly available data resources from the World Health Organization, the Government of India Open Government Data Platform, and OpenCity.

## Disclaimer

This project is intended for educational and analytical purposes. Its visualizations and model predictions are exploratory and should not be interpreted as validated medical findings or evidence of a causal relationship between pollution and disease.
