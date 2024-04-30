# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/f42cc101-956d-4574-bc55-a885374da77f)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/c8f8350c-fd76-449d-87dd-2df5caeebaa4)


```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/726ff35e-a206-427f-9007-65d317fe5260)


```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/05d0f36c-971e-4a8a-91d1-a2aba344762b)


```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/f2ed01e6-3434-4f6a-a488-96630dfdcbea)


```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/0d995601-c2de-4346-a14d-fc9faa6b6e5d)


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/e6b465a1-3439-4056-98f4-3d5b0b61c569)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/52feab25-9b27-478a-bbf3-a0024374a53e)


```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/b931f6ff-6631-42ef-803a-7b65ebcefab6)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/ed67c31f-de8b-4f50-a640-f28d30c35610)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/a91b271d-7b02-4993-9f41-8ea322e835ef)



```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/b6cf7881-c9fb-49fc-a30d-4b0b3bab56af)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/52e46cb8-07c3-4a3f-bf6b-f764bbe87af6)



```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/e9b92c21-09a6-4afb-90f5-cb454affec99)



```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/f75863ee-fa6d-4b2e-8609-e02462ffa863)


```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/4097d312-252b-451f-a7d8-5c36fc38584e)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/1220d483-7bce-4a24-9007-c9711f31af9b)


```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/4e5fcd5c-10da-4236-b90e-5d8acca14d98)



```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/f1cad486-b5c0-4149-a49a-30b22a962038)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/f66afee1-ec18-4a70-b526-c338b6c6aed8)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/241e1d24-59aa-4d4e-8116-7272a7235b72)


```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/3c6d016b-f167-4fec-9dd1-1fee23e01608)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/8f04d7d2-feb2-47d3-85eb-77e4d0286643)


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/78a0c5cb-8374-4616-ab17-68e96a1f2577)


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/426a00b4-1e34-40ff-8cff-3981cba1aedf)


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/7d50ff83-9eb3-48ea-b213-8153cdbaaf33)


```
hm=sns.heatmap(data=data)
```
![image](https://github.com/Ranjanranjan/EXNO-6-DS/assets/130027697/99673445-67d8-4132-86e7-744035961498)


# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
