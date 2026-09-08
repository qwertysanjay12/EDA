import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Perform data cleaning
df["Confirmed"] = df["Confirmed"].fillna(df["Confirmed"].mean())
df["Deaths"] = df["Deaths"].fillna(df["Deaths"].mean())
df["Recovered"] = df["Recovered"].fillna(df["Recovered"].mean())
df["Active"] = df["Active"].fillna(df["Active"].mean())

df["WHO Region"] = df["WHO Region"].fillna(df["WHO Region"].mode()[0])

df = df.drop_duplicates()

# Verify cleaned dataset
print("Missing Values:")
print(df.isnull().sum())

print("\nDuplicate Records:")
print(df.duplicated().sum())

print("\nCleaned Dataset:")
print(df)
<img width="509" height="407" alt="Screenshot 2026-07-21 194706" src="https://github.com/user-attachments/assets/aa498b20-ef19-415d-9075-847cfb22f929" />
