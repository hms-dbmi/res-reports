# res-reports

This repository contains R code for creating monthly metrics reports for the SWB platform. The directions below correspond to AIM AHEAD. 

### Setting up the repository for the first time
1. Clone the repository
2. Add a folder in the AIM-AHEAD directory called "db-exports". This is where you will save the exported data from dynamoDB every month.

### Running the metrics report
1. Navigate to dynamoDB in the main account
2. Export the following tables. Make sure to export the entirety of the tables (you will need to make sure all records are showing on the screen).
   - StudyPermissions
   - Studies
   - aim-prod-va-sw-EnvironmentsSc
   - aim-prod-va-sw-Users
3. Save the tables in the db-exports directory with the following names:
   - StudyPermissions = aa-fisma-studypermissions.csv
   - Studies = aa-fisma-studies.csv
   - aim-prod-va-sw-EnvironmentsSc = aa-fisma-environments.csv
   - aim-prod-va-sw-Users = aa-fisma-users.csv
4. Open the  `swb-metrics-FISMA.Rmd` file in RStudio
5. Knit the file as a word document. This will save the metrics report in the same directory as a word doc.
6. Check the word document and rename to include the current month and year (for example swb-metrics-FISMA July 2025.docx)
