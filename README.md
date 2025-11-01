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

# Coding:

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```
# Output:


<img width="1336" height="326" alt="image" src="https://github.com/user-attachments/assets/c4d639fd-c074-4abd-a8d6-26206f9fa105" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```

# Output:

<img width="744" height="581" alt="image" src="https://github.com/user-attachments/assets/0d53d198-5abe-4d20-bf59-14084aa7e7e0" />


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

# Output:


<img width="738" height="578" alt="image" src="https://github.com/user-attachments/assets/4302e551-f581-489c-bf7b-5bfffa496a9e" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

# Output:


<img width="997" height="656" alt="image" src="https://github.com/user-attachments/assets/609bde91-0842-42b1-b701-be07018f2a03" />


```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```

# Output:


<img width="822" height="607" alt="image" src="https://github.com/user-attachments/assets/a4bbf91b-af41-45ad-8eb5-5d9f28a7d7bb" />


```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

# Output:


<img width="822" height="583" alt="image" src="https://github.com/user-attachments/assets/6a68485d-4a5b-40d1-833c-b62cca3d55b6" />


```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```

# Output:

<img width="803" height="578" alt="image" src="https://github.com/user-attachments/assets/e523cc5e-83c2-4743-8d14-fd79b682a100" />


```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```

# Output:


<img width="706" height="572" alt="image" src="https://github.com/user-attachments/assets/3b22606f-c67b-4df5-9293-11cae267f591" />



```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

# Output:

<img width="710" height="564" alt="image" src="https://github.com/user-attachments/assets/ca715aa9-b84a-4cf8-bc8d-a7b86adc2310" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```

# Output:

<img width="731" height="571" alt="image" src="https://github.com/user-attachments/assets/8d4e8cfb-0b60-4ee6-a8b5-a34d8a28743d" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

# Output:

<img width="755" height="634" alt="image" src="https://github.com/user-attachments/assets/0a3358ad-f356-47c8-85dd-4f6b6d900103" />


# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
