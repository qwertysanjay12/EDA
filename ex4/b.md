import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Display data types before conversion
print("Before Conversion:")
print(df.dtypes)

# Convert data types
df["Confirmed"] = df["Confirmed"].astype(int)
df["Deaths"] = df["Deaths"].astype(int)
df["Recovered"] = df["Recovered"].astype(int)
df["Active"] = df["Active"].astype(int)

# Display data types after conversion
print("\nAfter Conversion:")
print(df.dtypes)
<img width="226" height="389" alt="Screenshot 2026-07-21 194905" src="https://github.com/user-attachments/assets/b25996ec-21b1-4cb7-b9a8-156777359e7d" />
