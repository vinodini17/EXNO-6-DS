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
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/46974ab5-7fc7-40fb-a9b2-1616f16727bc)
```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/772058e7-b9c9-4946-af42-d4406deedba8)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/00076ba5-5f2a-4c33-9423-e06f766c1128)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```
![image](https://github.com/user-attachments/assets/3b9eb27a-c0b9-457f-a02f-8086f94e405f)
```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/ba675234-156c-4f40-ba00-b91adbf8c295)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/a8875910-e94e-4f61-9231-b3149c6b5c08)
```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image](https://github.com/user-attachments/assets/a1202464-30c2-4c24-8684-f980c4dc569d)
```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/064c936b-69b7-4b04-9139-92e04b3c7ddb)
```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```
![image](https://github.com/user-attachments/assets/75d93cfc-103e-4935-bb9b-529b7e02a18d)
![image](https://github.com/user-attachments/assets/0f6680c0-650a-4cb6-b7a3-9228272f82de)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/5aa1f428-1294-42a2-9696-3f54053a37ef)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town,Divided by Class")
```
![image](https://github.com/user-attachments/assets/52cf845e-40a3-498e-ae6f-77defcd62af5)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/4512ff1c-abe3-4d2f-97b9-81c67965af87)
```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```
![image](https://github.com/user-attachments/assets/a288772d-c3c9-489a-b964-fcea264cf95e)
```
sns.histplot(data=num_var,kde=True)
```
![image](https://github.com/user-attachments/assets/eb6e12be-8dc3-4375-a00b-69ee220fce25)
```
sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/user-attachments/assets/6411df41-8b23-4ce5-ba97-160d90cc6099)
```
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```
![image](https://github.com/user-attachments/assets/557baafa-c44d-46ab-b03d-0e01c5db5220)
```
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Student Marks')
```
![image](https://github.com/user-attachments/assets/cc753817-cd75-4cf9-9409-3dce7023c06f)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/b6550aa1-ea2c-4978-ae0e-cff9920d6325)
```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image](https://github.com/user-attachments/assets/206df3e2-54af-4abd-b2e5-a31311276f92)
```
sns.boxplot(x='Pclass',y='Age',data=tit,palette='rainbow')
plt.title("Age by Passenger Class,Titanic")
```
![image](https://github.com/user-attachments/assets/81ddc5a1-6823-479b-b360-fc21fc88eaa5)
```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/ab7e35ac-a698-4216-a3bb-dbff277f49bb)
```
import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
```
![image](https://github.com/user-attachments/assets/57d0dbbd-da57-48ba-a7fe-7e548ab2b107)
```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/48df3249-f2bc-4f44-8e33-7ed92a07dc8f)
```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x="tip",y="day",data=tip)
```
![image](https://github.com/user-attachments/assets/88ed24c3-72ab-41da-bc86-bc6cbb5424ab)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/db1d9b73-a36f-4782-bbc4-c242755e029a)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/ef326aa4-2bcc-4ab9-b274-b1855378c6cf)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/3ff8d8d7-8b00-4330-9ce5-d1a7cb4aad7e)
```
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
```
![image](https://github.com/user-attachments/assets/1fbe9442-4177-4a2f-84bd-ffd61ec0d776)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/d50fead1-94c9-42dd-8af8-544edc2673d5)
```
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```
![image](https://github.com/user-attachments/assets/3ce516bc-0d85-405f-b09e-a3709bff6ab2)

# Result:
 Data Visualization using seaborn python library for the given datas has been performed successfully.
