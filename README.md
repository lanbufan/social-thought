#  ADDING GENDER VARIABLE TO DATASET

##  CORD__pp_gender_abstract.py (master_ script)

* This py_script can create gender variables using human names. This script is abstracted enough to accomodate any column in a csv that contain lists of human names. In 2020 alone, I used this script to predict gender on more than 700, 000 first names. The master script accomplish the following task:

1. PARSE ALL LAST NAME FROM LIST OF AUTHORS (see get_au_last_name.py)

* from: Harvey, Raymond A.; Rassen, Jeremy A.; Kabelac, Carly A.; Turenne, Wendy
* to: ['Harvey', 'Rassen', 'Kabelac', 'Turenne']

2. PARSE ALL FIRST NAME FROM LIST OF AUTHORS (see GENDER_get_first_name_cur.py)

* from: Harvey, Raymond A.; Rassen, Jeremy A.; Kabelac, Carly A.; Turenne, Wendy
* to: ['Raymond', 'Jeremy', 'Carly', 'Wendy']

3. ASSIGN UNIQUE ID TO LAST NAME (see GENDER_assign_last_name_id.py)

* from: ['Harvey', 'Rassen', 'Kabelac', 'Turenne']
* to: [[1788, 'harvey'], [90250, 'rassen'], [104105, 'kabelac'], [104106, 'turenne']]

4. ASSIGN UNIQUE ID TO FIRST NAME (see GENDER_assign_first_name_id.py)

* from: ['Raymond', 'Jeremy', 'Carly', 'Wendy']
* to: [[3894, 'raymond'], [2099, 'jeremy'], [8961, 'carly'], [4990, 'wendy']]

5. ADD DUMMY VARIABLES FOR ANALYSIS (see WOS_GENDER_add_two_flags.py)

7. QUERY NAMSOR API TO GET GENDER DATA (see WOS_GENDER_namesor_api.py)

    subarna khatry return ==>

    {'first_name': 'subarna',
     'gender_scale': 0.9606992177969973,
     'id': None,
     'last_name': 'khatry',
     'likely_gender': 'female',
     'probability_calibrated': 0.9803496088984986,
     'score': 20.156151371724143}

8. POST-API QUERY - ADD GENDER VARIABLES TO TARGET DATASET (see GENDER_add_gender_variables.py)

* from: [[3894, 'raymond'], [2099, 'jeremy'], [8961, 'carly'], [4990, 'wendy']]
* to: [[3894, 'raymond', 'male'], [2099, 'jeremy', 'male'], [8961, 'carly', 'female'], [4990, 'wendy', 'female']]

* this script also add a number of key gender dummy variables: first_au_female_1 (is the first author female); last_au_female_1 (is the last author female), etc..

9. DETERMINATION OF GENDER ABOVE or BELOW CUT-OFF POINT (see GENDER_add_prop_dummy_cut_off.py)

* from: [[3894, 'raymond', 'male'], [2099, 'jeremy', 'male'], [8961, 'carly', 'female'], [4990, 'wendy', 'female']]
* to: [[3894, 'raymond', 'male', 0.995278343], [2099, 'jeremy', 'male', 0.99353481], [8961, 'carly', 'female', 0.910756111], [4990, 'wendy', 'female', 0.973693259]]

* flag_first_below (is the gender prediction probability for the first author 'raymond' above the cut-off point of 0.73, if yes, True; else False
* flag_last_below (is the gender prediction probability for the last author 'wendy' above the cut-off point of 0.73, if yes, True; else False
* etc...

10. EXAMPLE OF FINAL CORD-19 DATASET with FULL GENDER VARIABLES (see CORD_pp_to_pr_api_v74_training_set_all_nih_ror.csv)
