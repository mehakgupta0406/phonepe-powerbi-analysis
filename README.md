# PhonePe Payment Analytics Dashboard

An interactive Power BI portfolio project exploring transaction activity, payment outcomes, service performance, and user segments in a supplied PhonePe-labelled dataset.

**Status:** Dashboard complete. The report includes a styled payments overview, interactive filters, DAX measures, dynamic insights, and two supporting tooltip pages.

## Download and open

| File | Purpose | Download |
| --- | --- | --- |
| `PhonePe Dashboard Final.pbix` | Final interactive Power BI report | [Download dashboard](https://github.com/mehakgupta0406/phonepe-powerbi-analysis/raw/refs/heads/main/PhonePe%20Dashboard%20Final.pbix) |
| `Phonepe-Final-Dataset.xlsx` | Source workbook | [Download dataset](https://github.com/mehakgupta0406/phonepe-powerbi-analysis/raw/refs/heads/main/Phonepe-Final-Dataset.xlsx) |

GitHub cannot run an interactive PBIX report or preview these large binary files. Use the download links above, then open the dashboard in **Microsoft Power BI Desktop**.

1. Download the PBIX. Its saved data supports exploring the existing report.
2. Download the Excel workbook if you want to refresh the data.
3. If refresh reports a missing source, select **Transform data → Data source settings → Change Source** and point the Excel source to your downloaded `Phonepe-Final-Dataset.xlsx`.
4. Apply the changes and refresh. Source paths may need adjustment; refresh on a different computer has not been tested.

## Dashboard features

- **KPI cards:** total transactions, total transaction value, unique users, and successful transaction rate.
- **Growth indicators:** month-over-month transaction count and transaction value measures.
- **Monthly trends:** transaction value and volume on a dual-axis line chart.
- **Service performance:** payment value by service category.
- **Customer analysis:** top five users by transaction value and age-segment distribution.
- **Usage patterns:** weekday versus weekend transaction share.
- **Interactive controls:** month and payment-status slicers, chart selections, and supporting report tooltips.
- **Dynamic insights:** weekday transaction share and the leading service by transaction value, recalculated for the current filter context.
- **Presentation:** a consistent purple theme, aligned chart panels, and larger chart labels.

The age-segment chart counts users in the user table. Transaction-level filters do not necessarily reduce the user population when model relationships filter in one direction.

## Findings from the supplied dataset

These are descriptive findings from the unfiltered report, rather than claims about PhonePe's real business.

| Metric | Result |
| --- | --- |
| Total transactions | 300,000 |
| Total transaction value | Approximately 3.47 billion recorded amount units |
| Unique users | Approximately 108,000 |
| Successful transaction rate | 96.00% |
| Weekday transaction share | 71.6% |
| Leading service by transaction value | Loans |

The dataset's currency has not been independently confirmed, so monetary totals are not assigned a currency symbol here. Users, transactions, and dates may be subject to different filter contexts; interpret each visual according to its title and measure.

## Data and model

The source workbook contains two worksheets:

| Worksheet | Columns |
| --- | --- |
| `All_Users` | `User_ID`, `Name`, `Age`, `Join_Date` |
| `All_Transactions` | `Transaction_ID`, `Amount`, `User_ID`, `Service`, `Service Type`, `Payment_Status`, `Reason`, `Date` |

The report connects transactions to user records through `User_ID` and to a date table for monthly and weekday/weekend analysis. Measures are organized in the report's `Measures (2)` table.

Dataset origin, date coverage, synthetic-data status, and a specific reuse licence have not yet been documented. A full audit of source data quality is outside the completed dashboard validation.

## Dynamic insight logic

- **Weekday Share Insight:** weekday transaction count divided by total transaction count within the current selection, formatted as a percentage.
- **Leading Service Insight:** the service with the highest transaction value within the current selection. Ties are resolved alphabetically for a single, predictable result.
- Both insights return **No data** when the selection contains no transactions.

Validation checked the measures against multiple filter contexts:

| Selection | Weekday share | Leading service |
| --- | --- | --- |
| All data | 71.6% | Loans |
| January | 74.7% | Loans |
| Failed payments | 71.3% | Insurance |
| Pending payments | 72.9% | Loans |
| Empty selection | No data | No data |

The final saved dashboard was reopened in Power BI Desktop and both insight cards were checked for rendering. Validation covers the saved report and insight calculations; it does not establish dataset provenance or production readiness.

## Tools and project work

- Microsoft Power BI Desktop: data model, interactive visuals, slicers, and tooltips.
- DAX: KPI, growth, and filter-aware insight measures.
- Microsoft Excel: source workbook.
- AI assistance: dashboard styling, layout refinement, dynamic insight implementation, and documentation updates.

## Report versions

`PhonePe Dashboard Final.pbix` is the current report. The earlier `Phone pay Analysis.pbix` has been replaced to keep one clear dashboard entry point. Earlier committed versions remain available in Git history; the Excel dataset is retained.

## Data permission and attribution

The repository owner has confirmed permission to share the supplied files publicly. A source link and specific dataset licence have not yet been documented; this repository does not grant additional reuse rights.

This is an independent learning and portfolio project, not official PhonePe reporting.
