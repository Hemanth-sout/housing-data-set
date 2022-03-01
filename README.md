# housing-data-set
BIG DATA
import pandas as pd

data = pd.read_csv(r"C:\Users\dell\Downloads\Boston.csv")

data

data.head()

# count 

data.count()

data.isnull().sum()

import seaborn as sns
import matplotlib.pyplot as plt

sns.heatmap(data.isnull())

# converting columns names

data.head()

data.data = pd.to_taxdata(data.tax)
#if the column is object type  code works 



data.dtypes

# to add year from suparating from date

data.head()

data['year'] = data.CRIM.dt.year
#there is no date column sso no chnages but the syntax is the above to suparate year from date 

# to add month column suparating from year 

data.insert(1, 'month', data.date.dt.month)
#there is no date column sso no chnages but the syntax is the above to suparate year from date 

# removing columns

data.head()

data.drop(['ZN','DIS'],axis=1)

data.drop(['ZN','DIS'],axis=1,inplace = True)

data.head()

# filtering ,show the indus is 2.31 and how many are there 

data.head()

data.INDUS == 2.31

data[data.INDUS == 2.31]

#to find the number of indus add length functuions 

len(data[data.INDUS == 2.31])

# max and min 

data.head()

data.groupby('TAX').min()

data.groupby('TAX').max()

# lesser and greater

data[data.TAX<216]


data[data.TAX>216]


