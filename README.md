import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
dataset=pd.read_csv('https://student-datasets-bucket.s3.ap-south-1.amazonaws.com/whitehat-ds-datasets/uci-credit-card-fraud/UCI_Credit_Card.csv')
dataset
dataset.shape
dataset.isnull()
dataset['EDUCATION'].count()
type(dataset["EDUCATION"])
dataset=dataset[dataset['EDUCATION'].isnull()==False]
dataset
dataset.isnull().sum()*100/dataset.shape[0]
import seaborn as sns
plt.figure(figsize=(21,7))
sns.countplot(x='EDUCATION',data=dataset)
plt.grid()
plt.show()
dataset.info()
dataset['SEX'].count
dataset=dataset[dataset['SEX'].isnull()==False]
dataset
dataset['SEX'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='SEX',data=dataset)
plt.grid()
plt.show()
dataset['MARRIAGE'].count()
dataset=dataset[dataset['MARRIAGE'].isnull()==False]
dataset
dataset['MARRIAGE'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='MARRIAGE',data=dataset)
plt.grid()
plt.show()
dataset['PAY_0'].count()
dataset['PAY_5'].count()
dataset['PAY_5'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_5',data=dataset)
plt.grid()
plt.show()
dataset['PAY_6'].count()
dataset['PAY_6'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_6',data=dataset)
plt.grid()
plt.show()
dataset['default.payment.next.month'].count()
dataset['default.payment.next.month'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='default.payment.next.month',data=dataset)
plt.grid()
plt.show()
plt.figure(figsize=(10,5))
sns.boxplot(x='PAY_0',data=dataset)
plt.hist('PAY_0', bins = 6)
plt.show()
plt.figure(figsize=(10,5))
sns.boxplot(x='AGE',data=dataset)
plt.hist('AGE', bins = 6)
plt.show()
plt.figure(figsize=(10,5))
sns.boxplot(x='LIMIT_BAL',data=dataset)
plt.hist('LIMIT_BAL', bins = 6)
plt.show()
plt.hist('LIMIT_BAL', bins = 50)
plt.show()

dataset.loc[dataset['PAY_0'] < 0, 'PAY_0'] = 0 
dataset['PAY_0'].value_counts()
dataset['PAY_0'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_0',data=dataset)
plt.grid()
plt.show()
dataset['PAY_2'].count()
dataset['PAY_2'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_2',data=dataset)
plt.grid()
plt.show()
dataset['PAY_3'].count()
dataset['PAY_3'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_3',data=dataset)
plt.grid()
plt.show()
dataset['PAY_4'].count()
dataset['PAY_4'].isnull().sum()*100/dataset.shape[0]
plt.figure(figsize=(21,7))
sns.countplot(x='PAY_4',data=dataset)
plt.grid()
plt.show()

