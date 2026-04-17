# Project Timeline: Hospital ER Dashboard

A professional log of the development process, milestones, and challenges encountered during the creation of the Hospital ER Dashboard.

## Phase 1: Data Preparation & Initial Cleaning
- **Raw Data acquisition**: Started with a CSV file containing 9,216 rows and 11 columns of raw Hospital ER data.
- **Format Conversion**: Converted the source CSV to XLSX for better compatibility and handling within the Power BI ecosystem.
- **Power Query Optimization**:
    - Identified null values in the `Patient satisfaction score` field; validated that the remaining data (99%+) is complete and error-free.
    - **Feature Engineering**: Created a custom column for Patient Full Name by merging `First Name` and `Last Name`.
    - **Data Standardization**: Standardized gender labels from abbreviations (M, F, NC) to full descriptive terms (Male, Female, Not Confirmed).

## Phase 2: Data Modeling
- **Dimensional Modeling**:
    - Created a dedicated `Date Table` using the `CALENDAR` function to support time-intelligence features.
    - Expanded the `Date Table` with `Month Name` and `Year` columns for enhanced slicing capabilities.
- **Relational Mapping**: Established a one-to-many relationship between the `Date Table` and the `Hospital ER_Data` table using the Date field as the connecting entity.

## Phase 3: Dashboard Development & Troubleshooting
- **Layout Design**: Commenced work on the 'Monthly Overview' page, establishing the visual hierarchy with basic shapes and key patient metric cards.
- **Timestamp Mismatch Resolution**: 
    - *Action*: Normalized the `Patient Admission Date` in the ER table by creating a new `Admission Date (Date Only)` column (removing precise timestamps).
    - *Result*: Successfully established the relationship with the `Date Table`, enabling accurate filtering across all visuals.
- **KPI Visual Development**:
    - **Patient Volume**: Added a primary metric card for "Total Patients" with an area chart visualizing daily spikes.
    - **Display Optimization**: Implemented a specialized display measure to ensure total counts (e.g., 9217) are shown clearly without scientific abbreviations like "9K".
    - **Average Wait Time**: Integrated the secondary KPI card for "Average Wait Time," mirroring the design of the patient volume card for consistency.
- **Interactivity & UI**:
    - Formatted and implemented slicers for Month and Year.
    - Implemented layout containers (white rectangles) to group metrics and improve the dashboard's visual flow.

## Phase 4: Continued Development (Next Steps)
- Proceed with the 'Patient Demographics' page.
- Expand time-intelligence analysis for peak hour identification.
 changed one of them to average wait time so i have new visual same as patient but referring t the wait time of the patients

