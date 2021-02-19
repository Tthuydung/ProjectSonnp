# ProjectSonnp
import numpy as np 
import pandas as pd 
df_trans = pd.read_csv('transactions.csv')
df_trans.shape
df_trans.head()
df_trans.tail()
df_trans['transactions'].describe()
trans_columns = df_trans.columns.tolist()

for i in range(0, len(trans_columns)):
    print("***",trans_columns[i],"***")
    print(df_trans[trans_columns[i]].nunique(),'개')
    print(df_trans[trans_columns[i]].value_counts(normalize=False))
    
