import pandas as pd

data = {
    "customer_id": [1,2,3,4,5,1,2,3,1],
    "category": ["Fashion","Electronics","Fashion","Grocery","Fashion","Grocery","Electronics","Fashion","Fashion"],
    "amount": [1000,2000,1500,500,700,300,2500,1200,800]
}

df = pd.DataFrame(data)
# Total_revenue
total_revenue = df["amount"].sum()
print("The total revenue : ", total_revenue)

# Revenue by category
revenue_by_category = df[["category", "amount"]].values
print(revenue_by_category)

# Highest spent customer
highest_spent_customer = (
    df.groupby("customer_id")["amount"]
    .sum()
    .sort_values(ascending=False)
    .head(1)
)

print(highest_spent_customer)

# Category generated highest revenue
highest_revenue_generated_category = (
  df.groupby("category")["amount"]
  .sum()
  .sort_values(ascending=False)
  .head(1)
)
print(highest_revenue_generated_category)

# Customers ordering more than 2 times
more_than_2_times_ordered = (
  df.groupby("customer_id")["customer_id"]
  .count()
  .head(1)
)
print(more_than_2_times_ordered)

# Total revenue using loops
Total_revenue_using_loops = 0
for i in df["amount"]:
  Total_revenue_using_loops += i
print("Total revenue using loops:", Total_revenue_using_loops)
total = sum(df["amount"])
print(total)
