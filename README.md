# regression

Regression modelling is used to explain a phenomenon's behaviour. Let Y represent the phenomena of interest, in this case FDI. The data analyst uses regression modelling to understand Y's variability. A multiple regression model predicts the association between the response variable and the explanatory variables that we believe explain Y's behaviour.

This model's functional form is:
FDI = b0 + b1(GDP_cap) + b2(Gr_rate) + b3(ROC) + b4(Stable) + b5(Infra) + b6(Trade) + e
which is a linear regression model, the highlighted values are the explanatory variables, and "e" is the error term.

While, Variability or R2 (R2 = The Explained Variation in Y/The Total Variation in Y), which spans from 0% to 100%, is used to analyse the model's fitness. It evaluates how effectively the explanatory factors explain Y. The greater R2, the better the model's fit and prediction.
In this model, the researcher’s viewpoint should anticipate all explanatory factors to have a positive influence on the response variable, such as a rise in GDP_cap for the nation receiving the investment increasing FDI undertaken in the country. More FDI will be invested in a nation with greater trade (Trade) and infrastructure (Infra). The parameter Stable, will negatively affect FDI since the more are the government changes, the less stable a country's political situation is.

To begin, Infra and Trade are attribute variables, meaning that it describes their outcomes through characteristics such as gender. Thus, by applying the function "as.factor()"to an attribute, generates a new variable with the same values as the attribute variables but stores 


integer and string data as levels. This can help find hidden patterns or trends in data and improve the statistical model's accuracy and interpret-ability.

when fitting a regression model the research seeks to answer some questions, these are: Does the fitted model make sense? Overall is the model a good fit? and individually, are the explanatory variables important?
firstly, we will examine the impact of each individual variable to see if our viewpoint is correct.
 
As it was stated in the original expectation, ROC, GDP_cap, and Gr_rate exert a weak to mildly strong positive correlation, which describes a relationship between 2 elements, with the response variable FDI (of 0.609, 0.270 and 0.590); this suggests a positive trend that as each indicator grows so will the value of FDI undertaken. The explanatory variable Trade has a modest positive connection to FDI, since only a small portion of their interquartile range overlaps. As mentioned in the viewpoint, Stable also has a negative link with FDI of -0.411.

Infra has no impact on the response variable, indicating no link, this is observable through their distribution function as they’re almost identical. Although the first viewpoint seems to reflect the facts, the correlation between explanatory factors must also be considered. First, Infra and ROC are correlated, and do also ROC, GDP_cap, and Gr_rate are highly multicollinear. Multicollinearity occurs when variables are highly linked. Multicollinearity makes it difficult to determine an explanatory variable's influence on a response variable, which can complicate model interpretation. This is shown in multiple ways, but the main ones are correlation between explanatory variables and/or different expected signs for coefficients. Researchers must monitor the importance of employing all of these factors in the model and eliminate highly linked independent variables.
 
The fitted model's parameters differ from the basic assumptions that were established earlier. The regression model shows negative Gr_rate when all explanatory variables are combined, which was not predicted from the initial viewpoint. Gr_rate seems insignificant despite its substantial association with the response variable. This might be due to the strong multicollinearity between independent variables. 

  However, The model fits well, with an R2 of 74.8% and an adjusted R2 of 71.4%. F-stat = 22.1 > F-crit = 2.191, hence H1 is accepted through given a 5% significance level test. As indicated above, multicollinearity affected certain explanatory variables; these must be separately examined to determine their relevance using a t-test or p-value test to assess whether they are statistically significant. Per the perspective, Infra was negligible, and the fitted model shows it to be insignificant at a 5% level. It will be removed to analyse how the remainder of the model operates. 

After thorough study and elimination of unimportant and correlated explanatory variables (ROC, Infra, and Gr_rate) one by one through a 5% t-test, the final model had statistically significant remaining explanatory variables, which were preserved. R2 and R2 adjusted are 74.79% and 72.95%, indicating a significant relationship between the independent variables and the response variable, meaning GDP_cap, Stable, and Trade explain 74.79% of FDI. R2 adjusted has increased, because of its smaller bias in correlating competing regression models, it gives a better approach in comparing models with different k values. The model with the greatest adjusted R2 is fitter.
final model structure:
FDI = b0 + b1(GDP_cap) + b2(Stable) + b3(Trade) + e
for the coefficients: R has created three "sub" dummy variables for the variable Trade:
y = b0 + b1(GDP_Cap) + b2(Stable) + b3(Trade2) + b4(Trade3) + e
y =189.4274+0.9109(GDP_cap) + -0.5411(Stable) + 4.8837(Trade2) + 5.9368(Trade3) + e

