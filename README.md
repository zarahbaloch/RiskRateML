This project builds a workflow to predict health insurance charges using the insurance.csv dataset (Medical Cost Personal Dataset on Kaggle, https://www.kaggle.com/datasets/mirichoi0218/insurance). The repository includes a pipeline, modular code in src/, unit tests, and a final modeling notebook.

**Notebook Overview** 
- Load Data
- Exploratory Data Analysis
- Feature Engingeering
- Train/ Test Split
- Scaling
- Modeling (Linear Regression, Random Forest Regressor)
- Feature Importance

**Source Code (src/)**
- src/data.py (loads the dataset + basic information for EDA checks)
- src/features.py (splits df into x and y, encodes categoricals) 
- src/ models.py (train/ test split helper, feature scaling, LR training, RF training) 
- src/utils.py (metric calculation, clean printing functions)

  **Test Suite (tests/)**
Each part of the pipeline is validated using pytest

**Model Performance Summary** 
1) Linear Regression
    - MAE: 4181 (predicts charges with an average error of $4181) 
    - RMSE: 5796 (typical deviation is around $5796)
    - R2: 0.7836 (explains 78.36% of the data)
  
2) Random Forest (Stronger Model) 
    - MAE: 2558 (predicts charges with an average error of $2558)
    - RMSE: 4576 (typical deviation is around $4576)
    - R2: 0.8651 (explains 86.51% of the data)
  
