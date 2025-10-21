# CERN Dielectron Collision - Invariant Mass Prediction

Goal: Predict the invaraint mass of electron-positron collision data using linear regression.

## Dataset
 - 100 000 CERN dielectron collision events
 - Features:
    1) Run: The run number of the event.
    2) Event: The event number.
    3) E1, E2: The total energy of the electron (GeV) for electrons 1 and 2.
    4) px1,py1,pz1,px2,py2,pz2: The components of the momemtum of the electron 1 and 2 (GeV).
    5) pt1, pt2: The transverse momentum of the electron 1 and 2 (GeV).
    6) eta1, eta2: The pseudorapidity of the electron 1 and 2.
    7) phi1, phi2: The phi angle of the electron 1 and 2 (rad).
    8) Q1, Q2: The charge of the electron 1 and 2.
    9) M: The invariant mass of two electrons (GeV).
 - Target: Invariant mass (M) in GeV

## Approach
I implemented linear regression in three ways:
1. Scikit-learn linear regression model
2. Matrix operations
3. Gradient descent algorithm

## Results
 - Inital Root Mean Squared Error (RMSE) of 9.25 GeV.
 - After feature engineering it reduced to 6.17 GeV.
 - *33%* improvement

## Visualizations
 - Scatterplot: Predicted vs Actual values of M
 - Residualplot: Reveals linear model limitations. Nonlinear model like polynomial regression would likely perform better.
 - Heatmap: Correlation coeficients
 - Loss curve for the gradient descent implementation

## Technologies
- Python, NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn

## Files
 - "/notebooks/0_Data_Exploration.ipynb" - Data cleaning, adding few features, physics check
 - "/notebooks/1_sklearn_model.ipynb" - Scikit-learn implementation of linear regression
 - "/notebooks/2_linear_regression_using_matrix_operations.ipynb" - Matrix operation implementation
 - "/notebooks/3_linear_regression_using_gradient_descent.ipynb" - Gradient descent implementation
 - "/notebooks/4_feature_engineering.ipynb" - Feature engineering, RMSE reduction
 - "/notebooks/5_Visualizations.ipynb" - Few plots
 - "/data/dielectron.csv" - original data
 - "/data/cdata.csv" - cleaned data
 - "/data/final_data.csv" - data with added features
 - "/data/y_test.csv" - invariant mass true values
 - "/data/yPredictions.csv" - invariant mass predicted values
