# SNOWFLAKE_DATA_PIPELINE 
- ELT/ELT PIPELINE USING SNOWFLAKE
- TRANSFORMATION USING DBT
 
# Prerequisites
- create a partner account for dbt in Snownflake
- Go through -> https://quickstarts.snowflake.com/guide/accelerating_data_teams_with_snowflake_and_dbt_cloud_hands_on_lab/
- make changes in required .yml files for data source/marts/staging/warehouses/schema/tables/tests
   
# In Snowflake 
 1. INGEST DATA ( FOR TESTING PURPOSES IAM INGESTING DATA FROM MY LOCAL STORAGE USING SNOWSQL/CLI )
 2. LOAD THE DATA INTO STAGING AREA -> USING PUT COMMAND
 3. CREATE STREAMS AND TASKS ( IF REQUIRED )
 4. CREATE PROCEDURE ( IF REQUIRED )
 5. TRANSFORM THE DATA (DBT)
 6. LOAD THE DATA INTO CURATED ZONE OR TRANSFER TO AN  EXTERNAL DESTINATION
 7. CREATE VISUALIZATION / OR USE THE DATA FOR ANALYTICS ( IF REQUIRED )

- ALL THE REQUIRED CODE IS AVAILABLE IN MY REPOSITORY 
