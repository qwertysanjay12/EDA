import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Display original column names
print("Original Column Names:")
print(df.columns)

# Rename columns
df.rename(columns={
    "Country/Region":"Country_Region",
    "New cases":"New_Cases",
    "New deaths":"New_Deaths",
    "New recovered":"New_Recovered",
    "Deaths / 100 Cases":"Deaths_100_Cases",
    "Recovered / 100 Cases":"Recovered_100_Cases",
    "Deaths / 100 Recovered":"Deaths_100_Recovered",
    "Confirmed last week":"Confirmed_Last_Week",
    "1 week change":"One_Week_Change",
    "1 week % increase":"One_Week_Percent_Increase",
    "WHO Region":"WHO_Region"
}, inplace=True)

# Display renamed column names
print("\nRenamed Column Names:")
print(df.columns)

<img width="467" height="164" alt="Screenshot 2026-07-21 194832" src="https://github.com/user-attachments/assets/573da1d7-3d35-4148-bf95-88ae16cc67d4" />
