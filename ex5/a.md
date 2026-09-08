import pandas as pd

# Load the dataset
df = pd.read_csv("Laptop_Specification.csv")

# Select numerical columns
num_data = df.select_dtypes(include=['number'])

# Create correlation matrix
corr_matrix = num_data.corr()

# Display correlation matrix
print("Correlation Matrix")
print(corr_matrix)

<img width="431" height="124" alt="Screenshot 2026-07-28 201332" src="https://github.com/user-attachments/assets/558dbb2a-d52a-4c4e-9008-4d1afa745c4f" />
