# CA03 – Decision Tree Classification (Income Prediction)

## Project Overview
This project implements a **Decision Tree classification model** to predict whether an individual earns **more than $50K** or **less than or equal to $50K** based on demographic and employment-related attributes.

The goal of this assignment is to **build, evaluate, tune, and analyze** a decision tree model using a **structured, manual hyperparameter tuning process**. All analysis is performed in a **Jupyter Notebook** and follows the assignment instructions.

---

## Data Source
The dataset used in this project is provided by the **U.S. Census Bureau** and contains demographic information along with income labels.

- **Number of instances:** 48,842  
- **Number of attributes:** 7 (plus label and train/test indicator)  
- **Target variable:** Income  
  - ≤50K (0)  
  - >50K (1)

The dataset is accessed directly from the following source and used consistently throughout the project:  
https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true

Continuous variables in the dataset have been **discretized (binned)** into categorical groups, making them more suitable for decision tree modeling.

---

## Data Quality Analysis
A data quality analysis was performed to evaluate the completeness and structure of the dataset. This included checking for:

- Missing values  
- NaNs  
- Duplicate records  
- Descriptive statistics for each variable  

**Findings:**
- No missing values were found.
- Duplicate rows exist due to the discretization of features, which causes multiple individuals to share identical category combinations.
- These duplicates represent valid observations and were retained.

---

## Modeling Approach
A **Decision Tree Classifier** from the `scikit-learn` library is used for this project. The modeling process includes:

- Separating training and testing data  
- Training the classifier  
- Evaluating model performance using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion matrix

---

## Hyperparameter Tuning
Manual hyperparameter tuning is performed across **four sequential runs**. In each run, one hyperparameter is varied while the best-performing values from previous runs are retained.

The tuned hyperparameters include:
- Split criterion (Gini impurity or entropy)
- Minimum number of samples per leaf
- Maximum number of features
- Maximum depth of the tree

Model performance is evaluated using **test accuracy**, with results recorded in tabular form. Line graphs are used to visualize the relationship between hyperparameter values and model accuracy.

---

## Best Model Analysis
The best-performing decision tree model is selected based on the **highest test accuracy** achieved during hyperparameter tuning. Performance metrics for this model are reported and used to assess:

- Generalization performance  
- Potential overfitting  

---

## Prediction on New Data
The trained model is used to predict the income category of a new individual based on provided demographic attributes.

- A single-record DataFrame is created
- The same structure, binning, and encoding as the training data are applied
- The predicted income class and associated probability are reported

---

## Software and Libraries Used
The following software and libraries are required to run this project:

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn  

---

## How to Run the Project
To run this project:

1. Clone or download the repository  
2. Install the required libraries  
3. Open the Jupyter Notebook  
4. Run all cells sequentially from top to bottom  

No additional configuration is required.

---

## Acknowledgements
- Dataset provided by the **U.S. Census Bureau**
- Decision Tree implementation based on **scikit-learn**
- Assignment structure and requirements provided through course materials

---

## Authors
- Sude Ademogullari  
- Sadaf Sarbazi  
