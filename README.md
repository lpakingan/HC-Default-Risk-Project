# Home Credit Default Risk Prediction

Group project that created an EDA and machine learning pipeline for predicting loan default risk for underbanked populations lacking traditional credit histories.

## Dataset

**Home Credit Default Risk dataset from Kaggle:**
- 300,000+ loan applications
- 122 features across 7 related tables
- Bureau records, previous applications, and payment histories

## Methodology

### Data Preprocessing
- Handled missing values across multiple data sources
- Applied IQR-based outlier treatment with domain-specific constraints
- Integrated supplementary data from bureau records, previous applications, and payment histories

### Feature Engineering
Created 15 new features including:
- **Financial ratios:** credit-to-income, annuity-to-income
- **Temporal indicators:** age, employment duration
- **External score combinations**

### Modeling
- Implemented **Logistic Regression** as baseline model
- Developed **LightGBM** as primary prediction model
- Applied **isotonic probability calibration** for reliable PD estimates

## Business Applications

Final model outputs calibrated default probabilities that can be mapped to credit scores (300-850 scale) for:
- Risk-based pricing
- Portfolio management
- Regulatory compliance
