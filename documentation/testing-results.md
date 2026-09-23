# Testing Results

## Testing Objective

The automation was tested to confirm that it correctly processes ERP files, detects supply risks, sends Outlook notifications, and prevents duplicate alerts.

## Test Results

| Test scenario                          | Expected result                                     | Actual result                                       | Status |
| -------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | ------ |
| Five ERP Excel files available         | Files copied to the processed-data folder           | All expected files were copied successfully         | Passed |
| Expected ERP file missing              | Failure recorded and process stopped                | Failure branch and notification worked correctly    | Passed |
| Current-month record identified        | Record evaluated by the risk conditions             | Current-month records were processed correctly      | Passed |
| Expiry period is four months or fewer  | Record classified as a near-expiry risk             | Test record was correctly identified                | Passed |
| Closing inventory is greater than zero | Alert permitted when other conditions are satisfied | Inventory condition worked correctly                | Passed |
| Valid supply risk detected             | Outlook notification sent                           | Alert email was received successfully               | Passed |
| Workflow run again with the same risk  | Duplicate notification prevented                    | No second email was sent after the alert was logged | Passed |

## Validated Test Case

The following synthetic record was used to test the near-expiry alert:

* Reporting month: September 2026
* Product ID: P15
* Market ID: M05
* Closing inventory: 262 units
* Months to expiry: 4
* Risk category: Near expiry

## Final Outcome

The completed workflow successfully:

* Processes and validates incoming ERP files
* Identifies qualifying supply risks
* Sends automated Outlook notifications
* Records alerts in a text-based log
* Prevents repeated alerts for the same risk
* Supplies processed data for Power BI reporting

All data used in this portfolio project is synthetic and does not contain patient, customer, or confidential company information.
