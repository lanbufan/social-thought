#  CORD-19 Preprint Project

## Data Cleaning Procedure

### "CORD_PP_TO_PR_script_execution_master_data_cleaning.py" (master script)

* This py_script clean the raw version of CORD-19 csv and render it in a clear format usable for the record-linkage of COVID-19 preprints with their final published versions. This master script execute the following tasks:

1. REMOVE publications without article title (see in master script)

2. REMOVE publications published before 2019 (see CORD_filter_year_vx.py)

3. REMOVE non-COVID-19 publications using a set of keywords (see CORD_filter_covid_kw_vx.py)

4. REMOVE publications that are not articles (see in master script)

5. IDENTIFY PREPRINTS in the corpus of COVID-19 publications (see CORD_adhoc_pp_identification.py)

7. REPAIR WHO METADATA (see CORD_pp_coverage_nih_abstract.py)

8. ADD PREPRINTS from NIH iSearch dataset

9. REMOVE DUPLICATES (see CORD_filter_duplicate_cur.py)

10. REMOVE non-english language publications (see CORD_filter_lang_vx.py)

11. FIX ARXIV_ID (see CORD_fix_arxiv_id.py)

12. REMOVE PREPRINTS from other sources(see in master script)

13. CREATE FINAL CORD-19 CSV(see in master script)
