# Stages

Stages in Snowflake are locations used to store data.

Location where data is loaded FROM/TO.   
Not to be confused with datawarehouse stages.   

* Internal stages : snowflake managed   
* External stages : manged by external cloud provider (AWS, GCP , Azure )   

Uploading to stage : 

- by default AUTO_COMPRESS = TRUE 
- Data will be compressed .gz 
- Automatically encrypted (128 bit or 256 bit keys)

## Internal stages

There three differents types of stage : 

* User stages 
* Table stages 
* Internal Named stages
