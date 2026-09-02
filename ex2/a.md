import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("country_wise_latest.csv")
top10 = df.sort_values(by = "Confirmed", ascending = False).head(10)
plt.figure(figsize=(8,5))
plt.bar(top10["Country/Region"], top10["Confirmed"])
plt.title("Top 10 Countries by Confirmed Cases")
plt.xlabel("country")
plt.ylabel("confirmed cases")
plt.xticks(rotation=45)
plt.show()
<img width="1532" height="752" alt="Screenshot 2026-09-02 162458" src="https://github.com/user-attachments/assets/a9a13dcb-b5dd-4e1c-89cb-695ae7badee3" />
