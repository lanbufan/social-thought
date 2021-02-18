# social-thought
social scientist working on history and sociology of science, big data, mix-methods

#  CORD-19 Preprint Project

## Data Cleaning Procedure

1. "CORD_PP_TO_PR_script_execution_master_data_cleaning.py"

* This py_script clean the raw version of CORD-19 csv and render it in a clear format usable for the record-linkage of COVID-19 preprints with their final published versions. This master script execute the following tasks:

* **REMOVE publications without article title

* REMOVE publications published before 2019

* REMOVE non-COVID-19 publications using a set of keywords

* *REMOVE publications that are not articles 
