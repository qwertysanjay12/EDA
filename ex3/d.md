import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Fill missing categorical values using mode
df["WHO Region"] = df["WHO Region"].fillna(df["WHO Region"].mode()[0])

print(df)
<img width="506" height="159" alt="Screenshot 2026-07-21 194458" src="https://github.com/user-attachments/assets/ffc06e25-cbe9-4220-9089-b10217bb8937" />