where Trade1 = b0.
Therefore, increasing xi by one unit increases FDI by the highlighted estimates in the figure above.

Based on initial and final data analysis, the model is the best fit possible, and a link between explanatory variables and response variable is proven. R2 of ~ 75% suggests the model's prediction has "good value". This model's estimates are likely accurate.
Question 1.2)
y = b0 + b1x1 + b2x2 + b3Trade2 + b4Trade3 + e
y = 189.42 + 0.91(11.1) - 0.54(11) + 194.31(1) + 195.36(0) = 387.89
This estimate is 75% accurate, thus FDI will be £387.89million.
The model predicts FDI accurately but has flaws. The final 4 factors explain 3/4 of Y's variability, but 1/4 is unknown, therefore FDI's forecast may be imprecise.
FDI factors include per-capita GDP, political stability, and trade openness. In real life, elements such as corruption, inflation, and unemployment are also vital, as well as ROC and Gr_rate can have an impact, which, in this model are removed due to multicollinearity.
Question 2.1)
The corporation can assess its finances using the 4 financial ratios. A company's profitability over time is measured by its retained earnings ratio (x1). Profitable companies have higher retained earnings ratios. EBIT(x2) measures operating profitability. It measures a company's pre-tax profits and operational efficiency. Sales-to-total-assets ratio (x3) gauges revenue-generating ability. A higher ratio shows a company can generate revenue from its assets. Cash flow to total debt ratio (x4) indicates a company's debt-paying ability. Higher ratios may indicate good cash flow and debt repayment.
At first look, all the components will affect a corporation positively by looking at all the factors, therefore indicating a probability of whether the firm will go bankrupt or be solvent. The output Y represents a binary response variable, which can only take value 1 or 0. where 1 indicates solvency occuring and the 0 indicates bankruptcy. Thus, positive explanatory factors increase the likelihood of the firm's longevity.

In this case it can be assumed that a unit increase in the explanatory variables will increase the probability of a firm remaining solvent, this can be observed through the definition of the factors, high level x1, x2, x3 and x4 only improves the firm.

y = b0 +b1x2 + b2x2 + b3x3 + b4x4 + e is the model functional form.

 
The dependent variable shows a positive association with all explanatory factors except x4. The cash-flow to total debt ratio shows a slight negative effect on the dependent variable, which contradicts the earlier interpretation. A unit rise in x4 would increase the likelihood of the firm declaring bankruptcy. whereas x1, x2, x3 improve its solvency chance. 

The negative correlation of x4, which appears to be multicollinearity, is also affecting x1 and x2. High correlation causes multicollinearity. Model interpretation can be hindered by multicollinearity. The main ways multicollinearity is seen are correlation between explanatory variables and/or distinct predicted signs for coefficients. Researchers must assess the model's need for these parameters and delete strongly related independent variables.

Question 2.2)
Logistic regression models a binary response variable and one or more explanatory factors. Logistic regression predicts probability of an event occurring. It is a generalised linear model with a maximum and minimum probability. Based on the 4 parameters, Y might be solvent or bankrupt. A binary regression might model this data and predict the outcomes probability, which is solvency in this case.

Linear and logistic regression differ in three ways: logistic models have nonlinear Y-X relationships, a logistic model has non-normal error terms, for a logistic model the assumption of equal/constant variance (homoscedasticity) does not hold.
The outcome of a logistic model is obtained through a logit transformation, this models the non-linear relationship of Y and its Xs to linear, it transforms the predicted probability of Y = 1 (firm remaining solvent) into log odds of the event occurring. 
p/(1-p) = e^(b0 + b1x1 + b2x2 + bkxk) where p = P(Y=1|X=x)=e^(b0 + b1x1 +...)/(1 + e^(b0 + b1x1 +...) ) The odd ratio compares event odds for different degrees of explanatory variable.
The final model is the logit:
 g(x1,x2,...,xk)= log(p/(1-p))= b0 + b1x1+ b2x2+...+ bkxk.
