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

