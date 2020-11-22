# DataSciencePython

# Descriptive Data Analysis

## IMPORTS AND MERGE
Before we analyze anything, we need to import pandas. Data can be loaded from CSV files:

import pandas as pd

first we are dealing with two source. let's merge them to have an unique file. Merge is a panda's method:

df_train = pd.read_csv(r"C:\Users\Max\Documents\Python\train.csv", low_memory=False)
df_store = pd.read_csv(r"C:\Users\Max\Documents\Python\store.csv", low_memory=False)

#merge
df_raw = pd.merge(df_train, df_store, how="left", on='Store')

#printing the result
df_raw.sample()

## EXAMINATING DATA
 Data stored, now we can examine the columns and rows of the file. It shows the first Twenty rows and columns:
 
 df_raw.head(20)
 we can select a specific line using lists:

 df_raw[(df_raw.Customers > 555) & (df_raw.CompetitionDistance > 500.0)]
 
 