Finding the parameter values that maximise the likelihood function, which indicates the probability of observing a certain sample of data given a set of parameter values, is the MLE.
We will split test-train data 80:20 before model fitting. The training set is used to fit the logistic regression model, while the test set is used to assess its performance. It prevents overfitting, compares model performance, and improves training data fidelity. While "set.seed()" repeats the same random generalisation each time. 
Using the glm() function, estimate a logistic regression model.
 
The fitted model confirms the graph interpretation that x4 was negatively associated to Y. 

The fitted odds ratio logarithm, or logit of the firm's solvent probability p, is:
g(x1,x2,x3,x4) = log(p/(1-p))  = -3.47 + 11.01x1 + 22.72x2 + 1.25x3 - 0.64x4
If xi changes by one, the log probabilities of a firm being solvent rise by the indicated estimations in the figure above, for ceteris paribus. Therefore, the odds of a firm being solvent (vs being bankrupt) increases by e^(bi) for a unit change in ratio xi, with ceteris paribus. That is, for a change in x1, the odds of the event occurring increase by 6071357%. However, this number seems very unrealistic. Although the odd ratio extends from zero to infinity, it is to be questioned whether this result e^(x1) is plausible with the research being observed, Keeping in mind the first assumptions. The model's results may be biased or unreliable if certain those are not satisfied.
The researcher may determine if the four components are independently significant by looking at the Pr(>|z|) column, which does a Wald-test. At 5% significance, x4 doesn't appear to be substantially different from 0, suggesting removal as it doesn't predict the logit of the data.
However, to properly examine this, a G statistic is needed which test the goodness of fit.
G = likelihood without the predictors − likelihood with the predictors, a chi-squared statistic that identifies the null and alternative hypotheses: h0: bi = 0, h1: at least one differs from 0 where I = 1,2,3,4.
G calc = 81.77 > G crit = 9.48 at 5% sig. level, H1 is accepted, hence this model is statistically valid, and the variables have explanatory power. 
(Since we already know that 3 variables are different from 0, we simply utilise G to test model fitness)
The model appears to be fit, but x4 is not relevant, as determined by Wald test at 5% significance level. If two or more variables were insignificant, the formula "anova(model, test = "Chisq")" would have been needed to compare the smaller models to the following more complex ones by adding one variable at a time, which compares them by using the likelihood ratio test. 
We'll use the Akaike Information Criterion (AIC) to compare the alternative model's fit, which penalises for model parsimony. The formula is AIC = − 2*maximum log-likelihood + 2*number of parameters.
 
The prior model's AIC was 51.589, whereas the revised model's AIC is 51.645, demonstrating that all factors strongly explain logits. it enhances the new model. Since x4 was removed, the odds of a company becoming solvent have increased. Thus, changing x1 increases the event's probabilities by 2430336%. 
Using the 20% data set aside, is used to calculate the total accuracy rate. 

To fit the model predict.glm() is used, it utilises a generalised linear model to take a data frame or matrix with predictor variables and return a vector of predicted response variable values.
 
Given the 5th observation, the probability of the response variable being 1—the firm staying solvent—is 0.9995. While, for the 10th observation, the probability is 0.1305.
After obtaining the projected model, we may assess its accuracy with a confusion matrix, which shows the number of true positive, true negative, false positive, and false negative predictions generated by a statistical model.
 
According to the confusion matrix, our model's accuracy is 21/22 true positive and true negative situations. While the sensitivity, which is the proportion of occurrences when y =1, is 10/11 for the true positive, the true negative was successfully predicted at 11/11. The model prediction is in fact very high at a 95.45%


Question 2.3)
The 95.45% accuracy percentage doesn't distinguish between types of errors. However, model accuracy is not necessarily the most significant factor. In some circumstances, increasing true positives or true negatives is crucial. In a medical diagnosis application, a high recall (to reduce false negatives) may be more significant than precision. 

Based on initial and final data analysis, the model provides the best fit and links explanatory factors to response variables, with respect to the assumption established above. The model's 95.45% accuracy means that per unit increase in any explanatory variable, it will correctly predict whether the business will remain solvent or go bankrupt.
