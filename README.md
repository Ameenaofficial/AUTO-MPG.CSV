# AUTO-MPG.CSV
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv(r"C:\Users\AMEENA\Downloads\archive\auto-mpg.csv")
print(df.head())

#SCATTER PLOT
plt.figure(figsize=(10,6))
grp_by=(df.groupby("model year")["displacement"].mean())
plt.scatter(grp_by.index,grp_by.values,color="maroon",marker="D")
plt.title("SCATTER PLOT")
plt.xlabel("Model year")
plt.ylabel("Displacement")
plt.grid(True)
plt.show()
