# EMS-Responses
## Project Goal
To create a working dashboard via Power BI to filter and determine the effectiveness of our emergency response in NYC. Additionally, this should allow users to discover any trends in the type of emergency from 2020 to 2024.
## Functional Requirements
- System should be able to return relevant facts acording to dimension variables
- System should be eable to establish primary and secondary key relations from normalized tables
- Filters for data should be flexible and optimized
## Data Requirements
All data were retrieved from NYC Open Data. <br>
**Source**<br>
[Source Download](https://data.cityofnewyork.us/Public-Safety/EMS-Incident-Dispatch-Data/76xm-jjuj/about_data) <br>
**Structure**<br>
Columns: 31 <br>
Rows: 7,300,000
## Data Dictionary <br>
[Dictionary Download](https://data.cityofnewyork.us/api/views/76xm-jjuj/files/81bbb2f5-70df-49cc-8552-f2ca8040bee8?download=true&filename=EMS_incident_dispatch_data_description.xlsx)
<br>

## Information Architecture
- 7.3 Million rows of data will be acquired via an API collection script in python and saved chunk by chunk into a csv file.
- Data file will be compressed into parquet format through Pyspark
- Transformation will be done via Pyspark scripts
- Final parquet files will be created for each respective dimension/table for normalization
## Data Storage
- I'm making use of google collab and google drive to store temporary parquet files. Then finalized data tables in parquet format will be stored on my local storage for use.
## Data Transofmration & Cleaning
- Making sure that all Null or NA values are replaced appropriately within context
- Making sure time data are in a cohesive and correct time format
- Remove irrelevant rows of data that add noise to the rest
- Ensure data types are consistent between columns and are correct
## Power BI Visuals
### Violent Incidents
I created an interactive line-graph visual which shows all stabbing and shooting calls that occured between 2020-2024. We can adjust the time and borough accordingly. <br>
![Violent Incidents](https://github.com/user-attachments/assets/064b34d4-56a3-4274-8314-b3c765200bea)
