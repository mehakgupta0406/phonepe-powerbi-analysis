# PhonePe Power BI Analysis

**Status: Work in progress**

A learning project for exploring the supplied PhonePe-labelled user and transaction dataset in Microsoft Power BI. Dataset origin, authenticity, and redistribution permissions have not yet been verified. This project is not presented as official PhonePe reporting.

## Project files

| File | Purpose | Size |
| --- | --- | --- |
| `Phone pay Analysis.pbix` | Current Power BI Desktop project | 14,384,968 bytes (13.72 MiB) |
| `Phonepe-Final-Dataset.xlsx` | Supplied Excel workbook | 22,375,168 bytes (21.34 MiB) |

## Current progress

- The supplied Excel workbook and Power BI project are preserved in their original form.
- The workbook contains `All_Users` and `All_Transactions` worksheets.
- The PBIX package contains a data model and one report page, `Page 1`. No saved visual definitions were found in the package.
- Data cleaning, model relationships, DAX measures, refresh behaviour, and analytical results have not been validated.
- No completed dashboard, business insights, or recommendations are claimed at this stage.

## Dataset structure

| Worksheet | Fields |
| --- | --- |
| `All_Users` | `User_ID`, `Name`, `Age`, `Join_Date` |
| `All_Transactions` | `Transaction_ID`, `Amount`, `User_ID`, `Service`, `Service Type`, `Payment_Status`, `Reason`, `Date` |

The workbook includes person-level fields and transaction records linked by user ID. It has not been established whether these records are synthetic or real. Currency, data provenance, date coverage, and the meaning of each status require confirmation.

## Open the project

1. Download both project files from the repository.
2. Open `Phone pay Analysis.pbix` in Microsoft Power BI Desktop.
3. If refresh requests a missing Excel source, update its path through **Transform data > Data source settings > Change Source** to the downloaded workbook.
4. Review the queries and model before refreshing. Local source paths may need to be adjusted. Refresh has not been tested on another computer.

## Planned work

- Confirm dataset source, permissions, and whether records are synthetic.
- Review missing values, duplicates, data types, and user-to-transaction relationships.
- Define and validate measures before creating visuals.
- Explore transaction amounts, services, payment statuses, and trends where supported by the data.
- Add dashboard screenshots, documented methods, and evidence-based findings as work is completed.

## Publication and reuse

Keep this repository private until the data source and sharing rights are confirmed and both the workbook and embedded PBIX data have been reviewed for sensitive information. A PBIX file can contain imported records even when the report canvas is blank.

No dataset licence has been established, and no redistribution licence is granted here. Confirm permissions and remove or anonymise sensitive records in both files before making the repository public. Do not assume that the PhonePe label establishes ownership, authenticity, or permission to publish.
