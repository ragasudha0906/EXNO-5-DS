### EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

### Aim:
  To Perform Data Visualization using matplot python library for the given datas.

### EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

### Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

### Coding and Output:
# Line plot
```
import matplotlib.pyplot as plt
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.plot(x,y)
```
<img width="755" height="436" alt="i1" src="https://github.com/user-attachments/assets/4681e223-bc97-4e0a-af3a-c3657d082188" />

```
x_=[1,2,3]
y_=[2,4,1]
plt.plot(x_,y_)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('First Graph')
```
<img width="734" height="482" alt="i2" src="https://github.com/user-attachments/assets/50bf1a38-ba75-427e-ab6f-f374b183f4be" />

```
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1, label="line1")
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')
plt.legend()
```
<img width="799" height="480" alt="i3" src="https://github.com/user-attachments/assets/6d167a0c-c388-4d0e-bbca-abcad0afde53" />

```
xx=[1,2,3,4,5,6]
yy=[2,4,1,5,2,6]
plt.plot(xx,yy,color='blue',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='red',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Customized Graph')
```

<img width="782" height="476" alt="i4" src="https://github.com/user-attachments/assets/d53f4ad8-c719-4536-b0da-cafd1bc726f9" />

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.plot(years,apples)
plt.plot(years,oranges)
plt.xlabel('Year')
plt.ylabel('Tield(tons per hectare)');
plt.title("Crop Yields in Kanto")
plt.legend(['Apples','Oranges']);
```

<img width="823" height="470" alt="i5" src="https://github.com/user-attachments/assets/a8610c85-44a5-4e46-935b-ed83a1418c0e" />

```
plt.plot(years,apples,marker='o')
plt.plot(years,oranges,marker='x')
plt.xlabel('Year')
plt.ylabel('Tield(tons per hectare)');
plt.title("Crop Yields in Kanto")
plt.legend(['Apples','Oranges']);
```

<img width="926" height="458" alt="i6" src="https://github.com/user-attachments/assets/51a26fbf-eeb3-42f9-8cb0-5c534d93fbf9" />

# Scatter plot

```
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.scatter(x_values,y_values,s=30,color='blue')
```
<img width="889" height="447" alt="i7" src="https://github.com/user-attachments/assets/62191d2a-3db7-4b3d-9436-09d69de2ed10" />

```
import numpy as np
import pandas as pd
x=np.arange(0,10)
y=np.arange(11,21)
print(x)
print(y)
plt.scatter(x,y,c='r')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Graph in 2D')
plt.savefig('Test.png')
```
<img width="1021" height="499" alt="i8" src="https://github.com/user-attachments/assets/8e868ab4-1a60-4e39-8d4e-cba16426ea00" />

```
y=x*x
print(y)
```
```
plt.plot(x,y,'g*',linestyle='dashed',linewidth=2,markersize=12)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('2D Diagram')
```
<img width="955" height="477" alt="i9" src="https://github.com/user-attachments/assets/5d267583-bbc8-449c-863b-608033d246ba" />

```
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("sine wave form")
plt.plot(x,y)
plt.show()
```
<img width="1020" height="450" alt="i10" src="https://github.com/user-attachments/assets/8b6dc92f-fc20-4596-bdb2-1c467e0b4dc6" />

```
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
<img width="882" height="425" alt="i11" src="https://github.com/user-attachments/assets/15a22738-23e4-4596-bb08-78d7eef2f950" />

```
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spl(x_smooth)
plt.plot(x,y,'o',label='data')
plt.plot(x_smooth,y_smooth,'-',label='spline')
plt.legend()
plt.show()
```
<img width="971" height="419" alt="i12" src="https://github.com/user-attachments/assets/8f9ffe86-4ce3-49a4-b453-c088e9960ec6" />

```
height=[10,24,36,40,5]
names=['one','two','three','four','five']
c1=['red','green']
c2=['b','g']
plt.bar(names,height,width=1,color=c2)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My bar chart')
```
<img width="973" height="470" alt="i13" src="https://github.com/user-attachments/assets/7dc1b115-92b4-4a5c-9f59-b4c317d2d616" />

```
x=[2,8,10]
y=[11,16,9]
x1=[3,9,11]
y1=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x1,y1,color='b')
plt.title('Bar Graph')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
<img width="1033" height="443" alt="i14" src="https://github.com/user-attachments/assets/f45e2871-9b92-4257-892f-cdde6e4b0725" />

```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. of people')
plt.title('My histogram')
```

<img width="888" height="455" alt="i15" src="https://github.com/user-attachments/assets/672173ec-67aa-4f07-9ace-157b3d6af276" />

```
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='blue',alpha=0.5)
plt.show()
```

<img width="986" height="417" alt="i16" src="https://github.com/user-attachments/assets/2700c4f5-f760-401f-97a7-ad0d26c78edd" />

```
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
print(data)
```

<img width="821" height="458" alt="i21" src="https://github.com/user-attachments/assets/7033744b-0dd2-4355-955d-d825ec78efd0" />

```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```

<img width="1032" height="475" alt="i17" src="https://github.com/user-attachments/assets/0fa0fc4f-ba27-4830-a8d0-8958bd7ef420" />

```
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
colors=['y','b','r','g']
plt.pie(slices,labels=activities,colors=colors,startangle=90,shadow=True,explode=(0,0,0.1,0),radius=1.0,autopct='%1.1f%%')
plt.legend()
```

<img width="1017" height="411" alt="i18" src="https://github.com/user-attachments/assets/894720a5-a795-417e-9614-68cd85f7c941" />

```
labels='Python','C++','Ruby','Java'
sizes=[215,130,245,210]
colors=['gold','yellowgreen','lightcoral','lightskyblue']
explode=(0,0.4,0,0.5)
plt.pie(sizes,explode=explode,labels=labels,colors=colors,autopct='%1.1f%%',shadow=True)
plt.axis('equal')
```
<img width="977" height="460" alt="i19" src="https://github.com/user-attachments/assets/3905f7dd-7285-4e63-9a56-c53c0e03aeb0" />

```
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
colors=['r','y','g','b']
plt.pie(slices,labels=activities,colors=colors,startangle=90,shadow=True,explode=(0,0,0.1,0),radius=1.2,autopct='%1.1f%%')
plt.legend()
```
<img width="874" height="429" alt="i20" src="https://github.com/user-attachments/assets/5baabe0b-ce59-4036-b7aa-863714bcf8f0" />


### Result:

   This experiment provided a comprehensive understanding of how the Matplotlib library can be utilized to create various graphical representations of data. By implementing different visualization techniques such as line plots, scatter plots, bar charts, histograms, and pie charts, the importance of visual analysis was clearly demonstrated. These tools make it easier to interpret large datasets, uncover hidden patterns, and communicate insights effectively. Overall, Matplotlib proved to be a versatile and efficient library for visualizing data in Python.
