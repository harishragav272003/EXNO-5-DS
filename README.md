# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
NAME : Harish Ragav S
REG NO : 212222110013
```

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```

## Line Plot:

```
marks=[13,45,63,78]
student=['ABC','QOR','EFB','TOB']
plt.plot(marks,student)
plt.xlabel('Marks')
plt.ylabel('Student name')
plt.show()

student=['A','B','C','D']
attendence=[90,85,73,88]
plt.plot(attendence,student)
plt.xlabel('Attendence')
plt.ylabel('Student name')
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/915713f5-50b1-4013-8037-3a9cc599f291)

## Scatter Plot:

```
x=[10,20,30,40,50]
y=[100,200,300,400,500]
plt.scatter(x,y,label='stars',color='green',marker='*',s=30)
plt.show()

x=np.arange(0,15)
y=np.arange(0,15)
x
y
plt.scatter(x,y,c='r')
plt.xlabel('X axis')
plt.ylabel('y axis')
plt.title('Scatter plot')
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/7fab8701-3aee-4b5a-b729-cb82a6c2dd16)

## Pie Chart:

```
act=['eat','sleep','work','play']
slices=[3,7,8,6]
color=['r','y','g','b']
plt.pie(slices,labels=act,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,autopct='%1.1f%%')
plt.legend()
plt.show()

feedback=['Good','excellent','Perfect','Ok']
slices=[4,10,3,8]
color=['y','r','b','g']
plt.pie(slices,labels=feedback,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,autopct='%1.1f%%')
plt.legend()
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/a16d81be-4162-41f0-ba84-7d43883c3248)

## Area Chart:

```
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]
plt.fill_between(x, y1, color='blue')
plt.fill_between(x, y2, color='green')
plt.plot(x, y1, color='red')
plt.plot(x, y2, color='black')
plt.legend(['y1','y2'])
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/9d90b6c9-70ac-4f52-bec1-975fafa4afc7)

## Bar Chart:

```
height = [10, 24, 36, 40, 5]
names = ['one', 'two', 'three', 'four', 'five']
c1=['red', 'green'] 
c2=['b', 'g']
plt.bar (names, height, width=0.8, color=c1)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My bar chart!')
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/6685a45c-7ed2-44c4-8730-3a2e55acf7e3)

## Histogram:

```
x = [2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x, bins = 10, color='blue', alpha=0.5)
plt.show()
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/c7d07305-db41-438c-8585-81346fead120)

## Box Plot:

```
np.random.seed(0)
data=np.random.normal(loc=0, scale=1, size=100)
data
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/1073572a-2c3a-487c-a1b8-efdbc595ac91)

```
fig, ax= plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```
![image](https://github.com/Sriram8452/EXNO-5-DS/assets/118708032/3e04e28b-5a0e-412e-ad52-ecda68c69561)



# Result:

Thus, all the data visualization techniques of matplotlib has been implemented.
