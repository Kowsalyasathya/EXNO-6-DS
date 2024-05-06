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
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/0d729872-7216-419c-8749-f310077b7ec7)
### 1.Line Plot:
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[2,5,1,5,2]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/945d924c-aeeb-4415-a0b6-ea60b3e8c89e)
### 2.Multi Line Plot:
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/c93814cb-41b4-4813-81a6-1be3d8639a73)
### TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart:
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/d0430ad4-fa40-468d-bfe0-b4c709f3ca0d)
### 2.Scatter Plot:
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/8cdc6b74-6acd-488e-b01c-1646c1fc37f9)
### 3.Bubble Chart:
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 150))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/cbd39bdf-37fe-4a75-a2a6-5b5a47c756bd)
### TO CAPTURE DISTRIBUTIONS
### 1.Histogram:
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/7a66b328-991a-4ccb-bd62-a9d02883d686)
### 2.Box Plot:
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/aef8fc49-a951-4577-9934-dee0f4de25e7)
### 3.Violin Plot:
```
plt.figure(figsize=(10, 6))
sns.violinplot(x="class", y="age", hue="survived", data=titanic, split=True)
plt.title("Violin Plot of Age by Class and Survival")
plt.xlabel("Class")
plt.ylabel("Age")
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/00ae7b76-9cf6-4082-9149-b6de24b3b238)
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/73e6f4d4-aefe-4e94-9c7c-3cf88e35ca45)
### 4.Density Plot:
```
import matplotlib.pyplot as plt
titanic = sns.load_dataset("titanic")
plt.figure(figsize=(8, 5))
sns.kdeplot(data=titanic['age'], shade=True)
plt.title("Density Plot of Age")
plt.xlabel("Age")
plt.ylabel("Density")
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/c663d4c4-aa44-4c1c-b088-f751babbae3e)
### 5.HeadMap:
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
````
![image](https://github.com/Kowsalyasathya/EXNO-6-DS/assets/118671457/cd60bbc2-997c-48bb-b70b-ebcdd1bd2619)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
