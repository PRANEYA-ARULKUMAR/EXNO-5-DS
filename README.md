# EXNO:5-DATA VISUALIZATION USING MATPLOT LIBRARY

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
REG NO: 212224110045
NAME: A PRANEYA
```
# LINE GRAPHS
```
import matplotlib.pyplot as plt
x_val = [0,1,2,3,4,5]
y_val = [0,1,4,9,16,25]
plt.plot(x_val,y_val)
plt.show()
```
![Screenshot 2025-04-18 191240](https://github.com/user-attachments/assets/f8ba6a5b-5801-42ef-971b-6aee171238e6)
```
import matplotlib.pyplot as plt
plt.plot(x,y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('GRAPH-1')
plt.show()
```
![Screenshot 2025-04-18 191346](https://github.com/user-attachments/assets/3b2cdc24-9eab-4a3e-b110-e9071ecda7ed)
```
import matplotlib.pyplot as plt
x1 = [1,2,3]
y1 = [2,4,1]
plt.plot(x1,y1,label = 'line 1')
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x2,y2,label = 'line 2')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title("Two lines in the Same Graph")
plt.legend()
plt.show()
```
![Screenshot 2025-04-18 191440](https://github.com/user-attachments/assets/6ea89271-bc1a-4ace-b4ab-a3b10491168d)
```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 1, 5, 2, 6]

plt.plot(x,y, color='green', linewidth=3, linestyle='--', marker = '*', markerfacecolor='orange', markersize=10)
plt.ylim(1, 8)
plt.xlim(1, 8)
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("Dotted Line")
plt.show()
```
![Screenshot 2025-04-18 191522](https://github.com/user-attachments/assets/7348247c-f630-4364-bc09-bdc2af3fe9e0)

```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 1, 5, 2, 6]
plt.subplot(2,2,1)
plt.plot(x,y,'r--')
plt.subplot(2,2,2)
plt.plot(y,x,'g*--')
plt.subplot(2,2,3)
plt.plot(x,x,'bo--')
plt.subplot(2,2,4)
plt.plot(x,y,'go')
```
![Screenshot 2025-04-18 191603](https://github.com/user-attachments/assets/c5fc6524-a82d-4014-9f93-dc12cec9cd91)

# SINE WAVE FORM
```
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
np.pi
x=np.arange(0,3*np.pi,0.1)
y=np.sin(x)
plt.title("SINUSOIDAL WAVE")
plt.plot(x,y)
plt.show()
```
![Screenshot 2025-04-18 191751](https://github.com/user-attachments/assets/b5769284-1099-405a-b53e-906a707d0dd5)

# SCATTER PLOT
```
import matplotlib.pyplot as plt

x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]

plt.scatter(x_values, y_values, s=30, color="red")
plt.show()
```
![Screenshot 2025-04-18 191913](https://github.com/user-attachments/assets/542755c1-e4eb-440f-a155-1021e1f3d7b1)

# AREA CHART
```
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd

x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]

plt.fill_between(x,y1,color="pink")
plt.legend(['y1'])
plt.show()
```
![Screenshot 2025-04-18 192020](https://github.com/user-attachments/assets/8f515430-2687-40e2-a65f-aa4921d73d36)

# STACKED AREA CHART
```
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5,7,9,11,13]
y3 = [2,4,6,8,10]
plt.stackplot(x,y1,y2,y3,labels = ['Y1','Y2','Y3'])
plt.legend(loc = 'upper left')
plt.title('Stacked AREA Chart')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.show()
```
![Screenshot 2025-04-18 192401](https://github.com/user-attachments/assets/74dbfdc1-318f-4c82-b92c-39f33b848317)

# SPLINE CHART
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])
x_smooth = np.linspace(x.min(), x.max(), 300)
spline = make_interp_spline(x, y)
y_smooth = spline(x_smooth)
plt.figure(figsize=(8, 5))
plt.plot(x, y, 'o', label='Original Data')
plt.plot(x_smooth, y_smooth, label='Cubic Spline Interpolation')
plt.title("Cubic Spline Interpolation")
plt.xlabel("X-AXIS")
plt.ylabel("Y-AXIS")
plt.legend()
plt.show()

```
![Screenshot 2025-04-18 192640](https://github.com/user-attachments/assets/16f46b73-3821-4e5b-9acd-c7b42dd1d519)

# BAR GRAPHS
```
import numpy as np
import matplotlib.pyplot as plt
val = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
plt.bar(names, val,color = 'pink')
plt.show()
```
![Screenshot 2025-04-18 192824](https://github.com/user-attachments/assets/94356f15-0a67-4103-8385-1821437ab237)
```
import matplotlib.pyplot as plt
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
colors = ['b', 'g', 'b', 'g', 'b']
plt.figure(figsize=(8, 5))
plt.bar(names, values, color=colors)
plt.title("Bar Chart")
plt.xlabel("Categories")
plt.ylabel("Values")
plt.tight_layout()
plt.show()
```
![Screenshot 2025-04-18 193004](https://github.com/user-attachments/assets/08cbbe0c-25fd-437f-9105-5ef9807693e6)

```
import matplotlib.pyplot as plt

x = [2, 8, 10]
y = [11, 16, 9]
x2 = [3, 9, 11]
y2 = [6, 15, 7]

plt.bar(x,y,color="r")
plt.bar(x2,y2,color="b")
plt.title("Bar graph for 2 features")
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
```
![Screenshot 2025-04-18 193123](https://github.com/user-attachments/assets/47e34ea7-1a4f-48db-857f-ec07eecef682)

# HISTOGRAM
```
import matplotlib.pyplot as plt
import numpy as np
ages = [2,6,4,12,13,12,16,18,18,19,26,24,39,34,45,42,54,56,90,56,86,79]
range = (0,100)
bins = 10
plt.hist(ages,bins,range,color='brown',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('no of people')
plt.title('histogram')
plt.show()
```
![Screenshot 2025-04-18 193513](https://github.com/user-attachments/assets/18fa0c80-ae6f-4fc4-9e14-bd9ae70c3eda)

# BOX PLOT
```
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![Screenshot 2025-04-18 193625](https://github.com/user-attachments/assets/e13aded9-f94f-48bf-8079-668c1dc85d2f)
```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel("data")
ax.set_ylabel("values")
ax.set_title("box plot")
```
![Screenshot 2025-04-18 193700](https://github.com/user-attachments/assets/c9adae9b-3ff5-4b70-a989-7ee0a08f4760)

# PIE CHART
```
import matplotlib.pyplot as plt
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
colors=['r','y','g','b']
plt.pie(slices,labels = slices,colors=colors,startangle=90,shadow = True,explode = (0,0,0.1,0),radius=1.2,autopct='%1.1f%%')
plt.legend()
plt.show()
```
![Screenshot 2025-04-18 193759](https://github.com/user-attachments/assets/6990fa93-14f9-4692-863c-ae7b6157bf16)

# Result:
Thus the data visualization using matplot python library for the given datas are performed successfully.
