# EX:5 DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
### TO CAPTURE A TREND
### 1.Line Chart
```python
import matplotlib.pyplot as plt
import numpy as np
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.plot(x,y)
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/7b7bfc97-6d33-40a5-b031-dbd060d931d9)


### 2.Multi-Line Chart
```python
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label="line 1")
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Multi-Line Chart')
plt.legend()
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/b2f14ede-d3bd-4295-92bc-b76064150236)


### 3.Area Chart
```python
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/4a58ad27-98c2-4c6a-bf94-2e80cf9ee96b)


### 4.Stacked Area Chart
```python
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/a1daf8ae-650f-4313-9fe6-d770c5b6d13f)


### 5.Spline Chart
```python
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x1=np.linspace(x.min(),x.max(),100)
y1=spl(x1)
plt.plot(x,y,'*',label='data')
plt.plot(x1,y1,'-',label="spline")
plt.legend()
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/adf1a737-1098-4028-bf99-1bc5efb75c21)


### TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```python
val=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,val,color="blue")
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/84f11c03-1bc6-4c28-898b-28abb77c6f18)


### 2.Scatter Plot
```python
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.scatter(x,y,s=30,color="red")
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/d55773ad-64d8-46b5-8a44-3ecbb768bb34)


### 3.Bubble Chart
```python
x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 25, 30]
sizes = [100, 200, 300, 400, 500]
plt.scatter(x, y, s=sizes, alpha=0.5)
plt.xlabel('x_values')
plt.ylabel('y_values')
plt.title('Bubble Chart')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/627e553e-2838-4c39-bbc4-f0645245409c)


### TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```python
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='purple',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. Of People')
plt.title('Histogram')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/b6ecd88c-5393-4367-8381-d89738a75eed)


### 2.Box Plot
```python
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/a73b215f-1868-4e20-b805-5bb772cfa9c3)


### 3.Violin Plot
```python
data = [np.random.normal(loc=0, scale=1, size=100),
        np.random.normal(loc=2, scale=1, size=100),
        np.random.normal(loc=1, scale=2, size=100)]
plt.violinplot(data)
plt.xlabel('Groups')
plt.ylabel('Values')
plt.title('Violin Plot')
plt.xticks([1, 2, 3], ['Group 1', 'Group 2', 'Group 3'])
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/9d67082a-c9b1-498f-b4ed-4456a1b00307)


### 4.Density Chart
```python
data = np.random.normal(0, 1, 1000)
plt.hist(data, bins=30, density=True, alpha=0.5)
plt.title('Density Plot Example')
plt.xlabel('Values')
plt.ylabel('Density')
from scipy.stats import gaussian_kde
kde = gaussian_kde(data)
x_vals = np.linspace(min(data), max(data), 1000)
plt.plot(x_vals, kde(x_vals), 'r')
plt.show()
```

![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/abde6e32-0b72-4aa6-a290-b43d94292501)


### 5.Pie Chart
```python
act=['eat','sleep','work','play']
slices=[3,7,8,6]
color=['r','y','g','b']
plt.pie(slices,labels=act,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,
autopct='%1.1f%%')
plt.legend()
plt.show()
```

![image](https://github.com/chandrumathiyazhagan/EXNO-5-DS/assets/119393023/b4d24a1c-9c1f-4d5c-bf27-564e540a1cdc)


# Result:
  The Data Visualization using matplot python library is implemented successfully.

