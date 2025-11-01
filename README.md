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
import seaborn as sns
import matplotlib.pyplot as plt
```

```
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1454" height="253" alt="image" src="https://github.com/user-attachments/assets/09302aca-8c84-412f-a42e-73bde77b8ef4" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="696" height="577" alt="image" src="https://github.com/user-attachments/assets/69a85b90-ff32-4eea-9bfb-66ca79c2dab4" />

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
<img width="719" height="583" alt="image" src="https://github.com/user-attachments/assets/09e070f6-af3b-4f89-8dc5-d0ebb6800c50" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1607" height="718" alt="image" src="https://github.com/user-attachments/assets/53ee0ff7-a5e0-495a-9328-c0274387db17" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="712" height="576" alt="image" src="https://github.com/user-attachments/assets/2cadfade-b1d2-4b44-83e3-43d128212f69" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="772" height="575" alt="image" src="https://github.com/user-attachments/assets/05e35815-c11b-420b-9398-0f67cfe1c526" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="768" height="573" alt="image" src="https://github.com/user-attachments/assets/575b7c89-19d8-4dd5-bb1f-295e6cb99be8" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1609" height="680" alt="image" src="https://github.com/user-attachments/assets/91c44b37-b1d9-44b4-af6c-229749c57224" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="722" height="567" alt="image" src="https://github.com/user-attachments/assets/51554ee8-2fa7-43fd-9b3d-47671a795afd" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="733" height="691" alt="image" src="https://github.com/user-attachments/assets/3b21a92d-ec0d-4809-b573-945fd1e2e67b" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="723" height="601" alt="image" src="https://github.com/user-attachments/assets/1994749c-f48d-451a-90a6-17629ae00c94" />











# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
