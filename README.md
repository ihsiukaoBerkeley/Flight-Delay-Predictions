Approximately 7-9k flights daily (25% of domestic flights annually) are delayed in the United States, costing airlines and airports $16-20k hourly and leaving hundreds of thousands of passengers frustrated and scrambling. Delays also cost passengers ~$47 hourly, meaning each delay drastically increases the chances of passenger dissatisfaction and customer loss. Emerald Airlines’ annual survey reported passengers would be more amenable to a 15+ minute delay given advanced warning of ~2-3 hours (87% “Definitely Agree”). Thus, this project concerned the feasibility of detecting delays.

Analysis of the NOAA GSOD (daily weather) and the DoT ATP (airline performance) datasets indicated that weather and visibility conditions impacted potential delays the most, while a logistic regression learning model indicated an average classification ability (via F-0.5 score) of ~55-60%. However, implementing a graph network confirmed our hypothesis of nonlinearities in the data, with a Multilayer Perceptron returning ~60-65% classification ability (via F-0.5 score) on average.
