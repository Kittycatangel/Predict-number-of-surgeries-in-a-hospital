# Number of surgeries in a hospital

# Objectitives

Predict the number of surgeries that the hospital will have for this month.

# Instructions

The linear regression model is written in python v.3 programming lamguage (Jupyter Notebook).

# Method

I use OSEMN approach in every project. It means the data is obtained, scrubbed and cleaned, explored and visualized, modelled and interpreted.

Data science process is iterative, which means a lot of back-and-forth testing new ideas, new features to include, tweaking various hyper-parameters, and so on.

Data exploration is very important before to start modelling. I will do data cleaning, looking for missing values and replacing the missing values. Identifying outliers and solving the problem. Identifying linearity (linear relationship) and multicollinearity (detection of correlated parameters).

# Interpretation

Covariates are  given according how strong is the R squared, cofficients and p value. If in general r squared is close to 1, we have a good performing model. For covariates, if the p-value is les than 0.05 and high coefficient, it meanes that this particulr covariate has a direct impact on the model prediction and we need to keep including this particular covariate. If the included covariate has a p value greater than 0.05 and low coeffieciet we can eliminate this particular coeffiecent form our prediction model.

The most significat coeffiecient that positively impact the model is "surgeries last month" according to the multi linear regression model using statsmodels.

The linear regersion model ( linear relationship between surgeries last month and surgeries this month) had R squared of 0.89 which is very good. However when we include all other features., the model does not perfom as good with R squared of 0.7. Other features should be included in the model to accurately predict the number of surgeries with the least mean absolute error (MAE).

The output for the regression summary is : 

OLS Regression Results
Dep. Variable:	surgeries_this_month_log	R-squared:	0.751
Model:	OLS	Adj. R-squared:	0.702
Method:	Least Squares	F-statistic:	15.21
Date:	Tue, 14 Sep 2021	Prob (F-statistic):	3.83e-35
Time:	14:54:33	Log-Likelihood:	-144.08
No. Observations:	200	AIC:	356.2
Df Residuals:	166	BIC:	468.3
Df Model:	33		
Covariance Type:	nonrobust		
coef	std err	t	P>|t|	[0.025	0.975]
const	0.0698	0.217	0.321	0.748	-0.359	0.499
surgeries_last_month_log	0.8169	0.041	19.937	0.000	0.736	0.898
age_in_yrs_log	0.0227	0.040	0.560	0.576	-0.057	0.103
service_id_2	0.2682	0.096	2.780	0.006	0.078	0.459
service_id_3	-0.3728	0.103	-3.631	0.000	-0.575	-0.170
last_name_ANDERSON	-0.2249	0.272	-0.827	0.409	-0.762	0.312
last_name_BROWN	-0.4384	0.295	-1.485	0.139	-1.021	0.144
last_name_CLARK	0.0332	0.266	0.125	0.901	-0.493	0.559
last_name_DAVIS	-0.0600	0.306	-0.196	0.845	-0.663	0.543
last_name_GARCIA	0.0724	0.378	0.192	0.848	-0.674	0.819
last_name_HALL	0.1341	0.296	0.453	0.651	-0.450	0.718
last_name_HARRIS	0.0888	0.278	0.320	0.749	-0.459	0.637
last_name_HERNANDEZ	-0.2681	0.378	-0.708	0.480	-1.015	0.479
last_name_JACKSON	0.1904	0.273	0.697	0.487	-0.349	0.730
last_name_JOHNSON	-0.0348	0.278	-0.125	0.901	-0.584	0.515
last_name_JONES	0.1751	0.348	0.504	0.615	-0.511	0.861
last_name_KING	-0.1180	0.271	-0.435	0.664	-0.653	0.417
last_name_LEE	0.1110	0.306	0.363	0.717	-0.493	0.715
last_name_LEWIS	-0.0481	0.278	-0.173	0.863	-0.596	0.500
last_name_MARTIN	0.1686	0.296	0.570	0.569	-0.415	0.753
last_name_MARTINEZ	0.0129	0.344	0.038	0.970	-0.666	0.691
last_name_MILLER	-0.0271	0.294	-0.092	0.927	-0.607	0.553
last_name_MOORE	-0.0877	0.323	-0.272	0.786	-0.725	0.549
last_name_ROBINSON	0.1133	0.307	0.369	0.712	-0.492	0.719
last_name_RODRIGUEZ	-0.0720	0.279	-0.258	0.796	-0.622	0.478
last_name_SMITH	-0.0874	0.295	-0.296	0.768	-0.671	0.496
last_name_TAYLOR	0.1148	0.296	0.388	0.699	-0.470	0.700
last_name_THOMAS	-0.0728	0.309	-0.236	0.814	-0.682	0.537
last_name_THOMPSON	-0.0831	0.306	-0.272	0.786	-0.687	0.521
last_name_WALKER	-0.4127	0.307	-1.344	0.181	-1.019	0.194
last_name_WHITE	-0.5823	0.309	-1.887	0.061	-1.192	0.027
last_name_WILLIAMS	-0.0601	0.308	-0.195	0.845	-0.667	0.547
last_name_WILSON	-0.2389	0.323	-0.739	0.461	-0.878	0.400
last_name_YOUNG	0.0643	0.443	0.145	0.885	-0.810	0.939
Omnibus:	140.252	Durbin-Watson:	2.058
Prob(Omnibus):	0.000	Jarque-Bera (JB):	1685.527
Skew:	-2.510	Prob(JB):	0.00
Kurtosis:	16.306	Cond. No.	34.5

# Conclusion

Linear regression model(sklearn) is a model with mean absolute error of 20. This Model predict the number of surgeries for this month within 20 of the true number of surgeries on average.

Multiple linear regression model with statsmodel have R squared of 0.7. The linear regression model shows a good correlation between surgeries last month and the surgeries this month with R squared of 0.89.
