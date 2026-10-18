# etl-json-to-delta-reconciliation
PySpark ETL source-to-target reconciliation using nested JSON, Databricks, Delta tables, and automated data quality validations.
ETL JSON-to-Delta Reconciliation Framework

## Project Workflow

This project demonstrates ETL source-to-target reconciliation using PySpark in Databricks. It processes nested JSON data, flattens arrays and nested structures, loads the transformed data into a Delta table, and validates the results using a separate testing notebook.

## Technologies Used

- Python
- PySpark
- Databricks Free Edition
- Delta Lake
- Unity Catalog

## Project Workflow

1. Create a sample nested JSON dataset.
2. Store the JSON file in a Unity Catalog volume.
3. Read the JSON file into a PySpark DataFrame.
4. Flatten nested structures using `explode()`.
5. Load the transformed data into a Delta table.
6. Independently derive expected data in the testing notebook.
7. Perform source-to-target reconciliation.
8. Generate a consolidated validation report.

## Validation Reporting

The testing notebook collects validation results in a reusable Python function and converts them into a PySpark DataFrame. The report includes validation names, expected results, actual results, and PASS/FAIL status.

The report can be exported for review in Excel.

## Project Structure

The project contains a development notebook, a separate testing notebook, and a sample nested JSON source file.

## Purpose

This project demonstrates practical PySpark data processing, nested JSON transformation, Delta table usage, and ETL data quality testing.
