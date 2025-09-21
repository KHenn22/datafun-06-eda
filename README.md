# datafun-06-eda
Northwest Data Analytics Fundamentals Week 6

## Setup (clone, venv, install, verify) (2025-09-21)

Follow these commands on macOS (bash) to reproduce what I did: cloning the repo, creating a Python virtual environment, installing dependencies from `requirements.txt`, and verifying the installation.

```bash
# 1) Clone the repository (choose SSH or HTTPS)
# SSH (requires SSH keys configured):
git clone git@github.com:KHenn22/datafun-06-eda.git
# OR HTTPS:
git clone https://github.com/KHenn22/datafun-06-eda.git

# 2) Change into the project directory
cd datafun-06-eda

# 3) (Optional) Check Python version
python3 --version

# 4) Create a virtual environment (recommended name: .venv)
python3 -m venv .venv

# 5) Activate the virtual environment (bash)
source .venv/bin/activate

# 6) Install pip requirements
pip install -r requirements.txt

# 7) Verify installed packages
pip list
```

Notes:
- The `pip list` command prints installed packages in the active venv; that's how I verified packages were installed.
- If you used a different venv name, adjust the `source` path accordingly.
- To deactivate the venv when finished: `deactivate`.

## Data: titanic.csv

[titanic.csv](https://github.com/KHenn22/datafun-06-eda/blob/main/titanic.csv)

Description:

- `titanic.csv` is a passenger-level dataset used for introductory data analysis and classification. Each row represents one passenger on the RMS Titanic; the usual target column is `Survived` (0 = died, 1 = survived).


Columns (exact, from `/titanic.csv`):

| Column | Description |
|---|---|
| survived | Survival (0 = No, 1 = Yes) |
| pclass | Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| sex | Sex (male/female) |
| age | Age in years (may contain missing values) |
| sibsp | Number of siblings/spouses aboard |
| parch | Number of parents/children aboard |
| fare | Passenger fare |
| embarked | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| class | Textual passenger class (First/Second/Third) — derived/duplicate of `pclass` |
| who | High-level category (man/woman/child) |
| adult_male | Boolean indicating adult male |
| deck | Deck letter (often missing) |
| embark_town | Full name of embarkation town |
| alive | Textual survival ('yes'/'no') |
| alone | Boolean indicating whether passenger was alone |

 

## Data verification: titanic.csv (actual file)

Header / columns found in `/titanic.csv`:

```
survived,pclass,sex,age,sibsp,parch,fare,embarked,class,who,adult_male,deck,embark_town,alive,alone
```

First 10 data rows (as CSV):

```csv
0,3,male,22.0,1,0,7.25,S,Third,man,True,,Southampton,no,False
1,1,female,38.0,1,0,71.2833,C,First,woman,False,C,Cherbourg,yes,False
1,3,female,26.0,0,0,7.925,S,Third,woman,False,,Southampton,yes,True
1,1,female,35.0,1,0,53.1,S,First,woman,False,C,Southampton,yes,False
0,3,male,35.0,0,0,8.05,S,Third,man,True,,Southampton,no,True
0,3,male,,0,0,8.4583,Q,Third,man,True,,Queenstown,no,True
0,1,male,54.0,0,0,51.8625,S,First,man,True,E,Southampton,no,True
0,3,male,2.0,3,1,21.075,S,Third,child,False,,Southampton,no,False
1,3,female,27.0,0,2,11.1333,S,Third,woman,False,,Southampton,yes,False
1,2,female,14.0,1,0,30.0708,C,Second,child,False,,Cherbourg,yes,False
```

Notes:
- These columns include both the classic Kaggle columns and a few derived/extra columns like `class`, `who`, `adult_male`, `deck`, `embark_town`, `alive`, and `alone` which appear when using seaborn's `titanic` dataset or an augmented version.

