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
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
df = sns.load_dataset("tips")
df
```
<img width="866" height="461" alt="image" src="https://github.com/user-attachments/assets/abcf28fa-ecca-4511-b89a-2560338a4ca1" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
<img width="998" height="626" alt="image" src="https://github.com/user-attachments/assets/80e99207-21c5-401a-8804-faeda28b245c" />

```
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill,label='Tip')
plt.xlabel("Day of the Week")
plt.ylabel("Amount")
plt.title("Average Tip and Total Bill by Day")
plt.legend()
```
<img width="976" height="643" alt="image" src="https://github.com/user-attachments/assets/2940245f-9f41-4c47-bd2f-ff870796b7ee" />

```
sns.barplot(x="day",y="total_bill",data=df,hue="sex",palette='Set2')
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Sex")
```
<img width="823" height="530" alt="image" src="https://github.com/user-attachments/assets/81b8773e-80c0-4367-b739-19d846310554" />

```
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=df)
plt.xlabel("Total Bill")
plt.ylabel("Tip Amount")
plt.title("Scatter Plot of Total Bill vs Tip")
```
<img width="928" height="522" alt="image" src="https://github.com/user-attachments/assets/f1e58803-8a6b-48d8-8735-27ebe4bda09e" />
```
np.random.seed(0)
marks = np.random.normal(loc=70,scale=10,size=100)
marks
```
<img width="726" height="413" alt="image" src="https://github.com/user-attachments/assets/c043fce7-87fb-4d70-b890-406200e7d910" />

```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', color='blue', shrink=0.7)
plt.xlabel("Marks")
plt.ylabel("Density")
plt.title("Histogram of Students Marks")
```

<img width="826" height="539" alt="image" src="https://github.com/user-attachments/assets/aeb08c98-fda4-4e22-a159-e3b72f788b5b" />

```
sns.histplot(data=df, x="total_bill", hue="sex", bins=20, kde=True, palette="Set2")
```
<img width="804" height="519" alt="image" src="https://github.com/user-attachments/assets/d206c300-493c-4e80-9ea5-bead77b90a75" />

```
sns.boxplot(data=df, x="day", y="total_bill", hue="sex")
```
<img width="913" height="552" alt="image" src="https://github.com/user-attachments/assets/a1615557-ec9d-44e3-a1a2-6f2a0ee6e56e" />

```
sns.boxplot(data=df, x="day", y="total_bill", hue="smoker", linewidth=3, width=0.7, boxprops={'facecolor': 'pink', 'edgecolor': 'red'}, whiskerprops={"color":"blue", "linestyle": "--", "linewidth": 1.6}, capprops={"color":"green", "linestyle": "--", "linewidth": 1.6}, medianprops={"color":"black","linewidth": 1.6}
            )
```

<img width="750" height="540" alt="image" src="https://github.com/user-attachments/assets/c98247b3-4365-40a8-a0cb-76c1807d606e" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```

<img width="827" height="461" alt="image" src="https://github.com/user-attachments/assets/e27d204f-bb3d-4b4d-903f-92384ac016e8" />

```
sns.violinplot(x="day", y="total_bill", hue="sex", data=df)

plt.title("Total Bill Distribution by Day and Gender")
plt.show()
```

<img width="710" height="558" alt="image" src="https://github.com/user-attachments/assets/5325e415-9288-4b75-8af6-245ef6081f11" />

```
sns.violinplot(x="day", y="total_bill", hue="sex", data=df, split=True)
plt.title("Split Violin Plot of Total Bill by Day and Gender")
plt.show()
```

<img width="710" height="558" alt="image" src="https://github.com/user-attachments/assets/9ac6f9fe-420f-400a-a005-62f64abc4a75" />

```
sns.violinplot(x="day", y="tip", data=df, inner="box")
plt.title("Tip Distribution by Day")
plt.show()
```

<img width="848" height="470" alt="image" src="https://github.com/user-attachments/assets/4a0ad7b5-c590-4780-af1d-44e9c9ed4efe" />

```
sns.kdeplot(data=df,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="769" height="464" alt="image" src="https://github.com/user-attachments/assets/8e638e28-996d-4690-8214-88fb9850fae5" />

```
sns.kdeplot(data=df,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set1',alpha=0.8)
```

<img width="821" height="459" alt="image" src="https://github.com/user-attachments/assets/bb012953-af19-427e-9bef-d179e860e275" />

```
sns.kdeplot(data=df,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set1',alpha=0.8)
```

<img width="811" height="465" alt="image" src="https://github.com/user-attachments/assets/a05a22c1-a417-4126-ba9e-b8504ffc8556" />

```
sns.kdeplot(data=df, x="total_bill", y="tip", fill=True)
plt.title("2D KDE Plot of Total Bill vs Tip")
plt.show()
```

<img width="852" height="469" alt="image" src="https://github.com/user-attachments/assets/bf7a42e6-d4d4-46bc-a095-b3fbd217e936" />

# Result:
 Thus the program executed successfully.
