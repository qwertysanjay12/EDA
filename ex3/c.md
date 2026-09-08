import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Fill missing numerical values using mean
df["Confirmed"] = df["Confirmed"].fillna(df["Confirmed"].mean())
df["Deaths"] = df["Deaths"].fillna(df["Deaths"].mean())
df["Recovered"] = df["Recovered"].fillna(df["Recovered"].mean())
df["Active"] = df["Active"].fillna(df["Active"].mean())

print(df)
<img width="501" height="156" alt="Screenshot 2026-07-21 194434" src="https://github.com/user-attachments/assets/4fda47e8-35a7-498a-a403-c0fe56a82694" />
