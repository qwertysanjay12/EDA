import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Display unique WHO Region values
print(df["WHO Region"].unique())
<img width="458" height="44" alt="Screenshot 2026-07-21 194638" src="https://github.com/user-attachments/assets/c1f9babd-33db-4f77-bb54-ad248752e1fd" />
