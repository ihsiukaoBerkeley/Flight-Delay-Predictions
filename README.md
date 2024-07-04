## Flight Delay Predictions

### Abstract

Approximately 7-9k flights daily (25% of domestic flights annually) are delayed in the United States, costing airlines and airports $16-20k hourly and leaving hundreds of thousands of passengers frustrated and scrambling. Delays also cost passengers ~$47 hourly, meaning each delay drastically increases the chances of passenger dissatisfaction and customer loss. Emerald Airlines’ annual survey reported passengers would be more amenable to a 15+ minute delay given advanced warning of ~2-3 hours (87% “Definitely Agree”). Thus, this project concerned the feasibility of detecting delays.

Analysis of the NOAA GSOD (daily weather) and the DoT ATP (airline performance) datasets indicated that weather and visibility conditions impacted potential delays the most, while a logistic regression learning model indicated an average classification ability (via F-0.5 score) of ~55-60%. However, implementing a graph network confirmed our hypothesis of nonlinearities in the data, with a Multilayer Perceptron returning ~60-65% classification ability (via F-0.5 score) on average.

### Results and Discussion

Final analysis of the normalized datasets indicated that the Logistic Regression (LR) and the Multilayer Perceptron (MLP) models performed the best out of all four architectures tested for this project. The LR model boasted an ~ 60% success rate with moderate overfitting, while the MLP model performed even better with an ~ 65% success rate, albeit with heavier overfitting. Meanwhile, the Decision Tree algorithm performed fairly well (~ 57%) but scaled less adequately time-wise than the LR and MLP models, and the XGBoost model was unscalable past 3 years of data.

However, as can be seen in the tables above, the excellent results seen in the LR and MLP models unfortunately were seemingly only present during the training phase, not the test, as the F-0.5 scores dropped drastically after transitioning from the training to the test phases. This is curiously in opposition to the Area Under the Curve (AUC) scores, though, as both the LR and MLP models scored in the 60-70% range (consistent with the training F-0.5 scores) for both phases very consistently. It's hypothesized that this effect may have been due to an improperly calibrated F-beta score, but it could also have been due to the feature selection procedure, as both processes have massive effects on the model's ability to properly interpret results.

## For more information, please view the Final Report
