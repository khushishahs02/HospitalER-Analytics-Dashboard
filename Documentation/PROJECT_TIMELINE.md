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
- **Current Challenge - Timestamp Mismatch**: 
    - *Observation*: Patient cards appeared blank when filtered by the new date slicers.
    - *Root Cause Analysis*: Discovered that the `Patient Admission Date` in the raw data contains precise timestamps, while the `Date Table` entries are fixed at midnight (00:00:00), causing a join failure.
- **Next Steps**: Implementing data transformation to normalize the `Patient Admission Date` to a date-only format (removing timestamps) and creating a new calculated column to ensure accurate relationship mapping.
