import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Remove duplicate records
df = df.drop_duplicates()

print(df)
<img width="497" height="154" alt="Screenshot 2026-07-21 194603" src="https://github.com/user-attachments/assets/e13e1def-eaec-40d3-8d11-1f45db01962d" />
