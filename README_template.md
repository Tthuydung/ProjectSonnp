# Customer Churn Exploration

## Description

Predict behavior to retain customers. 
One can analyze all relevant customer data and develop focused customer retention programs.

## Environment set up

Change directory to project folder, and start with create and activate virtual environment
```bash
python3 -m venv venv  # create virtual environment in ./venv
source venv/bin/activate  # activate virtual environment
```

Install packages in environments.  
 ***IMPORTANT***: install packages, kernels when inside the virtual environment
```bash
(venv) pip3 install pip3 -U  # get latest version of pip
(venv) pip3 install ipykernel  # install ipykernel
(venv) ipython kernel install --user --name [PROJECT-NAME] --display-name [PROJECT-NAME]
```
Refresh and create new notebook using project kernel

To manage the ipykernel, consider following commands:
```bash
jupyter kernelspec list  # to show available kernels
jupyter kernelspec uninstall [KERNEL-NAME]  # to uninstall a kernel
```

## Data Acquisition

### Data set 1:
- Source: https://www.kaggle.com/pavanraj159/telecom-customer-churn-prediction/data
- Server location: `./data/raw/telecom-churn`
- About: 
    - Each row represents a customer, each column contains customer’s attributes described on the column Metadata.
    - Customers who left within the last month – the column is called Churn. Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies. 
    - Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges. 
    - Demographic info about customers – gender, age range, and if they have partners and dependents

### Data set 2:
- Source: https://www.kaggle.com/c/churn-analytics-bda/data
- Server location: `./data/raw/churn-analytics-bda`
- About: 
    - Data from kaggle competition 
    - 3 files: `train.csv`, `test.csv`, `sampleSubmission.csv`
    
### Data set 3:
- Source: https://www.kaggle.com/kmalit/bank-customer-churn-prediction/data
- Server location: `./data/raw/bank-customer-churn`
- About: 
    - Data from kaggle notebook 

## Data Exploration 

Summarize the data information here or link to a notebook in `notebook/data_exploration_number.md`

Here are the steps we agreed to work on:
- number of rows/columns
- number of categorical/numerical data
- check for missing values
- box plots, histogram and density plots, correlation matrix for numerical columns
- bar graphs for categorical columns
- summary 
All analysis should be applied to whole data set, churn data set and non-churn data set.

Notebook links once merged:
- [notebook1](url)
- [notebook2](url)
- [notebook3](url)

### Conclusion:
- Final dataset: dataset 2
- Columns:
    - Phone_No: set_index
    - Keep all columns in the initial    
- Data preparation steps:
    - State: convert to int 
    - Area_Code: convert to int 
    - Integer columns: leave as is, might apply min-max scaler
    - Keep minutes columns
    - Create total_charge column
  
## Data Preparation 

Summarize the data preparation steps here or link to a notebook in `notebook/data_preparation_number.md`
- [notebook1](url)
- [notebook2](url)

## Data Taggling/Labelling

Any specific taggling should be noted here or link to a notebook in `notebook/notebook_name.md`
- This step is not available in this project.

## Model selection 

Summarize a list of candidate models here 

Link to a notebook in `notebook/notebook_name.md`
- [notebook1](url)
- [notebook2](url)

Results

|Model   |Missing-value handling method   |Accuracy   |
|---|---|---|
|RandomForest   |Emperical mean estimator on train set   |96.941%   |
|RandomForest   |Rule-based   |97.647%   |


## Model training

Start move to `./src/training`

Go back to `Environment set up` and repeat the steps 

Add `README.md` to src to show steps to prepare training

Transfer notebooks from previous steps to executable `*.py` scripts

## Model wrap-up

Create a file in `./src/training/to_deploy.md` containing:

- Architecture requirements
- Package requirements
- Scripts, data and model to bring to deployment


## Model deployment

Start move to `./src/deploy`

Set up:
```
./src/deploy
    venv/
    model/
    requirements.txt 
    scripts.py 
``` 
