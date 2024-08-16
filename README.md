# Python_Diwali_Sales_Analysis

Python project for beginners- Analyze Diwali sales data to improve customer experience and sales

<<<<<<<<<<<
Diwali Data Analysis by python

pip install jupyter

jupyter notebook

localhost:8888/tree

https://jupyter.org/try-jupyter/edit/?path=untitled.py

import numpy and other library

df= pd.read_csv(r'file_[ath',encoding='unicode_escape'

read the csv file

df.shape --tell 1000 rows and 15 columns

df.head() top 5 rows andisplay wished rows

#>>>>>>>>>>>>data cleaning<<<<<<<<<

df.info()--information howmany rows and columns datatype(int,obj,float), count of null and not null

>>drop unwanted, unnamed column

df.drop(status, 'unnamed columsn') -- will delete the unwanted columns

df.isnull(df) --check the null value gives false for not null and true for null

>>drop null values NaN,None

df.dropna(inplace=True)--will delete all null rows and inplace for save

>>change data type float to int

df['amoun'].astype('int')

>>list of columns

df.columns

>>change the column rename column

df.rename(column={'maritail_status' : 'shaadi'})

>>describe() method return description of the data in dataframe(i.e count, min, max, std, 25%, 50%, 75%)

df.describe()

df[['age', 'orders']].describe() --describe the columns

#exploratory data ana;ysis

gender column exploring

sns is seaborn

>>display the chart of geneder count

sns.countplot(x = 'gender', data = df')

>>for values of count m and f in gender

ax = sns.countplot(x = 'gender', data = df')

for bars in ax.containers:
         ax.bar_label(bars)

>>group by gender and sum amount and sort amount in asc

df.groupby(['Gender'], as_index=False)['amount'].sum().sort_values(by = 'amount', ascending=False)

sales_gen=df.groupby(['Gender'], as_index=False)['amount'].sum().sort_values(by = 'amount', ascending=False)

sns.barplot(x = 'gender', y = 'amount', data = sales_gen)



