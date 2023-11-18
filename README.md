**Aim:**

To Perform Data Visualization on a complex dataset and save the data to a file.

**Explanation:**

Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

**Algorithm:**

### [Step:1 Importing necessary packages](https://github.com/AaronDominic/Mini-Project#step1-importing-necessary-packages)

### [Step:2 read the data set](https://github.com/AaronDominic/Mini-Project#step2-read-the-data-set)

### [Step:3 Execute the methods](https://github.com/AaronDominic/Mini-Project#step3-execute-the-methods)

### [Step:4 run the program](https://github.com/AaronDominic/Mini-Project#step4-run-the-program)

### [Step:5 get the output](https://github.com/AaronDominic/Mini-Project#step5-get-the-output)

**Program:**

```
import pandas as pd
```

```
import numpy as np
```

```
import matplotlib.pyplot as plt
```

```
import seaborn as sns
```

```
df=pd.read_csv("/content/credit_data_1.csv")
```

```
df
```

```
df.head()
```

```
df.info()
```

```
df.tail()
```

```
df.describe()
```

```
df.shape
```

[![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image001.png)](https://user-images.githubusercontent.com/143015231/282435053-686642b4-0735-4671-84b4-98a9a05d36b5.png)

```
df['dependents'].value_counts()
```

```
from sklearn.preprocessing import LabelEncoder
```

```
le = LabelEncoder()
```

```
df['dependents'] = le.fit_transform(df['dependents'])
```

```
df.head(10)
```

```
df.isnull().sum()
```

```
missing_percentage = (df.isnull().sum())/(df.shape[0])*100
```

```
missing_percentage
```

```
df.duplicated().value_counts()
```

```
sns.boxplot(y="dependents",data=df)
```

```
sns.countplot(y="dependents",data=df)
```

```
sns.histplot(y="dependents",data=df)
```

```
sns.scatterplot(df['income'],df['expenditure'])
```

```
sns.barplot(data=df, x='income', y='owner')
```

```
df.corr()
```

```
sns.heatmap(df.corr(),annot=True)
```

```
plt.figure(figsize=(20, 7))
```

```
sns.lineplot(data=df, x='age', y='expenditure')
```

```
plt.show()
```

```
sns.kdeplot(x=df['active'],data=df)
```

```
sns.countplot(y="card",data=df)
```

**Output:**

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image003.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image005.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image007.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image009.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image011.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image001.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image012.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image014.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image015.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image016.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image017.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image019.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image021.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image023.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image025.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image027.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image029.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image031.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image033.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image035.png)

![image](file:///C:/Users/bharg/AppData/Local/Packages/oice_16_974fa576_32c1d314_314f/AC/Temp/msohtmlclip1/01/clip_image037.png)

**Result:**

Hence the program to analyze the data set using data science is applied sucessfully.
