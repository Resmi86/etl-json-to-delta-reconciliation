
# ETL JSON-to-Delta Reconciliation Framework

PySpark ETL source-to-target reconciliation using nested JSON, Databricks, Delta tables, and data quality validations.

## Project Overview

This project demonstrates ETL source-to-target reconciliation using PySpark in Databricks. It processes nested JSON data, flattens arrays and nested structures, loads the transformed data into a Delta table, and validates the results using a separate testing notebook.

## Technologies Used

- Python
- PySpark
- Databricks Free Edition
- Delta Lake
- Unity Catalog

## Project Workflow

1. Create a sample nested JSON dataset containing customers, addresses, orders, and order items.
2. Store the JSON file in a Unity Catalog volume.
3. Read the JSON file into a PySpark DataFrame.
4. Flatten nested structures and arrays using `explode()`.
5. Load the transformed records into a managed Delta table.
6. Read the original JSON source and Delta target independently in the testing notebook.
7. Perform source-to-target reconciliation and generate a consolidated validation report.

## Validations Implemented

- Record count validation
- Missing record validation
- Extra record validation
- Duplicate key validation
- Column-level value comparison using null-safe comparisons
- Missing and extra column validation
- Data type validation
- Null value validation
- Negative testing using an intentionally modified target DataFrame

## Validation Reporting

The testing notebook collects validation results using a reusable Python function and converts them into a PySpark DataFrame. The report contains validation names, expected values, actual values, and PASS/FAIL status.

The report can be exported as a CSV file and opened in Excel.

## Project Structure

- `ETL_JSON_to_Delta_Reconciliation`: Development notebook
- `Test_ETL_Reconciliation`: Testing notebook
- `retail_source.json`: Sample nested JSON source file

## Purpose

This project demonstrates practical PySpark data processing, nested JSON transformation, Delta table usage, and ETL data quality testing.

## CI/CD Execution

GitHub Actions is configured to trigger the Databricks reconciliation job when changes are pushed to the `main` branch. 
