# Number of surgeries in a hospital

# Objectitives

Predict the number of surgeries that the hospital will have for this month.

# Instructions

The linear regression model is written in python v.3 programming lamguage (Jupyter Notebook).

# Method

I use OSEMN approach in every project. It means the data is obtained, scrubbed, cleaned, explored, visualized, modelled, and interpreted.

Data science process is iterative, which means a lot of back-and-forth testing new ideas, new features to include, tweaking various hyper-parameters, and so on.

Data exploration is very important before to start modelling. I will do data cleaning, looking for missing values and replacing the missing values. Identifying outliers and solving the problem. Identifying linearity (linear relationship) and multicollinearity (detection of correlated parameters).

# Interpretation

Covariates are  given according how strong is the R squared, cofficients and p value. If in general R squared is close to 1, we have a good performing model. For covariates, if the p-value is less than 0.05 and high coefficient, it meanes that this particular covariate has a direct impact on the model prediction and we need to keep including this  covariate. In contrast, If the included covariate has a p value greater than 0.05 and low coeffieciet we can eliminate this particular coeffiecent form our prediction model.

The most significat coeffiecient that positively impact the model is "surgeries last month" according to the multi linear regression model using statsmodels.

The linear regersion model using statsmodel( linear relationship between surgeries last month and surgeries this month) had R squared of 0.89 which is very good. However, when we include all other features., the model does not perfom as good with R squared of 0.7. Other features should be included in the model to accurately predict the number of surgeries with the least mean absolute error (MAE).




# Conclusion

Linear regression model(sklearn) is a model with mean absolute error of 20. This Model predict the number of surgeries for this month within 20 of the true number of surgeries on average.

Multiple linear regression model with statsmodel have R squared of 0.7. The linear regression model shows a good correlation between surgeries last month and the surgeries this month with R squared of 0.89.
