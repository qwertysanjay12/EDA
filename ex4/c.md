import pandas as pd

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Equal-Width Binning
df["Confirmed_EqualWidth"] = pd.cut(
    df["Confirmed"],
    bins=4,
    labels=["Low", "Medium", "High", "Very High"]
)

# Equal-Frequency Binning
df["Confirmed_EqualFrequency"] = pd.qcut(
    df["Confirmed"],
    q=4,
    labels=["Low", "Medium", "High", "Very High"]
)

# Display Result
print(df[["Country/Region","Confirmed","Confirmed_EqualWidth","Confirmed_EqualFrequency"]])
<img width="332" height="159" alt="Screenshot 2026-07-21 194937" src="https://github.com/user-attachments/assets/40acf528-7ecc-4191-86e5-a7c50370d09a" />

          
