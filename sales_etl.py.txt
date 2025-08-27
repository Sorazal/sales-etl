import csv
from openpyxl import Workbook

# Extract: read from CSV
sales = []
with open("sales.csv", "r") as file:
    reader = csv.DictReader(file)
    for row in reader:
        sales.append(int(row["amount"]))

# Transform: calculate metrics
total = sum(sales)
average = total / len(sales)
maximum = max(sales)
minimum = min(sales)

# Load: save results to Excel
wb = Workbook()
ws = wb.active
ws.title = "Sales Summary"

ws.append(["Metric", "Value"])
ws.append(["Total Sales", total])
ws.append(["Average Sale", average])
ws.append(["Highest Sale", maximum])
ws.append(["Lowest Sale", minimum])

wb.save("sales_summary.xlsx")
print("Report created: sales_summary.xlsx")
