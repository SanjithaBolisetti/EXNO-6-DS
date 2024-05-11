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
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x, y=y)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/2b12c632-fe18-4d8c-bd97-00713672aad0)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/7b6b4f84-17f1-4020-9950-39b4988dc907)

```
sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/c28f2b49-7974-4e7f-8fd2-6617a51f4d2e)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.xlabel("X Label")
plt.ylabel("Y Label")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/4bccc2f3-bcf0-4b5d-82ca-c7d9f482ffcc)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips = sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/09c6e777-b0ac-4ebf-ab51-ea2854b748bd)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)
plt.xlabel('Time of the Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/ae457838-95f5-4299-b171-0d527330b396)

```
years = range(2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896 ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/fe6e1191-a693-4631-99b4-39cb993e9326)

```
dt = sns.load_dataset('tips')
sns.barplot(x = 'day', y = 'total_bill', hue = 'sex', data = dt, palette = 'Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/05cf7d9a-2a7e-476c-8822-3e2d7c5ea127)

```
import pandas as pd
tit = pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/2e97f178-0deb-43f7-808e-fa485968c3f0)

```
plt.figure(figsize = (8,5))
sns.barplot(x = 'Embarked', y = 'Fare', data=tit, palette = 'rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/038f3058-c44e-4e9d-91b3-b6998ad30ede)

```
plt.figure(figsize=(8,5))
sns.barplot(x = 'Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/e11680a8-8b84-402f-8eac-bea5f0adcf3f)

```
tips = sns.load_dataset('tips')
sns.scatterplot(x = 'total_bill', y='tip', hue='sex', data=tips)
plt.title('Total Bill')
plt.xlabel('Tip Amount')
plt.ylabel('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/6fbc0493-d32a-45ca-8a3c-18f4f387b232)

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/b105d74d-53ab-4649-9880-efe45fdea4f7)

```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var = np.random.randn(1000)
num_var = pd.Series(num_var, name= "Numerical Variable")
num_var
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/795de0fb-0eff-444e-826c-9a2a3e8341f6)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/ac6e6403-d3af-4bdb-a79c-3f2f8a643800)

```
df=pd.read_csv('titanic_dataset.csv')
sns.histplot(data = df, x="Pclass", hue="Survived", kde=True)
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/bd36f5f9-680a-499c-90fd-7b05dd319078)

```
import seaborn as sns
import pandas as pd
tips = sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips['total_bill'], hue=tips['sex'])
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/e213e1a8-62c5-40c3-83bf-8b6fe9196d55)

```
sns.violinplot(x = "day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette = 'Set1', inner = "quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/3c813ca3-78f5-458f-bd0c-a70381c83c84)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```

![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/a0953b35-e3f7-4d73-ba12-487f514a5bb9)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x = tip["total_bill"])
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/20fa1317-41ff-4454-b192-d19b5f8cbd39)

```
sns.kdeplot(data=df, shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/041c1604-a477-4b76-b7a2-793ab9ff057d)

```
import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

mart = pd.read_csv("supermarket.csv")
mart = mart[['Gender', 'Payment', 'Unit price', 'Quantity', 'Total', 'gross income']]
mart.head(10)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/9d3e6447-f3b3-4f91-8f52-76a53872972e)

```
sns.kdeplot(data = mart, x = 'Total')
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/e569bbe9-ed77-44c9-b9f6-a3efdfe684e7)

```
sns.kdeplot(data = mart, x = "Unit price")
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/4a45762d-ec12-4277-8c64-7ab2afdfaf07)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/20ef122d-0def-4f87-bbfb-f08c37a34379)
```
sns.kdeplot(data=mart, x='Total', hue='Payment', multiple= 'stack')
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/a29b67d9-920d-4204-9e8c-b08b81ca62ee)

```
sns.kdeplot(data=mart, x='Unit price', y='gross income')
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/d40ab813-5d6a-4905-8c71-580e15343dcf)

```
data = np.random.randint(low = 1, high = 100, size = (10, 10))
print("The data to be plotted.\n")
print(data)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/1bd3301d-7b81-48c3-a52c-ddf7b2700514)

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/808b3d51-a074-40cc-8429-67bcbaa4127b)

```
hm = sns.heatmap(data = data, annot=True)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/95113eac-5201-4d53-b64f-280c7befcb11)
```
hm = sns.heatmap(data = data)
```
![image](https://github.com/SanjithaBolisetti/EXNO-6-DS/assets/119393633/72ae0e70-23b9-4f9d-8d6c-370efd6ccfe7)


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
