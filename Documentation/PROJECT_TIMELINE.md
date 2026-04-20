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
- **Expanded KPI Portfolio**:
    - **Average Satisfaction**: Developed a new measure to track the daily average patient satisfaction score.
    - **Referral Volume**: Implemented a measure to count the total number of patients referred to other departments.
- **Data Enrichment (DAX)**:
    - **Admission Status Flag**: Created a calculated column (`Admission Status`) using logic: IF admission flag is true then "Admitted" else "Not Admitted".
- **Visual Analytics Expansion**:
    - Integrated a Matrix Chart and Bar Chart to visualize the distribution of Admitted vs. Not Admitted patients.
- **Interactivity & UI**:
    - Formatted and implemented slicers for Month and Year.
    - Implemented layout containers (white rectangles) to group metrics and improve the dashboard's visual flow.

## Phase 4: Ongoing Development
- Finalizing the 'Monthly Overview' page with the newly added metrics.
- Commencing work on the 'Patient Demographics' page.
- Expanding time-intelligence analysis for peak hour identification.
- Proposed: `Patient Age Group` column using `SWITCH` logic for demographic segmentation.


now i added the patient referall bar chart.
made a new column for patient waittime status, i have chosen the threashhold as 30 mins, if the patient wait time is less than 30 mins then it is "Target Achieved" and if it is greater than 30 mins then it is "Target Missed".in report i made a donut chart for it.

made a donut hcart for patient gender distibution

made a bar chart for distribution of race wise patients

