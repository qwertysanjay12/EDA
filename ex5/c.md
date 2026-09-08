import pandas as pd

# Load the dataset
df = pd.read_csv("Laptop_Specification.csv")

# Select numerical columns
num_data = df.select_dtypes(include=['number'])

# Correlation matrix
corr_matrix = num_data.corr()

print("Highly Correlated Variable Pairs\n")

for i in range(len(corr_matrix.columns)):
    for j in range(i + 1, len(corr_matrix.columns)):
        value = corr_matrix.iloc[i, j]
        if value > 0.8 or value < -0.8:
            print(corr_matrix.columns[i],
                  "<-->",
                  corr_matrix.columns[j],
                  "=",
                  round(value, 2))
                  <img width="250" height="107" alt="Screenshot 2026-07-28 201305" src="https://github.com/user-attachments/assets/df019197-eba6-49ef-aabe-e8662cf1e3a1" />
