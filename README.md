#  CORD-19 Preprint Project

## Data Cleaning Procedure

### "CORD_PP_TO_PR_script_execution_master_data_cleaning.py"

* This py_script clean the raw version of CORD-19 csv and render it in a clear format usable for the record-linkage of COVID-19 preprints with their final published versions. This master script execute the following tasks:

1. REMOVE publications without article title

2. REMOVE publications published before 2019

3. REMOVE non-COVID-19 publications using a set of keywords

4. REMOVE publications that are not articles

5. IDENTIFY PREPRINTS in the corpus of COVID-19 publications

7. REPAIR WHO METADATA

7. ADD PREPRINTS from NIH iSearch dataset

8. REMOVE DUPLICATES 

9. REMOVE non-english language publications

10. FIX ARXIV_ID

11. REMOVE PREPRINTS from other sources

12. CREATE FINAL CORD-19 CSV
