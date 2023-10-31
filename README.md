# SNOWFLAKE_DATA_PIPELINE 
- ELT/ELT PIPELINE USING SNOWFLAKE
- TRANSFORMATION USING DBT

# In Snowflake 
 -- IAM USING SNOWSQL TO 
 
 1. Create a Stage/s
 -- Syntax
    -- For Reference -> https://docs.snowflake.com/en/sql-reference/sql/create-stage
    -- You can also create a stage using WEB UI
    -- Query 
    -  create or replace stage stage_snoflake_internal 
        file format = (format_name = <Name of file format > | TYPE = CSV) 
        comment = " Internal Stage  " 
   

 2. Push data into the stage -- ( Internal or External ) 
    
     - Query : PUT file:///tmp/data/orders_*01.csv @%stage_name AUTO_COMPRESS=FALSE;                               
 
 3.  Create a Snowpipe 

       - create pipe pipe_name as copy into table_name from @stage_name;
 
 4. Create Streams and tasks if necessary (Iam Not creating any stream or tasks )
 
 # In DBT   
- create a partner account for dbt in Snownflake
- Go through -> https://quickstarts.snowflake.com/guide/accelerating_data_teams_with_snowflake_and_dbt_cloud_hands_on_lab/ For better understanding
- make changes in required .yml files for data source/marts/staging/warehouses/schema/tables/tests in dbt
   
