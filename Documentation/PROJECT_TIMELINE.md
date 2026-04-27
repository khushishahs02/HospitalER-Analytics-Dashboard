# Project Timeline: Hospital ER Dashboard

A professional log of the development process, milestones, and challenges encountered during the creation of the Hospital ER Dashboard.

## Phase 1: Data Preparation & Dimensional Modeling
- **Initial Ingestion**: Acquired raw ER data (CSV, 9,216 rows, 11 columns) and converted to XLSX for enhanced compatibility.
- **Power Query ETL**:
    - Identified and handled null values in `Patient satisfaction score`.
    - **Feature Engineering**: Generated `Patient Full Name` by merging first and last names.
    - **Data Standardization**: Replaced gender abbreviations (M/F/NC) with full descriptive labels.
- **Dimensional Modeling**: 
    - Created a dedicated `Date Table` (DAX) with `Month Name` and `Year` columns.
    - Established relationships using the Date field as the primary connecting entity.

## Phase 2: Dashboard Development & Performance Optimization
- **Layout & Visual Hierarchy**: Established the 'Monthly Overview' framework using structured containers and KPI cards.
- **Timestamp Mismatch Troubleshooting**:
    - *Challenge*: Discovered that exact timestamps in the admission field prevented successful relationship mapping with the Date Table.
    - *Resolution*: Normalized `Patient Admission Date` to a date-only format, enabling accurate cross-filtering.
- **KPI Implementation**:
    - Developed measures for **Patient Volume**, **Average Wait Time**, **Satisfaction Score**, and **Referral Volume**.
    - Implemented a display override measure to prevent large numbers from being abbreviated (e.g., ensuring 9,217 is fully visible).
- **Advanced Logic & Visuals**:
    - **Calculated Columns**: Implemented `Admission Status` (Admitted/Not Admitted) and `Wait Time Status` (Target Achieved/Missed based on 30min threshold).
    - **Comparative Analytics**: Integrated donut charts for gender and wait time performance, and bar charts for racial demographics and department referrals.

## Phase 3: Finalization & Strategic Insights
- **Full Dashboard Suite**: Finalized all 4 core pages (Overview, Demographics, Time/Referral, and Performance).
- **Interactivity**: Integrated cross-page navigation, dynamic slicers, and interactive tooltips.
- **Deployment & Review**:
    - [x] Captured high-resolution previews for documentation.
    - [x] Documented KPI insights and business impact.
    - [x] Completed final project review and structure optimization.
    - [x] Synchronized all development logs into the project timeline.
