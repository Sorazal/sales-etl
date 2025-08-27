# Sales ETL Project

This project demonstrates a simple **ETL pipeline** built with Python.

- **Extract**: Reads sales data from a CSV file (`sales.csv`)
- **Transform**: Calculates total sales, average sale, highest sale, and lowest sale
- **Load**: Writes the results into an Excel file (`sales_summary.xlsx`) using `openpyxl`

---

## 📂 Files in this repository
- `sales_etl.py` → The main Python script
- `sales.csv` → Example input data
- `sales_summary.xlsx` → Generated output (created after running the script)
- `requirements.txt` → Python dependencies

---

## ▶️ How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt

2. Run the ETL script:
   python sales_etl.py
3.Check the generated Excel report:

File: sales_summary.xlsx

Requirements

Python 3.8+

openpyxl library


Notes

This is a simple ETL example for learning purposes.
It can be extended to fetch data from APIs, transform large datasets, and load results into databases or cloud storage.
