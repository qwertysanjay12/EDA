import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Display duplicate records
print(df[df.duplicated()])
<img width="922" height="44" alt="Screenshot 2026-07-21 194532" src="https://github.com/user-attachments/assets/846e774b-b6e7-4af2-99aa-5ae99c5cd669" />
