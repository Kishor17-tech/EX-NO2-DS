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


# RESULT
        <<INCLUDE YOUR RESULT HERE>>
