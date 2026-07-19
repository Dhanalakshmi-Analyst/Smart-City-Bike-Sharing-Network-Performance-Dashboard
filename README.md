# Smart City Bike Sharing — Network Performance Analysis

Data Analytics Module-End Project | Power Query · Power BI · DAX

## Project overview

This project analyzes 2,856 station-level records from a public bike-sharing
network spanning 25 city contracts. It covers station capacity, live bike
availability, operational status, banking facilities, bonus-enabled stations,
and update patterns over time (2022-2025).

The dataset was cleaned and transformed in Power Query, structured into a
star-schema data model (Sales fact table + Dim_City and Dim_Date dimension
tables), and analyzed using 16 custom DAX measures in Power BI.

**Note:** this dataset does not include trip-level, cost, or revenue data.
All findings are based on infrastructure capacity and live-availability
snapshots only (confirmed with course mentor).

## Folder contents

| File | Description |
|---|---|
| `bike_sharing_full_documentation.docx` | Full project documentation — overview, data cleaning, data modeling, DAX measures, dashboard features, and business insights (Descriptive/Diagnostic/Predictive/Prescriptive) |
| `bike_sharing_summary_report.docx` | One-page executive summary of key findings |
| `[project].pbix` | Power BI file — data model, DAX measures, and interactive dashboard |
| `icons/` | Custom teal-themed icon set used on the dashboard (bicycle, docking station, location pin, gauge, warning, checkmark) |
| Screenshots | Cleaning/transformation steps, data model, and dashboard views (embedded in the documentation) |

## Tools used

- **Microsoft Excel** — initial review and address-field cleanup
- **Power Query** — data cleaning, type conversion, Latitude/Longitude split, Dim_City and Dim_Date table creation
- **Power BI Desktop** — star-schema data modeling, DAX measures, dashboard design
- **DAX** — 16 measures including CALCULATE, SUMX, DIVIDE, COUNTROWS, DISTINCTCOUNT

## Data model

**Fact table:** Sales — station-level operational records
**Dimension tables:**
- Dim_City — 25 unique city contracts (Many-to-1 relationship on Contract Name)
- Dim_Date — unique Month-Year periods (Many-to-1 relationship on Update Month Year)

## Key findings (summary)

- Total bike stand capacity: **57,203** across **25 contracts**
- Available bikes: **19,646** | Available bike stands: **32,118**
- Network utilization rate: **66%**
- Active (OPEN) station capacity: **93.8%** | Closed: **6.2%**
- Capacity mismatch flagged: **5,439 stands (9.5%)** between reported Bike Stands and Available Bikes + Available Bike Stands
- Banking-enabled capacity: **11.1%** | Bonus-enabled stations: **70 of 2,856**
- **91.6%** of all records are dated in 2025, indicating a recent increase in data collection frequency rather than sudden network growth

See `bike_sharing_full_documentation.docx` for the complete analysis,
methodology, and recommendations.

## How to view

1. Open the `.pbix` file in Power BI Desktop to explore the interactive dashboard.
2. Open either `.docx` file in Microsoft Word for the written report.
3. Use the slicers on the dashboard (Contract Name, Status, Update Month Year) to filter results by city, operational status, or time period.
