# XML Processing Monitor

## Project Overview

This project simulates an XML file processing pipeline used in financial systems. It monitors files from the moment they enter the system until the processing is completed.

The project focuses on identifying files that require operational attention by analyzing validation results and processing status.

---

## Business Problem

Every day, XML files are received from different systems. Some files fail during validation, while others pass validation but fail during processing.

The goal of this project is to identify only the files that require action and classify the reason for the failure.

---

## Technologies Used

* SQL
* Common Table Expressions (CTE)
* Window Functions (ROW_NUMBER)
* CASE WHEN
* LEFT JOIN
* Performance-Oriented Query Design

---

## Database Tables

* **file_logs** – Stores information about incoming XML files.
* **validation_results** – Contains validation results for each file.
* **processing_results** – Stores processing attempts and statuses.

---

## Business Rules

* Display only FAST files.
* Show validation failures as **Validation Error**.
* Show processing failures (based on the latest processing attempt) as **Processing Error**.
* Exclude successfully processed files from the report.

---

## Expected Output

The final report includes:

* File Name
* Validation Status
* Latest Processing Status
* Problem Type

This allows operational teams to quickly identify and investigate problematic files.

