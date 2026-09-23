# Healthcare Supply Chain Risk Detection and Automation

A portfolio project demonstrating how healthcare supply-chain data can be transformed into operational insights and automated risk alerts using Excel, Power BI, Power Automate Desktop, Outlook, and Microsoft Lists.

## Business Problem

Healthcare supply teams manage large datasets containing inventory, demand, forecast, expiry, service-level, and supplier information. Manually reviewing this data can delay the identification of stock-outs, near-expiry inventory, supplier delays, and excess stock.

This project creates an automated workflow that detects relevant supply risks and sends alerts to support faster intervention.

## Solution Overview

The project combines business intelligence and workflow automation to:

* Analyse healthcare inventory and supply performance
* Monitor stock-outs, inventory health, service level, OTIF, forecast accuracy, and SLOB
* Detect near-expiry stock automatically
* Filter records using the current reporting month
* Send automated risk alerts through Outlook
* Record previously issued alerts
* Prevent duplicate notifications
* Support action tracking through Microsoft Lists

## Automation Workflow

1. Power Automate Desktop opens the processed Excel dataset.
2. The worksheet is loaded into a data table.
3. The flow determines the current month automatically.
4. Each record is evaluated against defined risk conditions.
5. A near-expiry risk is identified when:

   * The record belongs to the current month
   * Months to expiry are 4 or fewer
   * Closing stock is greater than 0
6. A unique risk key is generated for the record.
7. The alert log is checked to prevent duplicate notifications.
8. Outlook sends an automated email when a new risk is detected.
9. The risk key is added to the alert log.

## Example Detection

The automation successfully identified a near-expiry inventory risk for:

* Product ID: P15
* Market ID: M05
* Closing stock: 262 units
* Months to expiry: 4
* Risk category: Near-expiry inventory

## Tools Used

* Microsoft Excel
* Power BI
* Power Automate Desktop
* Microsoft Outlook
* Microsoft Lists
* OneDrive

## Key Skills Demonstrated

* Supply-chain analytics
* Inventory-risk detection
* Workflow automation
* Business process improvement
* Power BI dashboard development
* Conditional logic and data iteration
* Automated email notifications
* Duplicate-alert prevention
* Operational action tracking

## Project Outcome

The completed solution reduces the need to review large supply datasets manually. It converts inventory data into actionable risk alerts and ensures that the same issue is not repeatedly emailed during subsequent runs.

## Repository Structure

* `dashboard/` – Power BI dashboard screenshots
* `automation/` – Power Automate Desktop workflow screenshots
* `data/` – Anonymized sample data
* `tracker/` – Microsoft Lists screenshots
* `docs/` – Project documentation and workflow explanation

## Data and Privacy

This project uses synthetic or anonymized portfolio data. Personal email addresses, local computer paths, account information, credentials, and confidential company data are not included.
## Dashboard Preview

![Executive Supply Control Tower](dashboard/Executive%20Control%20Tower.png)

![Inventory Health and Forecast Analysis](dashboard/Inventory%20health%20and%20Forecast%20analysis.png)

![OTIF and Customer Delivery Performance](dashboard/OTIF%20and%20Customer%20Delivery%20Performance.png)

## Disclaimer

This is an independent portfolio project created for learning and demonstration purposes. It is not affiliated with, sponsored by, or endorsed by any healthcare or pharmaceutical company.
