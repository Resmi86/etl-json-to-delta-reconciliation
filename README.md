# etl-json-to-delta-reconciliation
PySpark ETL source-to-target reconciliation using nested JSON, Databricks, Delta tables, and automated data quality validations.
ETL JSON-to-Delta Reconciliation Framework

Project Overview

This project demonstrates ETL source-to-target reconciliation using PySpark in Databricks. It processes nested JSON data, flattens arrays and nested structures, loads the transformed data into a Delta table, and validates the results using a separate testing notebook.

Technologies Used

Python

PySpark

Databricks Free Edition

Delta Lake

Unity Catalog

Project Workflow

Create a sample nested JSON dataset containing customers, addresses, orders, and order items.

Store the JSON file in a Unity Catalog volume.

Read the JSON file into a PySpark DataFrame.

Flatten nested structures and arrays using explode().

Load the transformed records into a managed Delta table.

Read the original source and Delta target independently in the testing notebook.

Perform source-to-target reconciliation and generate a consolidated validation report.

Validations Implemented

Record count validation

Missing record validation

Extra record validation

Duplicate key validation

Column-level value comparison using null-safe comparisons

Missing and extra column validation

Data type validation

Null value validation

Negative testing using an intentionally modified target DataFrame

Validation Reporting

The testing notebook collects validation results in a reusable Python function and converts them into a PySpark DataFrame. The report includes validation names, expected results, actual results, and PASS/FAIL status.

The report can be exported for review in Excel.

Project Structure

The project contains a development notebook, a separate testing notebook, and a sample nested JSON source file.



Purpose

This project demonstrates practical PySpark data processing, nested JSON transformation, Delta table usage, and ETL data quality testing.
