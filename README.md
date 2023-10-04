# ODD2023-DataScience-Ex-03

```
import pandas as pd
from scipy import stats
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

```
from google.colab import files
uploaded = files.upload()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/8f5e780e-6f41-4b35-8c09-9a9097fcdc0a)
```
df = pd.read_csv('diabetes.csv')
df
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/681341b9-f544-404e-aebb-bd7a40fe0d95)

```
df.isnull().sum()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/33227d64-bb63-4af4-9ecd-e160317b93c1)

```
q1 = df.quantile(0.25)
q3 = df.quantile(0.75)
iqr = q3 - q1
iqr
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/dbdd2e01-33ed-4a22-bcd4-904cf3971b6e)

```
low = q1 - 1.5*iqr
high = q1 + 1.5*iqr
df = df[(df >= low) & (df <= high)]
df
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/445bb098-872e-4081-8bbc-fb19d3d14804)


```
sns.boxplot(df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/b65daa94-f541-4b22-91be-84e480fdaf39)

```
sns.displot(x ="Glucose", data = df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/f11ac48c-629b-42ee-b637-156af363c45a)

```
sns.displot(x ="BloodPressure", data = df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/a28dbad5-b5b4-428a-a053-fc3b4b5846a4)

```
sns.displot(x ="BMI", data = df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/9f15c4b1-914a-4d64-851c-b900d8b4fadd)

```
sns.displot(x ="DiabetesPedigreeFunction", data = df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/95b633da-38fb-4c12-af27-616e8e048c7d)

```
sns.displot(x ="Age", data = df)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/7b006225-450b-488a-baec-be0a882efffa)

```
from google.colab import files
uploaded = files.upload()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/673f281e-bce9-4d70-857f-09d58620dfb1)

```
df = pd.read_csv('employeesal.csv')
df
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/24c97489-8e6a-4027-9605-0cfcbefe0400)

```
df.isnull().sum()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/f2d92314-dd85-45fd-bd07-e802ef3a8727)

```
numeric_cols = df.select_dtypes(include=[int, float])
q1 = numeric_cols.quantile(0.25);
q3 = numeric_cols.quantile(0.75);
iqr = q3 - q1
iqr
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/7aa547c1-4a36-4718-b739-c214f7bc5304)

```
low = q1 - 1.5*iqr
high = q1 + 1.5*iqr
numeric_cols = numeric_cols[(numeric_cols >= low) & (numeric_cols <= high)]
numeric_cols.dropna()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/a2091ffe-1a79-4862-85c9-cd782db19e0d)

```
sns.boxplot(numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/60720920-3038-41e6-90c8-8d265d452f7f)

```
sns.histplot(x = 'Experience_Years',data = numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/43929001-b7ec-41a5-8922-40ff33e7b292)

```
sns.histplot(x = 'Age',data = numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/9109e564-d112-4701-a269-6ae51a6671ad)

```
sns.histplot(x = 'Salary',data = numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/a449e0cd-8718-4af7-b013-cee8b6b2c40d)

```
from google.colab import files
uploaded = files.upload()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/75622348-f807-4022-8986-a5f8fdae78aa)

```
df = pd.read_csv('SuperStore.csv')
df
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/c302e1c1-df37-4b54-935a-d1341c685af5)

```
df.isnull().sum()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/f12d9953-8e19-49a2-b832-1806f5b2f0fd)

```
df.dropna()
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/4e3f84a8-ec7b-434d-b2d2-2dc9a4060613)

```
df.dtypes
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/954b7688-aa1b-4cd0-85b1-d82b46f461a0)

```
numeric_cols = df.select_dtypes(include=[float])
q1 = numeric_cols.quantile(0.25);
q3 = numeric_cols.quantile(0.75);
iqr = q3 - q1
iqr
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/dd61c574-652c-498c-ab96-db93970a8ba2)

```
low = q1 - 1.5*iqr
high = q1 + 1.5*iqr
numeric_cols = numeric_cols[(numeric_cols >= low) & (numeric_cols <= high)]
```

```
sns.boxplot(numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/4aa63367-b85b-4aa1-9378-29d1a8adf3a6)

```
sns.histplot(x = 'Sales',data = numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/6e234b34-f8bf-45d0-bc92-94b721f78b85)

```
sns.countplot(x="Postal Code", data=numeric_cols)
```
![image](https://github.com/Vaish-1011/ODD2023-DataScience-Ex-03/assets/135130074/74bf18cb-8a8b-4826-a6f7-841a56eabf84)
