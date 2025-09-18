# EXNO2DS
# NAME:KISHOR K R
# REG NO:212224110032
# AIM:
  To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df
```

# OUTPUT:
<img width="1208" height="543" alt="Screenshot 2025-09-18 143529" src="https://github.com/user-attachments/assets/ef97f90d-1474-4f75-add6-7a3a91308cef" />


```
df.info()
```

# OUTPUT:
<img width="1206" height="439" alt="Screenshot 2025-09-18 143542" src="https://github.com/user-attachments/assets/c2d55a85-a344-48a2-8bc0-c9a43c4df9a1" />

```
df.describe()
```

# OUTPUT:
<img width="1216" height="335" alt="Screenshot 2025-09-18 143556" src="https://github.com/user-attachments/assets/7a8f942e-4df4-4280-b6a8-e7b174011461" />

```
df.dtypes
```

# OUTPUT:
<img width="1212" height="319" alt="Screenshot 2025-09-18 143605" src="https://github.com/user-attachments/assets/b916a2be-cce6-4482-94c4-f481523be48d" />


```
df.shape
```

# OUTPUT:
<img width="1193" height="84" alt="Screenshot 2025-09-18 143613" src="https://github.com/user-attachments/assets/a28f18a6-0eb1-434a-9007-79af9145d0f8" />


```
df['Age'].value_counts()
```

# OUTPUT:
<img width="1198" height="291" alt="Screenshot 2025-09-18 143622" src="https://github.com/user-attachments/assets/404e58de-6cc8-451c-844b-55d08790b775" />

```
df.set index("PassengerId", inplace=True)
df
```
# OUTPUT:
<img width="1210" height="495" alt="Screenshot 2025-09-18 143642" src="https://github.com/user-attachments/assets/4b6170c8-d5f1-4c04-b584-82e20f09809d" />

```
df.nunique()
```

# OUTPUT:
<img width="1211" height="303" alt="Screenshot 2025-09-18 143653" src="https://github.com/user-attachments/assets/27f77ae2-6329-4788-9dcd-dc8b6b838339" />

```
sns.countplot(data=df,x='Survived')
```

# OUTPUT:
<img width="1220" height="588" alt="Screenshot 2025-09-18 143719" src="https://github.com/user-attachments/assets/19dd40ed-c9d2-4c40-b441-b7545dd50647" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```

# OUTPUT:
<img width="1213" height="482" alt="Screenshot 2025-09-18 143730" src="https://github.com/user-attachments/assets/f993155d-a88e-415f-83fd-496320c3136f" />

```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=0.5)
```

# OUTPUT:
<img width="1221" height="625" alt="Screenshot 2025-09-18 143740" src="https://github.com/user-attachments/assets/14502153-6b69-44ca-9819-44ea43de9f53" />

```
df.boxplot(column="Age",by="Survived")
```

# OUTPUT:
<img width="1234" height="619" alt="Screenshot 2025-09-18 143750" src="https://github.com/user-attachments/assets/9323d0ca-3b46-41b4-8cfd-eb0187eab54d" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```

# OUTPUT:
<img width="1234" height="590" alt="Screenshot 2025-09-18 143759" src="https://github.com/user-attachments/assets/0f979e26-3927-4acf-8a83-0279f519ca6d" />

```
fig, axl=plt.subplots(figsize=(8,5))
plt=sns.boxplot(ax=axl,x='Pclass',y='Age',hue='Gender',data=df)
```

# OUTPUT:
<img width="1223" height="587" alt="Screenshot 2025-09-18 143807" src="https://github.com/user-attachments/assets/3081bce3-0286-41cc-95f9-7709594b4ee5" />

```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```

# OUTPUT:
<img width="1209" height="580" alt="Screenshot 2025-09-18 143819" src="https://github.com/user-attachments/assets/439fabb0-e64b-4cba-bd6e-b92d0723e954" />

```
import seaborn as sns
sns.catplot(x='Pclass',y="Age",hue="Gender",col="Survived",kind="box",data=df)
```

# OUTPUT:
<img width="1205" height="587" alt="Screenshot 2025-09-18 143832" src="https://github.com/user-attachments/assets/ab78cf3b-9b82-44c6-9ea2-4e80284c3d3f" />

```
sns.catplot(data=df,col="Survived",x="Gender",hue='Pclass',kind="count")
```

# OUTPUT:
<img width="1204" height="599" alt="Screenshot 2025-09-18 143840" src="https://github.com/user-attachments/assets/897476ec-b86e-4183-b1e9-f2cc5651d475" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```

# OUTPUT:
<img width="1220" height="621" alt="Screenshot 2025-09-18 143847" src="https://github.com/user-attachments/assets/04f25498-c506-45c8-9f5d-f7d4843516b5" />


```
corr=df.select dtypes(include=np.number).corr()
sns.heatmap(corr,annot=True)
```

# OUTPUT:
<img width="1213" height="595" alt="Screenshot 2025-09-18 143854" src="https://github.com/user-attachments/assets/4a32f674-2ac4-4109-aa1f-02f6bc068802" />


# RESULT
Thus the programs are executed successfully.
