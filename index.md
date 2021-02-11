# Portfolio

---

### Quick Links to GitHub Repositories
* [Project 1: Spatial Statistics](https://github.com/Emma-M-Collins/spatial_stats)
* [Project 2: Master's Project (Apriori Algorithm)](https://github.com/Emma-M-Collins/apriori)
* [Project 3: Linear Regression with Categorical Variables](https://github.com/Emma-M-Collins/turnout_time)
* [Project 4: Classification Showdown](https://github.com/Emma-M-Collins/classification)

---

## Spatial Statistics:<br>[Identifying High Suicide Rates in Colorado](https://github.com/Emma-M-Collins/spatial_stats)
* Aim to identify high rates of suicide among Colorado counties from publically available data from U.S. Census Bureau and Colorado Dept. of Health and Environment.
* Used Spatial Scan Test and Cluster Evaluation Permutation Procedure (CEPP) under Constant Risk Hypothesis to identify areas with higher rates of suicide.
* Re-tested using Poisson GLM for expected counts of suicide per county based a selection of statistically significant variables based on research.

![Proportion of Suicides](images/suicide_proportion.png)

---

## Master's Project:<br>[An Introduction to the Apriori Algorithm for Mining Association Rules...](https://github.com/Emma-M-Collins/apriori)
Master's project necessary for M.S. of Statistics degree completion.  Full paper, oral presentation slides, and apriori code examples on GitHub repository.

### Abstract
The apriori algorithm was originally created for use on transaction data, large datasets that record the items bought together in individual purchases over a set length of time.  Since its development in the mid 90's, the apriori algorithm has expanded into various areas of research.  The algorithm finds groupins of items frequently purchased together through use of joint and conditional probabilities and pruning.  The pruning method removes sets of items that do not reach use-picked thresholds to avoid longer computation times.  The apriori algorithm has been used in commerce, medical, and environmental fields, where items sold in a store are replaced by purchasing habits, patient demographics and symptoms, or geographical features, respectively.  Each topic has unique context with varying user-picked thresholds and different dimensions: we expect more observations of rainfall in a specific tropic climate than the number of patients diagnozed with a disease at a specific hospital.  Implications of incorrect analysis vary from inaccurate weather forcasts to life or death scenarios.  These parameters and frameworks are explored and compared for each area of study after introducting and explaining the apriori algorithm.  Lastly, a brief introduction to improvements and hybrid methods of the algorithm is provided.

---

## Linear Regression:<br>[Thornton Fire Department Turnout Time Analysis](https://github.com/Emma-M-Collins/turnout_time)

* Consulting with Thornton Fire Department (TFD) to help identify what variables, such as engine and call type, increase turnout time, the time it takes to put on the proper gear to leave the station after receiving a call.  
* Focus on *inference* over *prediction*.
* Raw data provided from TFD from 2014-2018, over 100,000 observations and 100 potential variables.  After discussion with TFD personnel, less than 15 variables were considered relevant to build the model.

![Call Type Boxplot](images/CallBox.png)

National Fire Protection Association recommends a 60 second turnout time (blue line) for EMS calls and 80 seconds (red line) for complex calls.

* Used BIC stepwise selection to determine final model.  Model was checked for any outliers and influential observations as well as a bootstrap test to ensure coefficient values.
* Final model has 105 coefficients because of the number of categorical variables, and over 78,000 degrees of freedom.

![Final Model](images/FinalModel.png)

The model uses Shift A, Engine 71 responding to an auto accident between 7 and 8 AM, in June 2014 as a reference level.  On average, a call with these features has a turnout time of 103 seconds.  All other calls, engines, shifts, and times will be compared to these. 

![Coefficients for Dummy Variables](images/CallCoeff.png)

Thus, if Shift A, Engine 71 responds to an EMS-ECHO call, between 7 and 8 AM in June 2014, they will be 10 seconds faster on average.  But if they respond to a hazmat call they will be about 10 seconds slower, on average. 

---

## Classification:<br>[Logistic Regression vs Random Forest on Sonar Dataset](https://github.com/Emma-M-Collins/classification)
* Uses the [Sonar dataset](https://archive.ics.uci.edu/ml/datasets/Connectionist+Bench+%28Sonar%2C+Mines+vs.+Rocks%29), from University of California, Irvine's [Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php). 
* 208 observations of binary data with 60 continuous predictors of highly colinear data.
* Aim to see whether logistic regression or random forest performs better.
* Better method will be determined by accuracy, precision, true positive rate, false positive rate, false negative rates, and ROC curves/AUC.
* Data split into 75% training data and 25% test data.

| Method (Test Data) | Accuracy | Precision |  TPR |  FPR |  FNR |
| ------------------ | --------:| ---------:| ----:| ----:| ----:|
|Logistic Regression |     0.615|      0.625| 0.714| 0.333| 0.429|
|Random Forest       |     0.808|      0.750| 0.964| 0.042| 0.321|

<br>

ROC Curves | & AUC
--- | ---
![](images/LRROC.png) | ![](images/RFROC.png)

* In all facets, random forest outperforms logistic regression.
* Logistic regression had a massive problem with colinearity, unstable results
* ROC curves also indicates random forest predicts much better, the high AUC indicates the method has high seperability

### Random Forest Wins!

---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
