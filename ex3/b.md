import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Display missing values
print(df.isnull().sum())
<img width="170" height="180" alt="Screenshot 2026-07-21 194405" src="https://github.com/user-attachments/assets/025dae41-8bed-4936-a82c-929e43c2afeb" />
