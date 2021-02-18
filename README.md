#  USING SUPERVISED MACHINE LEARNING (cross-validation framework) TO PREDICT PREPRINTS' PUBLICATION STATUS

* As part of my dissertation I developed an innovative record-linkage program to match preprint records to their final published, peer-reviewed counterparts. The extensive diagnostic test I perform reveals a F1-score of 0.86, which is the highest F-1 score ever recorded for an algorythm trying to match preprints with their peer-reviewed counterparts. That said, the main approach I developed as part of my PhD dissertation rely on a rule-based approach and not machine-learning. Using rule-based methods such as fuzzy matching is not problem in itself, but it is extremely cumbersome to maintain and optimize since the sensitivity analysis need to be performed manually. Machine-learning approaches on the other hand simplify both code optimization and performance analysis. Therefore, in addition to the main method I developed in my PhD, I am also currently building a logistic regression as a supervised machine learning model within a cross-validation framework.

##  FEATURE ENGINEERING

1. create thousands of independent variables to predict COVID-19 preprints' publication status (see ML_string_feature_engineering_abstract_temp.py)

* keywords approach - one-hot encoding
* gender
* institutional affiliations
* country
* university ranking
* etc.

2. Optimization of Logistic Regression's Hyperparameters (see cross__validation__v3.py)

3. Machine-Learning (see CORD_PP_ML_v2.py)

* Running Logistic Regression within a cross-validation framework
* Saving Model to be able to run it on the out-of-sample dataset
