import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
df = pd.read_csv("Laptop_Specification.csv")

# Select numerical columns
num_data = df.select_dtypes(include=['number'])

# Correlation matrix
corr_matrix = num_data.corr()

# Draw heatmap
plt.figure(figsize=(8,6))
sns.heatmap(corr_matrix,
            annot=True,
            cmap="coolwarm",
            fmt=".2f")

plt.title("Correlation Matrix Heatmap")
plt.show()
<img width="864" height="447" alt="Screenshot 2026-07-28 201227" src="https://github.com/user-attachments/assets/f76bf64c-28a1-498f-aaa7-b42ecd8de084" />
