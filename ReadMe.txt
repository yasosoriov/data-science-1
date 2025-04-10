The present analysis utilizes the Readmissions and Deaths - Hospital dataset, which contains data on hospital readmission and mortality rates in the United States. This dataset provides information on various hospitals, including location, performance measures for specific treatments, and comparisons with the national average.

The objective of this project is to analyze hospital readmission and mortality rates, identifying patterns and factors that may influence these indicators. Key questions explored include: Are there significant differences in service quality across different states? Do mortality and readmission rates vary based on hospital type or specialty? Can hospitals with better or worse performance be identified based on specific characteristics?

To answer these questions, exploratory data analysis (EDA) was conducted using univariate, bivariate, and multivariate visualizations. Graphs were used to represent data distributions and compare hospitals and regions. Additionally, missing values were identified and assessed for their impact on the analysis.

To assess the factors influencing hospital readmission and mortality rates, a regression approach was adopted using the Score variable as the target. This variable reflects either readmission or mortality rates, depending on the specific measure, and was chosen due to its relevance and availability across hospitals.

A feature selection process was applied to prioritize interpretability. The variable Denominator, which represents the number of cases evaluated per hospital and measure, was selected as the primary predictor. This choice is justified by its strong relationship with the Score and its presence across most entries.

Two regression models were trained and compared:

Linear Regression: chosen for its simplicity and interpretability.

Random Forest Regressor: selected as a more robust, non-linear alternative to capture complex patterns.

Model performance was evaluated using the following metrics:

Root Mean Squared Error (RMSE): selected as the main evaluation metric due to its interpretability in the same unit as the Score.

R² (coefficient of determination): used to assess how well the model explains the variability in the data.

The models produced the following results:

Linear Regression: RMSE: 4.92 R²: 0.00

Random Forest: RMSE: 5.03 R²: -0.04

Final Conclusions: The objective of this work was to apply feature selection, train a regression model, compute validation metrics, and draw conclusions based on a dataset related to hospital performance. The target variable was Score, and only Denominator was used as a predictor, with a focus on model interpretability.

Although the linear regression model was selected for its simplicity and the random forest for its ability to capture nonlinear relationships, the results show that neither model was able to explain the variability in Score effectively when using only Denominator as input. The R² values close to zero (and negative in the case of random forest) indicate that the models performed no better than simply predicting the mean Score.

This highlights the limitations of using a single feature to model complex outcomes such as hospital readmission or mortality rates. Future work should incorporate additional variables, such as measure type, medical condition, hospital characteristics, or geographic location. Exploring other modeling techniques, cross-validation, and multi-feature selection could also improve performance.

Overall, this analysis reinforces the importance of deep data understanding and thoughtful feature selection in predictive modeling.

