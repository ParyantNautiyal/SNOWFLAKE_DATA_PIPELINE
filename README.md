# SNOWFLAKE_DATA_PIPELINE 
- ELT/ELT PIPELINE USING SNOWFLAKE
- TRANSFORMATION USING DBT

# In Snowflake 
 -- IAM USING SNOWSQL TO 
 
 1. Create a Stage/s
 -- Syntax
    -- For Reference -> https://docs.snowflake.com/en/sql-reference/sql/create-stage
    -- You can also create a stage using WEB UI
 -- Query -> create or replace stage stage_snoflake_internal 
             file format = (format_name = "csv") 
             comment = " Internal Stage  " 
 
 
 -- For External Stage Query -> CREATE STAGE my_azure_stage
                                STORAGE_INTEGRATION = azure_int
                                URL = 's3://mybucket/encrypted_files/'    ## bucket path
                                file_format = (format_name = "csv") 
                                credentials=(AWS_KEY_ID='$AWS_ACCESS_KEY_ID' AWS_SECRET_KEY='$AWS_SECRET_ACCESS_KEY')

 2. Push data into the stage --( Internal or External ) : Iam creating both internal as well as External stage (using S3)
    
     -- Query : PUT file:///tmp/data/orders_*01.csv @%stage_name AUTO_COMPRESS=FALSE;                               
 
 3.  Create a Snowpipe so data gets moved to the table as soon as stage gets updated

       -- create pipe pipe_name as copy into table_name from @stage_name;
 
 4. Create Streams and tasks if necessary (Iam Not creating any stream or tasks )
 
 # In DBT   
 
-- Prerequisites
- create a partner account for dbt in Snownflake
- Go through -> https://quickstarts.snowflake.com/guide/accelerating_data_teams_with_snowflake_and_dbt_cloud_hands_on_lab/ For better understanding
- make changes in required .yml files for data source/marts/staging/warehouses/schema/tables/tests in dbt
   
