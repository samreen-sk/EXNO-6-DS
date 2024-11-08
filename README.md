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
![323212197-18a0f3c8-10a6-42b4-9eb3-45770f741ac3](https://github.com/user-attachments/assets/9212937d-8778-4296-b8bc-fc53857606b1)
```
df = sns.load_dataset("tips")
df
```
![323212387-0124fef5-dcba-4c31-9831-db85384d9c5a](https://github.com/user-attachments/assets/c367ff53-e877-45de-b06f-f0028e2efeba)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![323212532-1bbe2d28-735c-4114-aff7-9030d334c830](https://github.com/user-attachments/assets/4f0a534e-8194-4e95-ae56-6eb4db8113ad)

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
![323212649-4d6c2a15-2352-4ba4-bd6b-97a54cd93ce7](https://github.com/user-attachments/assets/bac1a88b-31ab-4d1a-8958-724eb9027671)

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
![323212764-86b30955-7bb2-44af-92d1-39e8be4b56ea](https://github.com/user-attachments/assets/af50e171-15d4-42f8-9275-d324b3d31133)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![323212867-27a32e9f-e734-4f47-adf1-bafddba998c3](https://github.com/user-attachments/assets/f1cb22f3-e4e0-4ec0-b39c-26ecbecc1089)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![323213027-31f5b45b-5a80-4259-a259-a4cecee25ee5](https://github.com/user-attachments/assets/b5c9ab29-cd28-46cb-9406-9caf2e6f7d97)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![323213184-359daca3-3920-4c78-b593-7d660c09cc36](https://github.com/user-attachments/assets/e14f0c2f-9f21-4e3d-b1e0-70cf3889bbe1)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![323213349-b749f1ee-b0a6-4a67-a340-f9cae8a8290a](https://github.com/user-attachments/assets/08dd8ffd-8df4-4fde-ba98-3c5d21507d52)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```

![323213630-03dbd087-2a3e-4bfa-8847-bc2e9bbe7cc3](https://github.com/user-attachments/assets/9f067f5d-2289-4396-a1e6-87f44ff0e60e)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![323213737-090114ac-6d91-4117-80ca-2bb2fe72af26](https://github.com/user-attachments/assets/96423be1-ae5b-436c-8088-1b84d92a64f0)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![323213860-b7984ccc-60c8-4cf2-ba31-0dafe6119b91](https://github.com/user-attachments/assets/f39a6bce-6a45-42a3-8940-3852871221bc)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![323213974-5e149370-320f-4c4b-b6e9-93839011d166](https://github.com/user-attachments/assets/b70f95c3-a259-4c33-a7d9-cebb8171898b)

```
sns.histplot(data = num_var, kde = True)
```

![323214138-39b3d5fa-e8af-45f5-afb2-2875c766a5e6](https://github.com/user-attachments/assets/c9f47666-fdd7-4cc3-8b98-b8f2178136b7)


```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![323214244-e8b91ede-1cc0-4087-beb6-c3c56d8137ee](https://github.com/user-attachments/assets/7a63e3ec-8c0a-490d-81df-36c228754eda)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![323214357-c7d0ff3a-e9a0-4369-a9c9-9229d84776c3](https://github.com/user-attachments/assets/7aa0ac07-ddc3-4d3a-a400-cf174db70fc4)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![323214462-dc5777c4-83cf-47d2-ba0c-b6bb81547441](https://github.com/user-attachments/assets/34cebb44-3f2b-4603-b968-ffede13f8f7d)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![323214570-8dec8878-d0bb-46ca-bc17-095aba86cffd](https://github.com/user-attachments/assets/986c3854-d3b7-4a5e-ac76-3ab6e12d184c)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

![323214740-32c63c42-35dc-47df-b851-c13e54c166aa](https://github.com/user-attachments/assets/6c694981-557b-413d-afdd-a32f3d57d3e2)


```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![323214850-bcbe61b9-5739-4853-a186-302272133266](https://github.com/user-attachments/assets/1e90ee4d-5d67-43ea-bdd3-a5097130824d)

```
sns.kdeplot(data=mart,x='PassengerId')
```

![323214956-727482e0-5b45-47e4-8542-93ebc9cfb5b7](https://github.com/user-attachments/assets/c9f43d05-f618-483f-b646-32b175c1e480)

```
sns.kdeplot(data=mart,x='Age')
```
![323215089-9bb955c9-ba97-48ab-b158-35a44931ccf6](https://github.com/user-attachments/assets/d6e413a3-227f-4aee-aa27-f74266bd2a9b)

```
sns.kdeplot(data=mart)
```
![323215191-8cc57d95-8df2-4483-8c98-2edbcfb68b0c](https://github.com/user-attachments/assets/600cff35-ba26-465d-8a11-2ab3ce29ff50)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![323215343-f56e128b-5393-46e8-acb6-33bfd6fde4a9](https://github.com/user-attachments/assets/ce796ae8-4efc-4850-9f3c-a253d4af539e)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![323215571-4f66d13f-770e-4b17-b29d-74f42cb4395e](https://github.com/user-attachments/assets/d4ad5574-f086-473a-9cce-81ca66a6f4f1)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![323215754-5eba9f52-3c11-4640-b78f-451463d24415](https://github.com/user-attachments/assets/8b37b0cf-075a-406e-8d5f-92b665ca85f2)


```
hm=sns.heatmap(data=data)
```


![323215874-4bbbf59a-e638-4c7b-bf5c-5298f9bada3b](https://github.com/user-attachments/assets/2df0e913-c749-4719-ad57-051b2dd85972)







# Result:


Thus, all the data visualization techniques of seaborn has been implemented.
