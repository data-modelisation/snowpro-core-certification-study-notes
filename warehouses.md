# Warehouses
Warehouse is used to provide <ins>compute resources</ins> to execute queries and operations.

Warehouses can be started and stopped at any time. They can also be resized at any time, even while running.   
A warehouse can be set to automatically resume or suspend, based on activity.   

## Typologies of the warehouse

Types of the warehouse :  
* Standard 
* Snowpark-optimized 

Standard is most suitable in most use cases 
Snowpark-optimized  is recommended for memory-intensive workloads such as ML training. 

Size : xs, s, m, l, xl, 2xl, 3xl 

Multi-cluster : add additional cluster and group queries in this one multi-cluster warehouse. Auto-scaling depending workflow. Great for concurrent users! 

For the complex workload it is better use bigger size of the warehouse! 

Scaling policy :  
- *Standard (default)*- favors starting additional warehouses.  
- *Economy* - favors conserving credits rather than starting additional warehouses. 
Cluster start only if the system estimates there's enough query load to keep the cluster <ins>busy for at least 6 minutes</ins>. Cluster shuts down after 5 to 6 consecutive successful checks. 

## Create warehouse

Admin->warehouses->new warehouse 

```sql
CREATE WAREHOUSE SECOND_WH
WITH
WAREHOUSE_TYPE=SNOWPARK
WAREHOUSE_SIZE = XSMALL
MIN_CLUSTER_COUNT = 1 
MAX_CLUSTER_COUNT = 2
AUTO_RESUME = TRUE 
AUTO_SUSPEND = 300 --5mins
COMMENT = 'This is our second warehouse '
```

```sql
DROP WAREHOUSE SECOND_WH;
```

# Tips 
Increasing the size of a warehouse does not always improve data loading performance!  

Larger is not necessarily faster for small, basic queries.  

# Links 
https://docs.snowflake.com/en/user-guide/warehouses-overview
