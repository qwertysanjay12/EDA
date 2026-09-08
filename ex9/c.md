import pandas as pd

# Load the dataset
df = pd.read_csv("Laptop_TTest_Dataset.csv")

# Group statistics
stats = df.groupby("Category")["Sales"].agg(
    ["count", "mean", "std", "min", "max"]
)

print("Sales Statistics by Category")
print(stats)
<img width="319" height="62" alt="Screenshot 2026-09-01 181548" src="https://github.com/user-attachments/assets/b143852f-aeb4-4253-b486-609c0edaaaf6" />
