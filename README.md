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
 Name: V Rishon Anand

 Reg no:212224240135
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
## Output
<img width="1459" height="410" alt="image" src="https://github.com/user-attachments/assets/ae7dada9-9c80-4f16-ac48-50950e373532" />


# 1. Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
## Output
<img width="774" height="716" alt="image" src="https://github.com/user-attachments/assets/da5f58d1-e0b8-4407-b2d2-0f04844275d0" />

## 2. Multi Line Plot
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
## Output
<img width="794" height="800" alt="image" src="https://github.com/user-attachments/assets/8c0dd776-d738-4820-825f-b657505f1740" />

# TO VISUALIZE RELATIONSHIPS
## 1. Bar chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
# Output
<img width="1737" height="824" alt="image" src="https://github.com/user-attachments/assets/fd6322d1-0155-45ee-8501-03352f0983ec" />

## 2. Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
## Output
<img width="859" height="687" alt="image" src="https://github.com/user-attachments/assets/c9a119d6-682f-4345-bfc1-aafbfe3a6ac5" />

## 3. Bubble Plot
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
## Output
<img width="899" height="686" alt="image" src="https://github.com/user-attachments/assets/50837369-311f-4793-aa00-c75d2a15b756" />

# TO CAPTURE DISTRIBUTIONS
## 1. Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
## Output
<img width="880" height="622" alt="image" src="https://github.com/user-attachments/assets/5b4d7261-431c-4e77-9ffb-13042e6f4b9d" />

## 2. Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
## Output
<img width="1698" height="784" alt="image" src="https://github.com/user-attachments/assets/75a98402-bc83-4e19-bda9-4587b5d9842d" />

## 3. Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
## Output
<img width="861" height="684" alt="image" src="https://github.com/user-attachments/assets/bf32eb9c-94e8-436c-a20d-bb92d39fe097" />

## 4. Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
## Output
<img width="890" height="811" alt="image" src="https://github.com/user-attachments/assets/dd325244-aa86-4e73-a215-282d3a8a174c" />

## 5. Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
## Output
<img width="892" height="795" alt="image" src="https://github.com/user-attachments/assets/2a28fd30-99f3-426b-a2a8-75b94400fb35" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
