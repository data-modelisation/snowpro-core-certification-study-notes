# Stages

Stages in Snowflake are locations used to store data.

Location where data is loaded FROM/TO.   
Not to be confused with datawarehouse stages.   

* Internal stages : snowflake managed   
* External stages : manged by external cloud provider (AWS, GCP , Azure )   


## Internal stages

Uploading : 
- by default AUTO_COMPRESS = TRUE 
- Data will be compressed .gz 
- Automatically encrypted (128 bit or 256 bit keys)
  
There three differents types of stage : 
* User stages 
* Table stages 
* Internal Named stages

### User stages @~
- tied to a user 
- cannot be accessed by other user 
- every user has default stage 
- cannot be altered or dropped 
- put files to that stage before loading 
- explicitly remove files again 
- loading to multiple tables 
- referred to with **@~**

### Table Stages @%TABLE_NAME
* automatically created with a table 
* can only be accessed by one table 
* cannot be altered or dropped 
* load to one table 
* referred to with '@%TABLE_NAME'

### Named stages @STAGE_NAME
* CREATE SATGE ...
* Snowflake database object 
* Everyone with privileges can access it 
* Most flexible 
* Referred to with '@STAGE_NAME'


## External stages 

* CREATE STAGE ...
* Snowflake database object 
* Everyone with privileges can access it 
* Referred to with '@STAGE_NAME'

```sql
CREATE STAGE <stage_name>
 URL = 's3://bucket/path/'
```

