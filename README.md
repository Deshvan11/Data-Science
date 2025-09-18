# 📊 Data Science – Pandas Quick Reference

 Pandas/README.md

If you’re working with data in **Python**, **Pandas** is your best friend.  
Here’s a handy cheat sheet to speed up your analysis 🚀  

---

# 📥 Data Import

import pandas as pd

pd.read_csv("file.csv")

pd.read_excel("file.xlsx")

pd.read_sql(query, conn)

pd.read_json("file.json")

pd.read_parquet("file.parquet")

   

#    Data Selection

df["col"]                          # Select column

df.loc[row, "col"]                 # Label-based

df.iloc[0:5, 0:2]                  # Integer-based

df.query("col > 5")                # SQL-style filter

df[df["col"].isin(["A", "B"])]     # Multiple values


# Data Manipulation
df.groupby("col").agg({"col2": ["mean", "sum"]})

df.merge(df2, on="key")

df.pivot_table(values="val", index="idx")

df.sort_values(["col1", "col2"])

df.melt(id_vars=["id"], value_vars=["A", "B"])

df.apply(lambda x: x * 2)

# Data Cleaning
df.dropna(subset=["col"])

df.fillna(method="ffill")

df.drop_duplicates(subset=["col"])

df["col"].replace({"old": "new"})

df["col"].astype("category")

# String Operation
df["col"].str.contains("pattern")

df["col"].str.extract("(\d+)")

df["col"].str.split(",", expand=True)


# Statistics
df.describe()

df["col"].agg(["mean", "median", "std"])

df["col"].value_counts(normalize=True)

df.corr(method="pearson")

# Time Series
df.resample("M").mean()        # Monthly average

df.rolling(window=7).mean()    # Rolling mean

df.shift(periods=1)            # Shift values

# Export

df.to_csv("output.csv")

df.to_excel("output.xlsx")

df.to_parquet("output.parquet")
  
df.to_json("output.json")




