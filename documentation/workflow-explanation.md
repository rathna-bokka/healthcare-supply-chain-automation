# Workflow Explanation

## Project Overview

This portfolio project demonstrates how healthcare supply-chain data can be processed, monitored, and converted into actionable alerts using Excel, Power BI, Power Automate Desktop, and Outlook.

The solution focuses on key supply-chain measures, including inventory availability, stock-outs, expiry risk, blocked inventory, forecast accuracy, service level, and OTIF performance.

## Workflow 1: ERP File Processing

1. The automation retrieves Excel files from the ERP export folder.
2. It verifies that all five expected files are available.
3. If the validation is successful, the files are copied to the processed-data folder.
4. The automation creates a processing log containing the date, time, number of files found, and completion status.
5. If files are missing, it records a failure message and stops the process.

## Workflow 2: Supply-Risk Detection

1. The automation opens the processed monthly supply workbook.
2. It reads the supply-chain records from the Excel worksheet.
3. Each record is checked against the current reporting month.
4. The workflow identifies inventory with four months or fewer remaining before expiry.
5. It confirms that closing inventory is greater than zero.
6. When both conditions are satisfied, Outlook sends a supply-risk notification containing the product, market, closing inventory, and expiry information.

## Duplicate-Alert Prevention

A unique risk key is created using the reporting month, product ID, market ID, and risk category.

Before sending an email, the automation checks the alert log. If the same risk key already exists, no duplicate notification is sent. New alerts are written to the log after the email is sent.

## Power BI Reporting

The processed data supports three Power BI dashboard views:

* Executive Supply Control Tower
* Inventory Health and Forecast Analysis
* OTIF and Customer Delivery Performance

These dashboards help decision-makers monitor supply performance, identify exceptions, and prioritize products requiring action.

## Tools Used

* Microsoft Excel
* Power BI
* Power Automate Desktop
* Microsoft Outlook
* Microsoft Lists or SharePoint for future tracker integration
