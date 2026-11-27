# PhonePe Transaction Analysis with Power BI

**Status: Work in progress**

A Power BI learning and portfolio project exploring the supplied PhonePe-labelled user and transaction dataset. The goal is to build an interactive report for understanding transaction activity, services, and payment outcomes.

## Download and open

| File | Open with | Download |
| --- | --- | --- |
| Power BI project (13.72 MiB) | Microsoft Power BI Desktop | [Download PBIX](https://github.com/mehakgupta0406/phonepe-powerbi-analysis/raw/refs/heads/main/Phone%20pay%20Analysis.pbix) |
| Excel dataset (21.34 MiB) | Microsoft Excel | [Download XLSX](https://github.com/mehakgupta0406/phonepe-powerbi-analysis/raw/refs/heads/main/Phonepe-Final-Dataset.xlsx) |

**Seeing “can’t show files that are this big” on GitHub?** The files are available to download. GitHub cannot display these files in its preview, and it does not run the interactive Power BI report. Use the download links above, or open a file’s page and select **Download raw file**.

### Open the Power BI project

1. Download both files.
2. Open `Phone pay Analysis.pbix` in Power BI Desktop.
3. If the Excel source cannot be found during refresh, use **Transform data → Data source settings → Change Source** to select your downloaded `Phonepe-Final-Dataset.xlsx`.
4. Review the queries and model, then refresh the data.

Source paths may need adjustment. Refresh on another computer has not yet been tested.

## Dataset

The supplied workbook contains two worksheets:

| Worksheet | Columns |
| --- | --- |
| `All_Users` | `User_ID`, `Name`, `Age`, `Join_Date` |
| `All_Transactions` | `Transaction_ID`, `Amount`, `User_ID`, `Service`, `Service Type`, `Payment_Status`, `Reason`, `Date` |

`User_ID` is a potential key for connecting user and transaction records; relationship quality still needs validation. Dataset origin, currency, date coverage, and whether the records are synthetic have not yet been documented.

## Current progress

- Initial Excel dataset and Power BI project uploaded.
- The PBIX contains a data model and one report page, `Page 1`.
- No saved visual definitions were found in the uploaded PBIX package.
- Data cleaning, model relationships, DAX measures, and analytical results still need validation.

## Planned analysis

- Review missing values, duplicates, and data types.
- Validate relationships between users and transactions.
- Define measures for transaction counts, amounts, and payment outcomes.
- Explore service categories and trends over time.
- Build report visuals, slicers, and filters.
- Add dashboard screenshots and findings supported by validated results.

These are planned tasks. Completed dashboards, business insights, and recommendations will be documented as the project develops.

## Tools

- Microsoft Power BI Desktop
- Power Query and DAX — planned for data preparation and measures
- Microsoft Excel

## Data permission and attribution

The repository owner has confirmed permission to share the supplied files publicly. A source link and specific dataset licence have not yet been documented; this repository does not grant additional reuse rights.

This is an independent learning project and is not official PhonePe reporting.
